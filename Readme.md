PowerShell Ed-Fi MyGet Installer Scripts
============

These scripts were made possible thanks to the Michael and Susan Dell Foundation.

Description
------------

These Powershell scripts install the public Ed-Fi binaries published on the MyGet feed.

**Note:** As of the latest update these scripts can install the ODS API, Docs,
AdminApp & SandboxAdmin in the following versions:

* v3.4.0
* v3.3.0
* v3.2.0
* v2.6.0

Binaries can be found here:

* Ed-Fi ODS/API: https://www.myget.org/feed/ed-fi/package/nuget/EdFi.Ods.WebApi.EFA
* AdminApp: https://www.myget.org/feed/ed-fi/package/nuget/EdFi.ODS.AdminApp.Web
* Sandbox Admin: https://www.myget.org/feed/ed-fi/package/nuget/EdFi.Ods.Admin.Web.EFA 
* Docs-Swagger: https://www.myget.org/F/ed-fi/api/v2/package/EdFi.Ods.SwaggerUI.EFA

Prerequisites
------------

We recommend that the following prerequisites are installed on the machine that
you are going to run the scripts on.

**NOTE:** If you do not have these prerequisites the scripts will install them
for you. This will require a restart.

1. MsSQL Server 2017 or higher. (If using for development you can use the
   Developer edition. If this will be a production environment please use
   appropriate licensing. These scripts were tested with versions 2017 and
   2019.) The scripts will install MsSQL Server Express 2019 if it doesn't find a
   preinstalled version.
2. IIS - Internet Information Services (The scripts will install and configure
   it.)
3. .Net Framework 4.8. (The scripts will install it but a restart will be
   required after install. This is why we recommend to be installed before
   hand.)

That is it =)

Setup Instructions
------------

1. Download the scripts in zip format \
   <img src="img/download.png" width="300" >
2. Unzip them to a known location like C:\temp\ed-fi \
   <img src="img/explorer1.png"  width="400">
3. Open PowerShell as an "Administrator" \
   <img src="img/powershell1.png" width="400">
4. Navigate to the path where you unziped the scripts \
   <img src="img/Powershell2.png" width="400">
5. Execute the following commands:

    ```PowerShell
    C:\temp\ed-fi\> .\BinaryInstall.ps1
    ```

   <img src="img/Powershell3.png" width="400"> \
   Then choose the environment you wish to install and install it. For the sake
   of this tutorial we will do "Production v3.4.0"

    ```PowerShell
    C:\temp\ed-fi\> Install-EdFiProductionV34
    ```

    You will see a screen like the one bellow: "Confirms Done" \
    <img src="img/PowershellDone.png" width="400">

Legal Information
------------

Copyright (c) 2019 Ed-Fi Alliance, LLC and contributors.

Licensed under the [Apache License, Version 2.0](LICENSE) (the "License").

Unless required by applicable law or agreed to in writing, software distributed
under the License is distributed on an "AS IS" BASIS, WITHOUT WARRANTIES OR
CONDITIONS OF ANY KIND, either express or implied. See the License for the
specific language governing permissions and limitations under the License.

See [NOTICES](NOTICES.md) for additional copyright and license notifications.
