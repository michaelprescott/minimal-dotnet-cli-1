# minimal-dotnet-cli-1

About
=====
Minimalistic .NET Core Project (Using only dotnet cli) - 1

Getting Started
---------------
1. Install .NET (dotnet cli)
    * for macOS - https://learn.microsoft.com/en-us/dotnet/core/install/macos
    * for Windows - https://learn.microsoft.com/en-us/dotnet/core/install/windows?tabs=net60
1a. Install .NET in Visual Studio Code
    * https://code.visualstudio.com/docs/languages/dotnet
    ** Just "Install the .NET Extension Pack" (We're assuming that you already have VSCode and you just installed dotnet CLI+SDK)
2. From the root of the project directory
    * Verify that you have successfully installed dotnet cli and it is accessible run `dotnet --version`
3. Create a minimal CLI application
    `dotnet new console -o ./src/Sample.Project`
    `cd ./src/Sample.Project`
    `dotnet run`
4. Create a minimal web API application
    * Starting from the root of this repo's directory, again.  If you are walking through steps above
        `cd ../../`
    * Create subproject for the Api
    `dotnet new webapi -o src/TodoApi`
    `cd src/TodoApi`
    `dotnet add package Microsoft.EntityFrameworkCore.InMemory`
Writing /var/folders/z9/gtkq0ch558j785shq0pyx40c0000gn/T/tmpAEq20p.tmp
info : X.509 certificate chain validation will use the fallback certificate bundle at '/usr/local/share/dotnet/sdk/6.0.402/trustedroots/codesignctl.pem'.
info : Adding PackageReference for package 'Microsoft.EntityFrameworkCore.InMemory' into project '/Users/michaelprescott/Projects/learn/minimal-dotnet-cli-1/src/TodoApi/TodoApi.csproj'.
info :   GET https://api.nuget.org/v3/registration5-gz-semver2/microsoft.entityframeworkcore.inmemory/index.json
info :   OK https://api.nuget.org/v3/registration5-gz-semver2/microsoft.entityframeworkcore.inmemory/index.json 111ms
info :   GET https://api.nuget.org/v3/registration5-gz-semver2/microsoft.entityframeworkcore.inmemory/page/0.0.1-alpha/3.1.3.json
info :   OK https://api.nuget.org/v3/registration5-gz-semver2/microsoft.entityframeworkcore.inmemory/page/0.0.1-alpha/3.1.3.json 109ms
info :   GET https://api.nuget.org/v3/registration5-gz-semver2/microsoft.entityframeworkcore.inmemory/page/3.1.4/6.0.0-rc.2.21480.5.json
info :   OK https://api.nuget.org/v3/registration5-gz-semver2/microsoft.entityframeworkcore.inmemory/page/3.1.4/6.0.0-rc.2.21480.5.json 126ms
info :   GET https://api.nuget.org/v3/registration5-gz-semver2/microsoft.entityframeworkcore.inmemory/page/6.0.0/7.0.0-rc.2.22472.11.json
info :   OK https://api.nuget.org/v3/registration5-gz-semver2/microsoft.entityframeworkcore.inmemory/page/6.0.0/7.0.0-rc.2.22472.11.json 108ms
error: Unable to load the service index for source https://pkgs.dev.azure.com/edmentum/_packaging/Ed/nuget/v3/index.json.
error:   Response status code does not indicate success: 401 (Unauthorized).

Usage: NuGet.CommandLine.XPlat.dll package add [options]

Options:
  -h|--help               Show help information
  --force-english-output  Forces the application to run using an invariant, English-based culture.
  --package               Id of the package to be added.
  --version               Version of the package to be added.
  -d|--dg-file            Path to the dependency graph file to be used to restore preview and compatibility check.
  -p|--project            Path to the project file.
  -f|--framework          Frameworks for which the package reference should be added.
  -n|--no-restore         Do not perform restore preview and compatibility check. The added package reference will be unconditional.
  -s|--source             Specifies NuGet package sources to use during the restore.
  --package-directory     Directory to restore packages in.
  --interactive           Allow the command to block and require manual action for operations like authentication.
  --prerelease            Allows prerelease packages to be installed.

  * Insure you have installed the `code` CLI
  * macOS - https://code.visualstudio.com/docs/setup/mac
  * Windows - https://code.visualstudio.com/docs/setup/windows
    `code --version`
    `code -r ../TodoApi` ## This is going to open the subproject folder, src/TodoApi, in VSCode.
  * Trust development certificate
    `dotnet dev-certs https --trust`

Trusting the HTTPS development certificate was requested. If the certificate is not already trusted we will run the following command:
'sudo security add-trusted-cert -d -r trustRoot -k /Library/Keychains/System.keychain <<certificate>>'
This command might prompt you for your password to install the certificate on the system keychain.

A valid HTTPS certificate is already present.

  * Press Ctrl+F5