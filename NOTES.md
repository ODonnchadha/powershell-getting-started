## PowerShell: Getting Started

- by Michael Bender
- This is an introductory course on PowerShell and how to use it for basic IT operations support.

- OVERVIEW:
    - Windows. Mac. Linux. Scripting & toolmaking.

- INTRODUCTION:
    - PowerShell/PowerShell Core (multiple platforms) is an execution engine.
    - ISE: Original integrated scripting engine. Visual Studio code. Cross-platform with extensions.
    - Windows admin center. Windows server & Microsoft Azure. PowerShell backend.
    - Windows Powershell.
        - Based on .NET standard. Built into Windows. Windows only. Feature complete. Full set of Windows PowerShell commands.
    - PowerShell Core:
        - Based on .NET Core. Download from GitHub. Runs on any platform. Open source. Sunset of Windows PowerShell commands.
    - Why?
        - (1) PowerShell is baked into Microsoft Tools. (2) Automation. (3) Multi-platform. (VS Code.)
        - (4) Better than GUI. (5) Certification. (6) Everybody is using it.
    ```javascript
        get-service
        get-service |
            Where-Object Status -eq 'Stopped'
        get-service |
            Where-Object Status -eq 'Stopped' |
            select-object Name, Status
    ```
    ```javascript
        $data =  get-service | Where-Object Status -eq 'Stopped' | select-object Name, Status
        $data
        $data | out-file .\stopped-services.csv
        notepad .\stopped-services.csv
        $data | export-csv .\stopped-services2.csv
        get-content .\stopped-services2.csv | more
    ```
    - Introduction to Windows PowerShell console. 
    - Installing the RSAT Tools on Windows.
    - Introduction to PowerShell Core.
    ```javascript
        $PSVersionTable
        (get-command).count
    ```
- BASICS:
    - 
