# Terminal North

**Terminal North** is a Windows diagnostic, monitoring, troubleshooting,
and system-repair toolkit built around a terminal-style interface.

> **Why I made this project**
>
> Terminal North originally started as a private `.exe` that I used for
> my own PC analysis, diagnostics, troubleshooting, and Windows system
> repairs. I later decided to make the project available online so other
> users and technicians can use it too.
>
> Terminal North performs legitimate Windows administration and
> diagnostic tasks. Some features require Administrator privileges
> because Windows itself restricts access to system repair, security,
> networking, services, restore points, and other protected components.
> The purpose of this README is to document what the program does so
> users can review its functionality before using it.

## Important Notice

Terminal North is **not designed to hide what it does**. Its functions
are based primarily on Windows commands, PowerShell, WMI/CIM, and
built-in Microsoft administration utilities.

Because the compiled version can request Administrator privileges and
execute PowerShell/system commands, security software may inspect it
more aggressively than an ordinary desktop application. Users should
only download releases from the project's official distribution location
and are encouraged to review the scripts/source when available.

Some repair or cleanup commands can modify Windows. Terminal North asks
for confirmation before important repair/cleanup operations, but you
should still understand a command before running it. Back up important
data before performing system repairs.

## Requirements

-   Windows 10 or Windows 11
-   64-bit Windows recommended
-   Windows PowerShell
-   Administrator privileges for protected system operations
-   Internet connection for features that query online services
-   Ookla Speedtest CLI for the Internet Speed Test module, when that
    feature is used

------------------------------------------------------------------------

# Main Menu

## \[1\] Terminal

Opens a terminal environment for command-line work.

## \[2\] System Information

Displays detailed information about the computer, including:

-   Computer and Windows information
-   Manufacturer and model
-   CPU
-   RAM
-   GPU
-   BIOS and motherboard
-   Physical disks and volumes
-   Network adapters
-   IP configuration
-   Battery information when available
-   Secure Boot
-   TPM
-   Microsoft Defender information
-   PowerShell/.NET environment
-   System uptime

## \[3\] Network Tools

Network troubleshooting submenu:

1.  **Ping** --- Test connectivity to a host.
2.  **Traceroute** --- Display the network path to a destination.
3.  **DNS Lookup** --- Resolve DNS names and addresses.
4.  **IP Configuration** --- Display Windows IP configuration.
5.  **Active Connections** --- Display current network connections.
6.  **Network Adapters** --- Display installed network adapters.
7.  **Gateway Test** --- Test connectivity to the default gateway.
8.  **Flush DNS Cache** --- Clear the Windows DNS resolver cache.
9.  **Back**

## \[4\] Performance Monitor

Displays live system performance information, including CPU, memory,
disk, network activity, processes, and available GPU information.

## \[5\] Disk Manager

Storage and disk diagnostic submenu:

1.  **Disk Dashboard** --- Overview of volumes, free space, physical
    disks, media type, and health.
2.  **Partitions and Volumes** --- Display partitions, drive letters,
    file systems, and sizes.
3.  **Physical Disk Information** --- Model, serial information, bus
    type, media type, firmware, and capacity.
4.  **SMART / Reliability Health** --- Display reliability information
    exposed by Windows and supported hardware.
5.  **Storage Performance** --- Current disk activity, reads, writes,
    and queue information.
6.  **Largest Files - User Profile** --- Locate large files inside the
    current Windows user profile.
7.  **Open Windows Disk Management** --- Launch `diskmgmt.msc`.
8.  **Open Optimize Drives** --- Launch the Windows drive optimization
    utility.
9.  **Export Storage Report** --- Generate a storage report.
10. **Back**

## \[6\] Process Manager

1.  **Active Processes** --- Name, PID, memory, and CPU information.
2.  **Top RAM Processes**
3.  **Top CPU Processes**
4.  **Search Process** --- Search by process name or PID.
5.  **Terminate Process** --- Terminate a process by PID after
    confirmation.
6.  **Process Details** --- Display detailed process information.
7.  **Live Process Monitor**
8.  **Open Windows Task Manager**
9.  **Export Process Report**
10. **Back**

> Terminating a process can cause unsaved work to be lost.

## \[7\] Windows Tools

Quick launcher for built-in Windows administration utilities:

1.  Task Manager
2.  Services
3.  Registry Editor
4.  Device Manager
5.  Event Viewer
6.  Disk Management
7.  Windows Update
8.  Computer Management
9.  System Information
10. System Configuration
11. Resource Monitor
12. Performance Monitor
13. Windows Security
14. Windows Defender Firewall with Advanced Security
15. Programs and Features
16. Startup Folder
17. Advanced System Properties / Environment Variables
18. Windows Memory Diagnostic
19. DirectX Diagnostic Tool
20. Power Options
21. Back

