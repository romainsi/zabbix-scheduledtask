================DiscoverScheduledTasks ================


This template use PowerShell Cmdlets to discover and manage Windows Tasks Scheduled. 

Default French translation.

Items : Task Last Result (Status for each tasks), Task Last Run Time, Task Next Run time

Discovery : All tasks Active or Running

Triggers : [HIGH] => Last Result of tasks FAILED



Install : 

- Import template,

- Install the Zabbix agent on your host,

- Copy DiscoverScheduledTasks.ps1 in your zabbix agent directory,

- In powershell script change $path variable for subsfolders,

- Add the following line to your Zabbix agent configuration file : 

EnableRemoteCommands=1

UnsafeUserParameters=1  

UserParameter=TaskSchedulerMonitoring[*],powershell -NoProfile -ExecutionPolicy Bypass -File "C:\Program Files\Zabbix Agent\DiscoverScheduledTasks.ps1" "$1" "$2"

Value mapping 'scheduledtask' is in french for error ID of tasks.

