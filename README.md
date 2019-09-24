# STM32CubeIDE-TouchGFX-Fix
Patches project files generated by CubeMX for STM32CubeIDE to work with TouchGFX

## Background

When generating TouchGFX projects using CubeMX and the STM32CubeIDE application, it will clobber a bunch of settings in the project XML that require you to configure each time. Super annoying, and since ST/TouchGFX team can't get around to fixing this in a timely manner this patch was created.

## Usage
It's a .NET Core application which you can run from the command line (Windows 10). After running the utility, you should be able to refresh your project (Right-click your project, choose Refresh) and build afterwards.

### Run a pre-built release

Download the [latest release](https://github.com/replaysMike/STM32CubeIDE-TouchGFX-Fix/releases), and run as follows:

```ps
STM32CubeIDE-TouchGFX-Fix -p C:\MyTouchGFXProjectLocation
```

or

### Build from source

```ps
dotnet build
dotnet publish -c Release -r win10-x64
```

or optionally build it / run in Visual Studio.

### Notes

It will patch the .cproject XML file to set the appropriate includes/source values required for building with TouchGFX.