## \[8\] Network Information

1.  Complete Network Overview
2.  Network Adapters
3.  IP Addresses
4.  Gateway Information
5.  DNS Information
6.  MAC Addresses
7.  Ethernet / Wi-Fi Link Speed
8.  Wi-Fi Details
9.  DHCP Information
10. Routing Table
11. Public IP
12. Live Network Traffic
13. Export Network Report
14. Back

## \[9\] Wi-Fi Information

1.  Current Wi-Fi Connection
2.  Wi-Fi Interface
3.  Current SSID / Access Point
4.  Signal Strength
5.  Channel / Radio Information
6.  Receive / Transmit Speed
7.  Saved Wi-Fi Profiles
8.  Wi-Fi Driver Information
9.  Nearby Wi-Fi Networks
10. Live Wi-Fi Monitor
11. Wi-Fi Adapter Statistics
12. Export Wi-Fi Report
13. Back

Saved Wi-Fi profile passwords are not intended to be displayed by this
module.

## \[10\] Hardware Monitor

1.  Hardware Overview
2.  CPU Information
3.  GPU Information
4.  Memory Information
5.  Temperature Sensors
6.  Fan / Sensor Information
7.  Motherboard / BIOS
8.  Battery / Power
9.  Live CPU / RAM Monitor
10. Export Hardware Report
11. Back

Sensor availability depends on what Windows, the motherboard, firmware,
and drivers expose. Terminal North does not invent unavailable
temperature or fan readings.

## \[11\] Startup Manager

1.  View Startup Programs
2.  Detailed Startup Information
3.  Current User Startup Registry
4.  All Users Startup Registry
5.  Open User Startup Folder
6.  Open All Users Startup Folder
7.  Open Windows Startup Apps
8.  Open Task Manager
9.  Export Startup Report
10. Back

## \[12\] Services Manager

Displays Windows services, their current state, display name, and
startup mode.

## \[13\] Driver Information

Displays signed Plug and Play driver information, including available
device names, manufacturers, driver versions, providers, dates, and INF
information.

## \[14\] Windows Security

Displays available information about:

-   Microsoft Defender
-   Real-time protection
-   Firewall profiles
-   Secure Boot
-   TPM

## \[15\] System Integrity

Provides explicit choices before executing Windows integrity commands:

-   `sfc /scannow`
-   `DISM /Online /Cleanup-Image /ScanHealth`
-   `DISM /Online /Cleanup-Image /RestoreHealth`
-   `chkdsk C: /scan`

No repair option should be selected without understanding its purpose.

## \[16\] Storage Cleaner

Analyzes accessible temporary files in Windows temporary locations,
estimates their size, and asks for confirmation before attempting
cleanup.

Files currently in use may be skipped.

## \[17\] Internet Test

Tests:

-   Connectivity
-   Ping latency
-   Packet loss information reported by `ping`
-   DNS resolution
-   DNS query response time

## \[18\] Port Viewer

Displays local TCP and UDP endpoints and active TCP connections,
including available local/remote addresses, ports, state, and owning
process IDs.

## \[19\] Event Logs

Displays recent Windows System log errors, warnings, and critical
events.

## \[20\] Battery Information

Displays available Windows battery information such as:

-   Charge level
-   Battery status
-   Estimated runtime when available

Can also generate the Windows `powercfg /batteryreport` HTML report
after confirmation.

## \[21\] Installed Software

Displays installed software information discovered from Windows
uninstall registry locations and Microsoft Store/Appx package
information for the current user.

The exact list can differ from the Apps page in Windows because Windows
exposes software through multiple installation technologies.

## \[22\] Windows Update Info

Displays:

-   Windows product/version/build
-   Recent installed hotfixes and update information available through
    Windows

## \[23\] User Accounts

Displays local Windows users and local groups, including available
account state information.

## \[24\] Environment Variables

Displays Windows environment variables, including values such as:

-   `PATH`
-   `TEMP`
-   `USERPROFILE`
-   System/user environment variables

> Exported reports or screenshots may contain usernames, paths, computer
> names, IP addresses, or other environment-specific information. Review
> them before posting publicly.

## \[25\] Export PC Report

Generates a TXT report containing available information about:

-   Computer
-   CPU
-   GPU
-   Memory
-   Disks
-   Network
-   Services

Review a generated report before sharing it online because system
reports can contain device-specific information.

## \[26\] Quick Diagnostics

Runs a quick diagnostic overview covering:

-   Internet connectivity
-   Physical disk health status
-   Available RAM
-   Automatic services that are not currently running
-   Windows component-store health check using DISM

