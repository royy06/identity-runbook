# OBJECTIVE
# ------------------------------
# Automate access review and enforce least privilege principles by:
# 1. Listing all users, their group memberships, and roles.
# 2. Identifying roles or permissions outside the allowed minimum.
# 3. Generating a CSV summary for documentation and runbook submission.

# ------------------------------
# PREREQUISITES
# ------------------------------
# 1. Admin access to Microsoft Entra ID / Microsoft 365.
# 2. PowerShell installed (Windows 10/11 recommended).
# 3. AzureAD or AzureADPreview module installed.
#    Install via: Install-Module AzureAD
# 4. Test users and security groups already created (Project 1).
# 5. Defined allowed roles for least privilege enforcement.

# ------------------------------
# 1. Connect to Microsoft Entra ID
# ------------------------------
Connect-AzureAD
# A pop-up will ask for admin credentials

# ------------------------------
# 2. Define allowed roles / whitelist
# ------------------------------
$AllowedRoles = @(
    "User",
    "Guest",
    "Member"
)

# ------------------------------
# 3. Retrieve all users
# ------------------------------
$Users = Get-AzureADUser -All $true

# ------------------------------
# 4. Create output folder
# ------------------------------
$OutputFolder = "$env:USERPROFILE\Documents\Project2_Access_LeastPrivilege"
New-Item -ItemType Directory -Path $OutputFolder -Force

# ------------------------------
# 5. Initialize output CSV
# ------------------------------
$OutputCSV = "$OutputFolder\AccessReview.csv"
$Results = @()

# ------------------------------
# 6. Check each user
# ------------------------------
foreach ($user in $Users) {
    # Get group memberships
    $Groups = Get-AzureADUserMembership -ObjectId $user.ObjectId | Select-Object DisplayName,ObjectType

    # Get directory roles
    $Roles = Get-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId | Select-Object AppRoleId,ResourceDisplayName

    # Identify roles not in allowed list
    $ExcessRoles = @()
    foreach ($role in $Roles) {
        if (-not ($AllowedRoles -contains $role.ResourceDisplayName)) {
            $ExcessRoles += $role.ResourceDisplayName
            # Optionally remove the role
            # Remove-AzureADUserAppRoleAssignment -ObjectId $user.ObjectId -AppRoleAssignmentId $role.Id
        }
    }

    # Create result object
    $Results += [PSCustomObject]@{
        User           = $user.UserPrincipalName
        Groups         = ($Groups.DisplayName -join ", ")
        Roles          = ($Roles.ResourceDisplayName -join ", ")
        ExcessRoles    = ($ExcessRoles -join ", ")
        LeastPrivilege = if ($ExcessRoles.Count -eq 0) { "✅" } else { "❌" }
    }
}

# ------------------------------
# 7. Export results to CSV
# ------------------------------
$Results | Export-Csv -Path $OutputCSV -NoTypeInformation

Write-Host "Access review complete. Results exported to $OutputCSV"
