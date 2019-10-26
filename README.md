# Sample Versioning Dotnet

This is a sample dotnet core project for config version to dll file

## Install

### dotnet versioninfo

```sh
dotnet tool install --global dotnet-versioninfo --version 1.0.2
```

### check version

```sh
versioninfo --version
```

## clone project

```sh
git clone https://github.com/chaiwatmat/sample-versioning-dotnet

cd sample-versioning-dotnet
```

## build & bump version

### build

```sh
dotnet build
```

### check current dll version

```sh
versioninfo
```

### result will look like

```sh
/Users/chaiwatmat/projects/github/sample-versioning-dotnet/mvc/obj/Debug/netcoreapp3.0/mvc.Views.dll
        FileVersionInfo.FileVersion:    1.0.0.0
        FileVersionInfo.ProductVersion: 1.0.0.0
/Users/chaiwatmat/projects/github/sample-versioning-dotnet/mvc/obj/Debug/netcoreapp3.0/mvc.dll
        FileVersionInfo.FileVersion:    1.0.0.0
        FileVersionInfo.ProductVersion: 1.0.0.0
/Users/chaiwatmat/projects/github/sample-versioning-dotnet/mvc/bin/Debug/netcoreapp3.0/mvc.Views.dll
        FileVersionInfo.FileVersion:    1.0.0.0
        FileVersionInfo.ProductVersion: 1.0.0.0
/Users/chaiwatmat/projects/github/sample-versioning-dotnet/mvc/bin/Debug/netcoreapp3.0/mvc.dll
        FileVersionInfo.FileVersion:    1.0.0.0
        FileVersionInfo.ProductVersion: 1.0.0.0
```

### build with new version

```sh
export assemblyVersion=1.1.0.0
dotnet build /p:Version=$assemblyVersion /p:AssemblyVersion=$assemblyVersion
```

### your version will change to

```sh
/Users/chaiwatmat/projects/github/sample-versioning-dotnet/mvc/obj/Debug/netcoreapp3.0/mvc.Views.dll
        FileVersionInfo.FileVersion:    1.1.0.0
        FileVersionInfo.ProductVersion: 1.1.0.0
/Users/chaiwatmat/projects/github/sample-versioning-dotnet/mvc/obj/Debug/netcoreapp3.0/mvc.dll
        FileVersionInfo.FileVersion:    1.1.0.0
        FileVersionInfo.ProductVersion: 1.1.0.0
/Users/chaiwatmat/projects/github/sample-versioning-dotnet/mvc/bin/Debug/netcoreapp3.0/mvc.Views.dll
        FileVersionInfo.FileVersion:    1.1.0.0
        FileVersionInfo.ProductVersion: 1.1.0.0
/Users/chaiwatmat/projects/github/sample-versioning-dotnet/mvc/bin/Debug/netcoreapp3.0/mvc.dll
        FileVersionInfo.FileVersion:    1.1.0.0
        FileVersionInfo.ProductVersion: 1.1.0.0
```