## \[27\] System Dashboard

Displays a one-page summary of the PC, including:

-   Manufacturer/model
-   Windows build
-   Uptime
-   CPU
-   GPU
-   RAM
-   System drive free space
-   Active network adapters

## \[28\] About

Displays Terminal North version/project information and changelog
information included in the application.

## \[29\] Network Scanner

Scans the local IPv4 network for reachable/local devices and displays
available information such as:

-   IP address
-   MAC address
-   Hostname
-   Neighbor state

For safety and performance, large networks may be limited to the local
`/24` range used by the tool.

Manufacturer/vendor identification is only displayed when the required
vendor information is available. The tool should not fabricate vendor
names.

## \[30\] Hardware Stress Test

Runs a **controlled diagnostic CPU/RAM load**, not an extreme
overclocking benchmark.

Features include:

-   User-selected duration
-   Limited duration range
-   CPU activity
-   Temporary memory allocation
-   Live CPU/RAM information
-   Manual stop with `Q`
-   Cleanup of test resources after the test

Monitor system temperatures and stability while using stress-related
features.

## \[31\] BSOD / Crash Analyzer

Checks for recent Windows crash information, including:

-   BugCheck-related System events
-   Minidump files in the Windows Minidump directory
-   `MEMORY.DMP` when present
-   Dump file date, size, and location

This module identifies available crash evidence; it does not
automatically prove the root cause of a BSOD.

## \[32\] Windows Repair Center

Central repair menu containing:

1.  `SFC /scannow`
2.  `DISM /Online /Cleanup-Image /CheckHealth`
3.  `DISM /Online /Cleanup-Image /ScanHealth`
4.  `DISM /Online /Cleanup-Image /RestoreHealth`
5.  `ipconfig /flushdns`
6.  `netsh winsock reset`
7.  `netsh int ip reset`
8.  Windows Update download-cache/component reset actions
9.  Back

Repair operations require confirmation. Some operations can require a
Windows restart afterward.

## \[33\] Device Diagnostics

Looks for Windows Plug and Play devices reporting a non-zero
Configuration Manager error code and displays available:

-   Device name
-   Manufacturer
-   Device class
-   Error code
-   Device ID
-   Driver version
-   Driver provider
-   INF file

## \[34\] Internet Speed Test

Uses the **Ookla Speedtest CLI** when `speedtest.exe` is installed and
available in `PATH`.

Terminal North intentionally does not generate fake download/upload
speed estimates when the official CLI is unavailable.

## \[35\] System Restore

Displays available Windows restore points and can request creation of a
new restore point named:

`Terminal North Restore Point`

Creation requires confirmation and depends on Windows System
Protection/Restore being supported and enabled.

## \[36\] Windows License Information

Displays non-secret Windows licensing information such as:

-   Windows edition
-   Version/build
-   Activation status
-   License description/channel
-   Only the partial product-key suffix exposed by Windows

Terminal North does not intentionally display the complete Windows
product key in this module.

## \[37\] PC Health Score

Provides a diagnostic status table using visible checks rather than an
arbitrary benchmark number.

Checks can include:

-   System drive free space
-   Physical disk health reported by Windows
-   Available RAM
-   Internet connectivity
-   Microsoft Defender real-time protection
-   Automatic services not running
-   Recent Windows hotfix information

Results use statuses such as:

-   **OK**
-   **WARNING**
-   **PROBLEM**

This is a diagnostic summary, not a guarantee that the computer has no
hardware or software problems.

## \[0\] Exit

Closes Terminal North.

------------------------------------------------------------------------

# Administrative Privileges

The compiled Terminal North executable may request Administrator
privileges because several Windows operations require elevation.

Examples include:

-   SFC
-   DISM repair operations
-   Network stack reset
-   Windows Update component maintenance
-   Some security information
-   Some hardware/system information
-   System Restore
-   Protected services and system configuration

Administrator access is requested so these legitimate diagnostic/repair
features can work. It should not be interpreted by itself as evidence
that an application is malicious.

# Commands and Windows Components Used

Depending on the selected module, Terminal North can use
Windows/PowerShell components including:

``` text
ping
tracert
ipconfig
ipconfig /flushdns
nslookup / DNS resolution
netsh
netsh winsock reset
netsh int ip reset
sfc /scannow
DISM
chkdsk
powercfg
Get-CimInstance
Get-ComputerInfo
Get-PhysicalDisk
Get-Disk
Get-Volume
Get-Partition
Get-NetAdapter
Get-NetIPConfiguration
Get-NetTCPConnection
Get-NetUDPEndpoint
Get-NetNeighbor
Get-Service
Get-WinEvent
Get-HotFix
Get-LocalUser
Get-LocalGroup
Get-MpComputerStatus
Get-NetFirewallProfile
Get-Tpm
Confirm-SecureBootUEFI
Get-ComputerRestorePoint
Checkpoint-Computer
Get-AppxPackage
Resolve-DnsName
Test-Connection
```

