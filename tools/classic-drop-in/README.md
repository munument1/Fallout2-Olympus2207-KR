# Olympus 2207 1.2a Korean drop-in build

The ZIP uses Extended sfall 4.2.6 and the Korean Text Engine v1.2.5 renderer. The patches here provide the source changes for both DLLs.

- [Extended sfall 4.2.6 source](https://github.com/FalloutTeamX/sfall-Extended/tree/283a7e4eeaac1d000a794eb9694336b5b4363a8d), GPL-3.0-or-later
- [Korean Text Engine v1.2.5 source](https://github.com/munument1/Fallout2-Korean-Text-Engine/tree/v1.2.5), MIT

Build both DLLs for x86. The public ZIP includes the corresponding license notices.

## Extended sfall

Check out the commit above and run these commands with MSBuild, the Windows SDK, and the June 2010 DirectX SDK installed. Set DXSDK_DIR to the DirectX SDK directory, including its trailing backslash.

    git apply sfall-extended-4.2.6-olympus.patch
    MSBuild sfall/ddraw.vcxproj /m /p:Configuration=Release /p:Platform=Win32 /p:PlatformToolset=v145 /p:WindowsTargetPlatformVersion=10.0.26100.0 /p:PostBuildEventUseInBuild=false

The built DLL is sfall/Release/ddraw.dll.

## Korean renderer

Check out v1.2.5, apply korean-engine-v1.2.5-olympus.patch, and build in an x86 Visual Studio developer prompt.

    cl /nologo /std:c++17 /EHsc /O2 /MT /LD /utf-8 src\font_standalone.cpp src\native_font_hooks.cpp src\native_appearance.cpp /link /Brepro /DEF:src\font_bridge.def /OUT:fallout2font.dll gdi32.lib user32.lib

Use the v1.2.5 fallout2font.ini and the three font assets with their licenses. The translation input is the published Olympus 2207 translation-data ZIP, SHA-256 2663af5bb72a0e5ee31e78b4c56f8594925cd3f9c3300dbd502287c7974f40ab. Include its game-facing translation files together with the two compiled DLLs, the font configuration, fonts, licenses, and readme. Keep Olympus's base game files, ddraw.ini and high-resolution patch out of the distributable.

Verified on the provided English Olympus 2207 1.2 plus 1.2a patch. The original olympus.exe and high-resolution patch remained in place. The Korean menu, first dialogue, hint prompt, and multiline tutorial-skip prompt displayed in-game.
