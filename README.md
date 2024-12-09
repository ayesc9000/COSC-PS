# Command Journal Summary

Below is a summary of all the commands from the journal, categorized by their general functionality.

| Cmdlet | Description |
| --- | --- |
| Get-Help | Displays help information about a specified PowerShell cmdlet. |
| Set-ExecutionPolicy | Set the permissions for running external PowerShell scripts, such as disabling script execution altogether, allowing only local scripts, or allowing any scripts including from the internet. |
| Select-Object | Select a specific property or properties in an object or select specific objects from within a collection of objects using parameters. |
| Get-Module | Get a list of available PowerShell modules, can be combined with PSRemoting to get modules on a remote system. |
| Import-Module | Import a module into the current PowerShell session, can be used with PSRemoting to import on a remote system. |
| Get-Variable | Get all currently defined variables in the current PowerShell session. |
| Remove-Variable | Remove a named variable entirely. |
| Read-Host | Obtain input from the user as a string. |
| Write-Host | Write text optionally from a variable to the screen. |
| Get-Credential | Prompt the user for a set of credentials with a message and optionally pre-filled username. |
| logoff | Sign out of the current user. |

## Processes & Services

| Cmdlet | Description |
| --- | --- |
| Get-Process | Display a list of all running processes on the host system. |
| Stop-Process | Stop a specified running process. Get-Process can be used to obtain the process ID to stop. |
| Get-Service | Get a list of all services on the host machine, including ones that are not running. Similar to Get-Process. |

## Local Computer

| Cmdlet | Description |
| --- | --- |
| Rename-Computer | Set the name of the host computer. |
| Set-TimeZone | Set the time zone of the clock on a computer based on the full name of the time zone (id). |
| Get-EventLog | Gets the contents of the system event log with the specified filters or parameters. This is an alternative to using the Event Viewer. |
| Get-WMIObject | Gets a specified Windows Management Instrumentation class or information about available classes. This enables more through system configuration and management on Windows hosts, including remotely. |
| Get-CimClass | Get a specific CIM class or all matching classes. Can be combined with the Namespace parameter for narrowed results. |
| Get-CimInstance | Get a specific CIM instance or all matching instances of a CIM class. Can be combined with the Namespace parameter for narrowed results. |
| Install-WindowsFeature | Install a new Windows feature or role onto a target system. |
| Get-LocalUser | Get a user on the target system by name or a unique identifier. |
| Set-LocalUser | Set the properties of a local user such as their username or password. |

## File System

| Cmdlet | Description |
| --- | --- |
| Get-Content | Get the content of an object at a specified location, such as text in the middle of a file or a certain parameter in a list. |
| Get-ChildItem | Get the contents of the current directory or one specified in the parameters. This is commonly aliased as cd. |
| Out-File | Save a string from a variable or piping into a text file on disk for later use. |
| Set-ItemProperty | Set the property of an item such as a registry key or folder. |
| Import-CSV | Create a new object using the contents of a CSV string or text file (via piping or variables). |
| Export-CSV | Convert and save an object and its properties as a CSV text document, following the original structure of the object. |
| ConvertTo-CSV | Performs the same task as Export-CSV with the exception that the resulting data is given back as a string to be used by other cmdlets rather than saved as a file. |
| Import-CliXML | Create a new object using the contents of a CLI XML string or text file (via piping or variables). |
| Export-CliXML | Convert and save an object and its properties as a CLI XML text document, following the original structure of the object. |
| ConvertTo-HTML | Convert an object and its contents into an HTML document which can be viewed in a web browser. |

## Networking

| Cmdlet | Description |
| --- | --- |
| Get-NetAdapter | Get a list of all network adapters in the host system or the details of a specific adapter, such as its name and link speed. |
| New-NetIPAddress | Create a new networking configuration on a specified adapter with the specified setttings. |
| Get-NetIPAddress | Get a list of all available network interfaces on a host system. |
| Remove-NetIPAddress | Remove a previous network configuration from the specified network interface. |
| New-NetRoute | Create a new route in the routing table on an interface. |
| Remove-NetRoute | Remove a route from the routing table on an interface. |
| Set-DnsClientServerAddress | Set the DNS servers used on a network interface. |

## Active Directory

| Cmdlet | Description |
| --- | --- |
| Add-Computer | Join a target system to an Active Directory domain server. |
| Remove-Computer | Remove a computer from an Active Directory domain. |
| Install-ADDSForest | Install a new Active Directory Domain Forest onto the target system. |
| New-ADUser | Create a new Active Directory domain user with specified name, email, password, etc. |
| Enable-ADAccount | Enable an Active Directory user account and allow it to be logged into. |
| Disable-ADAccount | Disable an Active Directory user account and disable it from being logged into. |
| Unlock-ADAccount | Unlock an Active Directory user account to allow for logins. |
| Set-ADAccountPassword | Set the password for an Active Directory user account with a new password specified as a secure string. |
| Remove-ADAccount | Delete a user from an Active Directory domain. |
| Add-ADGroupMember | Add a user to an Active Directory group. |
| Get-ADGroupMember | Get the users that are part of a group in Active Directory. |
| Remove-ADGroupMember | Remove a user from an Active Directory group. |

## PowerShell Remoting

| Cmdlet | Description |
| --- | --- |
| Enable-PSRemoting | Enable the ability to use PowerShell remoting. This must be done on both the host and client. |
| New-PSSession | Create a new PowerShell Remoting session with a specified computer on a domain or workgroup. |
| Get-PSSession | Get the details on all PSRemoting open sessions. |
| Remove-PSSession | Close an active PSRemoting session. |
| Enter-PSSession | Enter an existing PSRemote session as an interactive terminal. |
| Invoke-Command | Execute a PowerShell command on a remote system using PSRemoting. |

## Scheduled Tasks

| Cmdlet | Description |
| --- | --- |
| New-ScheduledTaskAction | Create a new action for a task. This defines what the task will perform. |
| New-ScheduledTaskTrigger | Create a new trigger for a task. This defines what the conditions to run this task are. |
| New-ScheduledTaskPrincipal | Create an object that defines the user account and process priority that a task will run at. |
| New-ScheduledTaskSettingsSet | Define the general settings and behaviours for a task. |
| New-ScheduledTask | Create a new scheduled task using the objects created from the cmdlets above. |
| Register-ScheduledTask | Register a scheduled task for execution. |

## Samba Shares

| Cmdlet | Description |
| --- | --- |
| New-SmbShare | Create a new Samba share in Windows with a specified name and path, as well as optional default permissions. |
| New-PSDrive | Mount a network file share to a drive mapping. You must specify the provider ‘FIleSystem’ for file shares. |

## Printers

| Cmdlet | Description |
| --- | --- |
| Add-Printer | Add a new printer to the system with a specified name, driver and port. |
| Get-Printer | Get the details of a printer by its name or port. |