Terminal North also launches standard Windows management tools where
appropriate.

# EXE Build

The project can be packaged into `TerminalNorth.exe` using PS2EXE.

The compiled launcher contains the Terminal North BAT and PowerShell
modules. At runtime, the packaged scripts can be extracted to a
temporary Terminal North working directory so the existing modules can
operate together. The launcher attempts to remove that temporary
directory when Terminal North closes.

The executable remains a Windows/PowerShell-based administration
toolkit; compiling it into an EXE does not change the purpose of the
underlying commands.

# Antivirus / SmartScreen Notice

A newly published, unsigned utility that:

-   is packaged from PowerShell,
-   requests Administrator privileges,
-   performs system administration,
-   launches command-line tools,
-   and is not yet widely downloaded

may receive additional scrutiny from Microsoft Defender, SmartScreen, or
third-party security products.

Users should verify that they obtained Terminal North from the official
project/release location. If source code is published with the release,
users can inspect it before running the executable.

Do **not** disable antivirus protection merely to run Terminal North. If
a release is unexpectedly detected, verify the file/source and
investigate the detection rather than blindly bypassing security
controls.

# Privacy

Terminal North is primarily intended to analyze the local Windows
computer.

Some modules can display potentially sensitive local information, such
as:

-   Local usernames
-   Computer name
-   IP addresses
-   MAC addresses
-   Network configuration
-   Installed software
-   Running processes
-   Device information
-   File paths
-   Environment variables
-   System/event logs

Do not publish screenshots or exported reports without reviewing them
first.

The Internet Speed Test requires the external Ookla Speedtest CLI when
used. Features that explicitly retrieve public-IP or other online
information require network access.

# Safety

Before using repair features:

1.  Save your work.
2.  Back up important files.
3.  Read the selected operation.
4.  Create a restore point when appropriate.
5.  Do not interrupt Windows repair operations unnecessarily.
6.  Restart Windows when a repair command explicitly requires it.

Terminal North is a diagnostic/technician utility. It cannot guarantee
that a repair operation will solve a particular Windows problem.

# Project Structure

The current Terminal North build is based on a main BAT interface plus
PowerShell modules for specialized functionality, including:

``` text
Terminal_North_ADVANCED_37_OPTIONS.bat
Kali_RGB_System_Info.ps1
Terminal_North_AdvancedModules_V2.ps1
Terminal_North_DiskManager.ps1
Terminal_North_HardwareMonitor_STABLE_BACKFIX.ps1
Terminal_North_NetworkInformation.ps1
Terminal_North_PerformanceMonitor.ps1
Terminal_North_ProcessManager.ps1
Terminal_North_StartupManager_FIXED.ps1
Terminal_North_WiFiInformation_FIXED_V2.ps1
```

The packaged EXE can bundle these components into a single distributable
executable.

# Troubleshooting

### A module shows `N/A`

Windows may not expose that sensor or property through the API being
used. This is especially common with temperatures, fan speeds, battery
details, SMART/reliability data, and some GPU information.

### A repair command fails

Try running Terminal North as Administrator and read the Windows error
returned by the command. Some repairs also depend on Windows services
and the state of the component store.

### Speed Test says that Speedtest CLI is missing

Install the official Ookla Speedtest CLI and make sure `speedtest.exe`
is available through the Windows `PATH`.

### System Restore cannot create a restore point

Check whether System Protection is enabled for the Windows system drive
and whether Windows permits a new restore point at that time.

### Wi-Fi information is incomplete

The information returned by Windows can vary by Wi-Fi adapter, driver,
Windows language, and connection state.

### Some software is missing from Installed Software

Windows applications can be installed using different technologies. The
module combines common uninstall-registry entries and Appx information,
but no single Windows inventory method is guaranteed to represent every
application exactly like Windows Settings.

# Disclaimer

Terminal North is provided as a diagnostic and system-administration
utility.

Use it at your own risk. The author is not responsible for data loss,
configuration changes, downtime, or other damage caused by misuse,
interrupted repair operations, unsupported hardware, Windows bugs, or
commands executed without understanding their effect.

If you do not understand a repair option, do not run it until you know
what it changes.

------------------------------------------------------------------------

## Terminal North

**Windows Diagnostics • Hardware • Network • Storage • Security • Repair
• Monitoring**

Originally built as my personal Windows analysis and repair toolkit ---
now prepared for public use.
