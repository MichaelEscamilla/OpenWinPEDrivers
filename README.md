OpenOSD
> [!NOTE]
> Last Updated: 2025.01.08


# WinPE Drivers Repository
The WinPE Drivers Repository is a Community effort to provide a central location for WinPE Drivers.  These Drivers can be used with OSDCloud (soon), MDT, SCCM, or any other Deployment Solution that uses WinPE Boot Images. 

The content of this Repository is provided as-is, and no warranty is given.  Please test these Drivers in your environment before using them in Production.

Currently this Repository is being finalized, with a Community release later this month.


## Community Contributions
This Repository is a Community effort, and we welcome your contributions.  If you have WinPE Drivers that you would like to add to this Repository, please submit a Pull Request.  We will review your submission and merge it into the Repository.

If you have any feedback from testing these Drivers, please submit an Issue.  We will review your feedback and update the Repository as needed.


## OSDCloud Integration
OSDCloud will soon remove the `CloudDriver` parameter when using `Edit-OSDCloudWinPE`. Instead, you will be able to select WinPE Drivers from this Repository.


## Git Requirement
Since this Repository will be cloned, you will want to make sure that you have Git for Windows https://gitforwindows.org/ installed.  The easy way to install Git for Windows is to use Winget.

```powershell
# Install Git for Windows using Winget
winget install -e --id Git.Git
```

Since Git for Windows needs to modify your Path, you will need to relaunch PowerShell, or run this snippet:

```powershell
function Update-EnvironmentValues {
    $locations = 'HKLM:\SYSTEM\CurrentControlSet\Control\Session Manager\Environment','HKCU:\Environment'
    $locations | ForEach-Object {   
        $k = Get-Item $_
        $k.GetValueNames() | ForEach-Object {
            $name = $_
            $value = $k.GetValue($_)
            Set-Item -Path Env:\$name -Value $value
        }
    }
}
Update-EnvironmentValues
```


## Clone the WinPE Drivers Repository
You can use the following snippet to clone the Repository to your local machine to use the Drivers.  It is recommended that you use the specified location as this will be the default location when using OSDCloud v2.  If you plan on Contributing and submitting a Pull Request, you will want to fork the Repository and clone your fork to a different location.

```powershell
# Source Git Repository
$Source = 'https://github.com/OSDeploy/WinPEDrivers.git'

# Destination Folder
$Destination = $env:ProgramData + "\OSDeploy\WinPEDrivers\"

# Git Clone Reset and Clean
# This method is used to keep the Destination in sync with changes from the Source
git clone "$Source" "$Destination"
Push-Location "$Destination"
git fetch origin
git reset --hard origin/main
git clean -f -d
Pop-Location
```