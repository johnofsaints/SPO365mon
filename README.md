# SPO365mon
Monitoring Health of O365 SharePoint  

Windows Powershell command to monitor SharePoint Server Health: 
>Get-PnPHealthScore -Url https://contoso.sharepoint.com

Retrieves the current health score value of the server which is a value between 0 and 10. Lower is better.

How to run PowerShell from linux:
>https://docs.microsoft.com/en-us/powershell/scripting/install/installing-powershell-core-on-linux?view=powershell-6

Get Splunk linux install package: 
>https://docs.splunk.com/Documentation/SplunkLight/7.2.5/Installation/InstallonLinux

Crontab every minute:
>* * * * * /opt/splunk/bin/scripts/sphealth.sh >> /opt/splunk/bin/scripts/sphealth.log 2>&1

Splunk spl:
>index="sharepointhealth"|timechart span=1m avg(HealthScore)

>index="sharepointhealth"|timechart max(HealthScore)

>index="sharepointhealth"|timechart max(HealthScore) span=1h


Reference:
>https://docs.microsoft.com/en-us/powershell/module/sharepoint-pnp/get-pnphealthscore?view=sharepoint-ps
