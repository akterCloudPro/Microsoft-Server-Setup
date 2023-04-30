### 1. Install the Remote Tools Administration Pack
Install-WindowsFeature RSAT-ADDS

### 2. Install .Net Framework 4.8
https://docs.microsoft.com/en-us/exchange/plan-and-deploy/prerequisites?view=exchserver-2019

### 3.Visual C++ Redistributable Package for Visual Studio 2013
https://support.microsoft.com/en-us/topic/update-for-visual-c-2013-redistributablepackage-d8ccd6a5-4e26-c290-517b-8da6cfdf4f10

### 4. Install URL Rewrite

### 5. Add the required Lync Server or Skype for Business Server components
a. Install-WindowsFeature Server-Media-Foundation
b. Install Unified Communications Managed API 4.0
https://www.microsoft.com/en-us/download/details.aspx?id=34992

### 6. install the required Windows components
Install-WindowsFeature Server-Media-Foundation, NET-Framework-45-Features,
RPC-over-HTTP-proxy, RSAT-Clustering, RSAT-Clustering-CmdInterface,
RSAT-Clustering-Mgmt, RSAT-Clustering-PowerShell, WAS-Process-Model, Web-Asp-Net45,
Web-Basic-Auth, Web-Client-Auth, Web-Digest-Auth, Web-Dir-Browsing,
Web-Dyn-Compression, Web-Http-Errors, Web-Http-Logging, Web-Http-Redirect,
Web-Http-Tracing, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Lgcy-Mgmt-Console,
Web-Metabase, Web-Mgmt-Console, Web-Mgmt-Service, Web-Net-Ext45,
Web-Request-Monitor, Web-Server, Web-Stat-Compression, Web-Static-Content,
Web-Windows-Auth, Web-WMI, Windows-Identity-Foundation, RSAT-ADDS

### 7. Download and mount ISO
https://www.microsoft.com/en-us/download/details.aspx?id=103477

### 8. Active Directory commands
Extend the Active Directory schema
- .\Setup.exe /PrepareSchema /IAcceptExchangeServerLicenseTerms_DiagnosticDataON
(This parameter enables sending data to Microsoft.)
- .\Setup.exe /IAcceptExchangeServerLicenseTerms_DiagnosticDataON /PrepareAD /OrganizationName: “ClickForBaby”
- .\Setup.exe /IAcceptExchangeServerLicenseTerms_DiagnosticDataON /PrepareAllDomains
