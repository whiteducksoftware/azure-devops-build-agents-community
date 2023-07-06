```yaml
trigger:
  - master

pool:
  vmImage: 'ubuntu-latest'

jobs:
  - job: powershell
    displayName: PowerShell Container Example
    # Set PowerShell container image with tag
    container: mcr.microsoft.com/powershell:latest
    steps:
      # Execute PowerShell inline script
      - script: pwsh -Command "Write-Host Hello World"
        displayName: PowerShell Inline
      # Execute PowerShell inline script with environment variable
      - script: pwsh -Command "Write-Host Hello $NAME"
        displayName: PowerShell Inline + Environment Variable
        env:
          NAME: World
      # Execute PowerShell script file with environment variable
      - script: pwsh -File ./getEnvironmentVariable.ps1
        displayName: PowerShell Script
        env:
          NAME: World
```

getEnvironmentVariable.ps1

```powershell
Write-Host Hello $env:NAME
```
