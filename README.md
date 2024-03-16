﻿# Florine's Fallout 4 VR
_Last updated: 2024-03-16_

> A thorough, beginner-friendly guide for a stable, vanilla-ish experience.

**Motivation**  
Fallout 4 VR sucks quite badly for modern VR standards.
Gameplay is lackluster; graphics, lighting, and performance are bad; and there's plenty of VR-only bugs in addition to
the bugs in vanilla.
As is typical with Bethesda games, you can fix most of that with a whole lot of mods.
The modding scene for FO4VR has evolved a lot over time, and as a result not all tips and tricks you read online are
still accurate.

This guide aims to be comprehensive and beginner-friendly.
You can choose to follow it in its entirety, or pick and choose parts for your own list.

**Goals**  
I describe what I did to get a **stable, enjoyable, reasonable-looking** game.
Other resources, like
[GingasVR's excellent overhaul](https://docs.google.com/document/d/1KjAhJ3RAqUxp5TYivW7fjSC_XVEuAafiJmHfCVnb2VI/), are
good, but too non-vanilla for my tastes.
Meanwhile, my list only deviates from vanilla when I think there's a very good reason, like replacing VATS with bullet
time because the former just isn't nice in VR.


**Performance**  
I didn't really focus on performance because I have a powerful PC.
However, I mostly avoided mods that negatively affect performance.

---

**Table of contents**  
<a name="toc"></a>[**How to read this guide**](#how-to-read) | [**Setup**](#setup) | [**Configuration**](#configuration) | [**List of mods**](#list-of-mods) | [**Finishing up**](#finishing-up)

---


# 1 How to read this guide<a name="how-to-read"></a> <small><sup>[top ▲](#toc)</sup></small>
> [!TIP]
> Read this guide carefully.

This section deals with the basics:
Why FO4VR modding is difficult, how this guide deals with version numbers, and common abbreviations.

## 1.1 About modding Fallout 4 VR<a name="about-modding-fo4vr"></a> <small><sup>[top ▲](#toc)</sup></small>
(**TODO: Lower your expectations, instabilities, difficulties, etc.**)

## 1.2 About version numbers<a name="about-version-numbers"></a> <small><sup>[top ▲](#toc)</sup></small>
Whenever I mention a tool or a mod, I will write down which version and variant I used.
For example, I might write "F4SEVR (v0.6.20)" to mean that I downloaded version 0.6.20 of
[F4SEVR](https://f4se.silverlock.org/).

If the version I wrote down is still the latest version when you're reading this, then just use that version.
If a newer version exists, and I don't explicitly mention you should download the version I mention, then you'll have to
judge for yourself whether it's more likely the update will _fix_ bugs or will _add_ bugs.

## 1.3 About tags<a name="about-tags"></a> <small><sup>[top ▲](#toc)</sup></small>
Some choices I make are more vanilla than others, and some choices make sense for people who already played Fallout 4,
but make no sense for first-time Fallout 4 players.
Therefore, I will tag tools and mods to let you know what to expect.
Here is a list of tags.

|                |                                                                    |
|----------------|--------------------------------------------------------------------|
| ![required]    | Necessary to make the game worth it in VR. Install this.           |
| ![recommended] | Good for all players. Install this, unless you seriously disagree. |
| ![optional]    | Good, but personal preference. Install if you want.                |

## 1.4 Abbreviations<a name="abbreviations"></a> <small><sup>[top ▲](#toc)</sup></small>
| Abbreviation      | Meaning                              | Example                                   |
|-------------------|--------------------------------------|-------------------------------------------|
| **FO4VR**         | Fallout 4 VR                         |                                           |
| **FO4AU**         | Fallout 4: Automatron  (the 1st DLC) |                                           |
| **FO4FH**         | Fallout 4: Far Harbor (the 3rd DLC)  |                                           |
| **FO4NW**         | Fallout 4: Nuka-World  (the 6th DLC) |                                           |
| **MO2**           | Mod Organizer 2                      |                                           |
| **`[fo4_dir]`**   | Where you installed non-VR FO4       | `C:\Steam\steamapps\common\Fallout 4\`    |
| **`[fo4vr_dir]`** | Where you installed FO4VR            | `C:\Steam\steamapps\common\Fallout 4 VR\` |
| **`[username]`**  | Your Windows username                | `florine`                                 |


# 2 Setup<a name="setup"></a> <small><sup>[top ▲](#toc)</sup></small>
Before you can start modding FO4VR, you need to make sure you have a clean install and have the right software
installed.

## 2.1 Removing old files<a name="removing-old-files"></a> <small><sup>[top ▲](#toc)</sup></small>
> [!TIP]
> If you haven't installed FO4VR yet, check the [software requirements](#software-requirements) to learn the correct
> installation directory.

> [!NOTE]
> If you have never installed FO4VR on your computer before, you can skip this section.

If you previously used other mods for FO4VR, make sure those are removed.
If you used MO2, make you use a clean MO2 profile, preferably by creating a new profile.
If you previously installed mods without a mod manager, make _extra_ sure you completely remove all mods.

You can remove old files as follows.
1. Delete the `C:\Users\[username]\AppData\Local\Fallout4VR\` directory in its entirety.
   This contains old configuration files.
2. The following apply only if you have already installed FO4VR:
   1. Delete the entire `[fo4vr_dir]` directory, but

      1. **not** `[fo4vr_dir]\Data\Video\`, and
      2. **not** files in `[fo4vr_dir]\Data\` that start with `Fallout4`.

      If you cannot find `[fo4vr_dir]`, check the [abbreviations](#abbreviations).
   2. In Steam, verify the integrity of FO4VR's game files.
      ([Check Steam's help pages to learn how.](https://help.steampowered.com/en/faqs/view/0C48-FCBD-DA71-93EB))

## 2.2 Software requirements<a name="software-requirements"></a> <small><sup>[top ▲](#toc)</sup></small>
> [!WARNING]
> You should install FO4VR into the right directory.
> Read this section carefully!

* **Windows 11** (v23H2) <sub>![required]</sub>  
  I use Linux for everything, including gaming, but for VR gaming it's just not a good choice as of 2024.
* **SteamVR** (v2.4.3) <sub>![required]</sub>
* **Fallout 4 VR** (v1.2.72.0.1) <sub>![required]</sub>
  * Do **not** install FO4VR in or below `C:\Program Files (x86)\`.
    Doing so may result in specific mods/tools unexpectedly failing, because Windows doesn't like it when software
    changes things in `Program Files (x86)`.
  * If you're fine with not putting FO4VR on your `C:\` drive,
    [install FO4VR on another drive as explained in Steam's help pages](https://help.steampowered.com/en/faqs/view/4BD4-4528-6B2E-8327).
    For performance reasons, you should prefer installing on an SSD.
  * If you don't want to or cannot put FO4VR on another drive,
    [move your entire Steam installation to another directory as explain in Steam's help pages](https://help.steampowered.com/en/faqs/view/4BD4-4528-6B2E-8327).
    Personally, I went for `C:\Users\[username]\Steam\`.
  * No, there is no simpler way. Yes, this is required.
* **Fallout 4 with all DLC** (v1.10.163) <sub>![recommended]</sub>  
  [More information below.](#using-dlc-in-fo4vr)
* **[Mod Organizer 2](https://www.modorganizer.org/)** (v2.5.0) <sub>![required]</sub>
  * Use the `.exe` installer.
  * For performance reasons, you should prefer installing on an SSD.
  * Install MO2 in a place where you don't need admin rights to access it.
    For example, install it somewhere in your home directory.
    Personally, I went for `C:\Users\[username]\MO2\`.
  * (**TODO: Explain instances.**)
* **[Visual C++ Redistributable](https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist)** ([direct link](https://aka.ms/vs/17/release/vc_redist.x64.exe)) <sub>![required]</sub>
* **[7-Zip](https://7-zip.org/)** <sub>![required]</sub>

## 2.3 Using DLC in FO4VR<a name="using-dlc-in-fo4vr"></a> <small><sup>[top ▲](#toc)</sup></small>
FO4VR does not include the DLC, which sucks.
Luckily, if you have non-VR FO4, you can just copy the DLC files into your FO4VR installation and then install a few
patches (included in the [mod list](#list-of-mods)).
If you don't have non-VR FO4 with DLC, and don't want to buy it, you can safely skip the steps that require DLC.

To copy non-VR FO4's DLC into FO4VR,
1. go to the `[fo4_dir]\Data\` directory,
2. select all files that start with `DLC`, except those that start with `DLCUltraHighResolution`, and
3. copy those files to `[fo4vr_dir]\Data\`.


# 3 Configuration<a name="configuration"></a> <small><sup>[top ▲](#toc)</sup></small>
You should now have the required software.
Before you install mods, there's some settings to tweak.
These settings relate to stability, visual quality, and performance.

> [!NOTE]
> Even if you skip these steps, at least launch the game once.
> This will set up important files and registry entries.

## 3.1 Basic settings<a name="basic-settings"></a> <small><sup>[top ▲](#toc)</sup></small>
1. Steam > Fallout 4 VR > Settings > General > Uncheck "Enable the Steam Overlay while in-game" (If you cannot disable, you disabled it globally. That's fine too.)
2. `[fo4vr_dir]\Fallout4VR.exe` > Properties > Compatibility > Check "Disable full-screen optimisations"
3. While in-game in VR:
   1. Settings > VR Performance:
       1. Anti-Aliasing: TAA
       2. Anisotropic Filtering: 16
       3. Character Lighting: Off
4. MO2: (**TODO: ???**)

## 3.2 INI configuration<a name="ini-configuration"></a> <small><sup>[top ▲](#toc)</sup></small>
INI files contain extra game settings that are not found in the game's menus.

To edit these settings,
1. shut down FO4VR if it's running,
2. open MO2,
3. in the main toolbar, click `Tools` (the icon has puzzle pieces),
4. click `INI Editor`, and
5. select the tab `fallout4custom.ini`.

### 3.2.1 How does an INI file work?
Take a look at the tab `fallout4.ini` to get a feel of what an INI looks like.

INI files obey the following rules.
* An INI file is divided into sections, indicated by square brackets.
  For example, the line `[Display]` starts a section with display settings.
  A section ends when a new section starts.
* After starting a section you can set variables, one on each line.
  A variable has a name and a value, separated by an equals sign.
  For example, `fItemRotationSpeed=0.4` changes the variable `fItemRotationSpeed` to have value `0.4`.
* The names of sections and variables are important.
  You cannot choose your own names.
* Variables should be in the correct section.
  Putting a variable in the wrong section has no effect.
* If you have multiple lines setting the same variable, only the first assignment is used.
* You cannot split up a section.
  If you start section `[Display]`, then start section `[VR]`, and then again start section `[Display]`, the settings in
  the second `[Display]` section are ignored.

### 3.2.2 Settings you should add
> [!IMPORTANT]
> The following changes should go into `fallout4custom.ini`.

> [!IMPORTANT]
> Make sure each section/variable occurs at most once.

**Default MO2 settings** <sub>![required]</sub>
```ini
[General]
sLocalSavePath=__MO_Saves\
bUseMyGamesDirectory=1
```

**Ensure mods load correctly** <sub>![required]</sub>
```ini
[Archive]
sResourceDataDirsFinal=
bInvalidateOlderFiles=1
sResourceStartUpArchiveList=Fallout4 - Startup.ba2, Fallout4 - Shaders.ba2, Fallout4 - Interface.ba2, Fallout4_VR - Shaders.ba2
sResourceIndexFileList=Fallout4 - Textures1.ba2, Fallout4 - Textures2.ba2, Fallout4 - Textures3.ba2, Fallout4 - Textures4.ba2, Fallout4 - Textures5.ba2, Fallout4 - Textures6.ba2, Fallout4 - Textures7.ba2, Fallout4 - Textures8.ba2, Fallout4 - Textures9.ba2, Fallout4_VR - Main.ba2, Fallout4_VR - Textures.ba2
```

**Disable in-game supersampling** <sub>![required]</sub>  
To enable supersampling, use the SteamVR settings.
```ini
[VRDisplay]
fRenderTargetSizeMultiplier=1.0
```

**Improve TAA performance/quality trade-off** <sub>![recommended]</sub>  
Most other FO4VR guides recommend these same values.
```ini
[Display]
fTAAPostSharpen=0.675
fTAASharpen=1.0000
fTAAHighFreq=0.8000
fTAALowFreq=0.5000
fTAAPostOverlay=0.675
```

**Increase Pip-Boy rendering quality** <sub>![recommended]</sub>
```ini
[Display]
uPipboyTargetHeight=1400
uPipboyTargetWidth=1752
```

**Allow sprinting regardless of head orientation** <sub>![recommended]</sub>
```ini
[Controls]
fSprintStopDirectionThresholdDegrees=360.0000
```

**Increase item rotation speed in workshop mode** <sub>![recommended]</sub>
```ini
[Workshop]
fItemRotationSpeed=0.4
```

**Make swimming slightly easier** <sub>![recommended]</sub>
```ini
[VR]
fSwimSpeedScalar=1.2500
fVrSwimDragCoefficient=0.0500
fVrSwimHMDFloatThreshold=0.7200
bVrSwimDeliberateResurface=1
```

**Set move direction relative to headset instead of controller** <sub>![optional]</sub>
```ini
[VRInput]
bUseWandDirectionalMovement=0
```

### 3.2.3 Additional settings
Above are the settings that I used.
There's many more settings you can tweak.
Here's a bunch of other resources that may be useful for you.

* <sub>![reddit]</sub> [INI Tweak Megathread](https://www.reddit.com/r/fo4vr/comments/7kenxb/)
* <sub>![reddit]</sub> [Comprehensive modding and tweaking guide for Fallout 4 VR](https://www.reddit.com/r/fo4vr/comments/d55jzy/)



# 4 List of mods<a name="list-of-mods"></a> <small><sup>[top ▲](#toc)</sup></small>
> [!NOTE]
> Make sure you know [what the abbreviations mean](#abbreviations) and understand
> [the relevance of version numbers](#about-version-numbers).

* **TODO: About load order** 

## 4.1 External libraries<a name="external-libraries"></a> <small><sup>[top ▲](#toc)</sup></small>
First of all, here's a few required mods/tools.
These are essentially toolkits that directly alter the game engine, and are required by many other mods.

> [!IMPORTANT]
> These mods should be installed manually.
> They should not be installed with MO2.

> [!IMPORTANT]
> These mods should be installed into `[fo4vr_dir]`, _not_ into `[fo4vr_dir]\Data\`.

1. **[F4SEVR](https://f4se.silverlock.org/)** (v0.6.20) <sub>![required]</sub>  
   This is a framework that allows modders to write custom scripts. Many other mods require this.
   * **Installation instructions:**
     1. Go to [the F4SE website](https://f4se.silverlock.org/), find the "Fallout 4 VR runtime", and click "7z archive".
     2. Use [7-Zip](https://7-zip.org/) to extract the downloaded file into `[fo4vr_dir]`.
     3. If you did this correctly, you should have the file `f4sevr_1_2_72.dll` in the same directory as
        `Fallout4VR.exe`.
        If this is not the case, you probably created the directory `[fo4vr_dir]\f4sevr_0_6_20\`, and you should copy
        the contents of that directory into `[fo4vr_dir]`.
2. **[fo4vr_improvements](https://github.com/fholger/f4ovr_improvements)** (vcas_v2) <sub>![required]</sub>  
   Improves some filters and shaders specifically for VR, and fixes issues the game has with Valve Index controllers.
   (If you don't use Index, this won't hurt either.)
   * **Installation instructions:**
     1. Go to [the mod's releases page](https://github.com/fholger/f4ovr_improvements/releases), and download the file
        `fo4vr_contrast_adaptive_sharpening_v2.7z`.
     2. Use 7-Zip to extract the downloaded file into `[fo4vr_dir]`.
        When prompted, choose to overwrite existing files.
     3. If you did this correctly, you should have the file `fo4_openvr.cfg` in the same directory as `Fallout4VR.exe`.
   * **Note:**
     If you verify the integrity of your game files in Steam, Steam will (partially) overwrite this mod, and you will
     have to re-install this mod.
3. **[vrperfkit](https://github.com/fholger/vrperfkit)** (v0.3) <sub>![required]</sub>  
   Enables upscaling and foveated rendering, which improves performance by a lot.
   * **Installation instructions:**
     1. Go to [the mod's releases page](https://github.com/fholger/vrperfkit/releases), and download the file
        `vrperfkit_v0.3.zip`.
     2. Extract the downloaded file into `[fo4vr_dir]`.
        When prompted, choose to overwrite existing files.
     3. If you did this correctly, you should have the file `vrperfkit.yml` in the same directory as `Fallout4VR.exe`.
     4. After installing, find the file `vrperfkit.yml`, open it with Notepad, and change `method: cat` to
        `method: fsr`.
        * Otherwise (at least on my machine), the game looks fine on my monitor, but inside my VR headset the screen is
          black.
   * **Note:**
     If you verify the integrity of your game files in Steam, Steam will (partially) overwrite this mod, and you will
     have to re-install this mod.
   * **Untested alternative:** [Fallout4 Upscaler VR](https://www.nexusmods.com/fallout4/mods/73715)
4. **[xSE PluginPreloader F4](https://www.nexusmods.com/fallout4/mods/33946)** (v0.2.5.1) <sub>![required]</sub>  
   Will pre-load F4SEVR scripts before loading a save.
   * **Installation instructions:**
     1. Go to the [NexusMods page](https://www.nexusmods.com/fallout4/mods/33946).
     2. Go to "Files", click "Manual download", and again click "Download".
     3. Extract the downloaded file into `[fo4vr_dir]`.
     4. If you did this correctly, you should have the file `IpHlpAPI.dll` in the same directory as `Fallout4VR.exe`.

> [!NOTE]
> From now on, all listed mods should be downloaded and installed through MO2.

## 4.2 Libraries<a name="libraries"></a> <small><sup>[top ▲](#toc)</sup></small>
These mods provide utilities used in other mods.
These do not affect your game directly, but are required by many other mods.

1. **[Address Library for F4SE Plugins](https://www.nexusmods.com/fallout4/mods/47327)** (v1.10.163.0) <sub>![required]</sub>
2. **[VR Address Library for F4SEVR](https://www.nexusmods.com/fallout4/mods/64879)** (v1.6.1) <sub>![required]</sub>
3. **[Fallout4 VR Tools](https://www.nexusmods.com/fallout4/mods/45167)** (v0.1) <sub>![required]</sub>

## 4.3 Stability and Patches<a name="stability-and-patches"></a> <small><sup>[top ▲](#toc)</sup></small>
These mods fix bugs, either in the base game or in other mods.

1. **[Fallout 4 Version Check Patcher](https://www.nexusmods.com/fallout4/mods/42497)** (v1.00) <sub>![required]</sub>  
   (**TODO: Move this to Section 1.1?**)
   FO4VR and FO4 don't have the exact same engine because FO4VR is derived from an older version of FO4.
   If someone makes a mod for FO4, it will contain the version number of the engine it's made for.
   If you then use this mod in FO4VR, you'll get warnings because the mod uses a newer version of the engine you're
   using.
   This mod disables those warnings.
   The only major relevant bug that can accidentally occur because of this version mismatch is that your game will crash 
   immediately when you load an incompatible mod, so if you see the warning (without using this mod) then it means you
   didn't have problems anyway...
2. **[Unofficial Fallout 4 Patch - UFO4P](https://www.nexusmods.com/fallout4/mods/4598)** (v2.1.5) (requires all DLC) <sub>![required]</sub>  
   Fixes a bunch of bugs, big and small, in the base game.
   Though there are some incompatibilities because VR is not supported by the mod authors (like with most other mods on
   this list), overall the pros outweigh the cons.
3. **[Unofficial Fallout 4 VR Fix](https://www.nexusmods.com/fallout4/mods/47117)** (v1) (requires all DLC) <sub>![required]</sub>  
   Fixes a VR-specific bug in UFO4P.
   * **Load order:** Below UFO4P (**TODO: Move this elsewhere?**)
4. **[DLCVR - Fallout 4 VR and DLC standalone bug fixes](https://www.nexusmods.com/fallout4/mods/28842)** (v1.0.4) (requires FO4FH or FO4NW) <sub>![required]</sub>  
   Fixes issues specific to FO4FH and FO4NW, relating to invisible floors and so on.
   * **Variant:** Depends on your DLC.
5. **[Edmond's Automatron VR Workbench Rebuild](https://www.nexusmods.com/fallout4/mods/55692)** (v1.0) (requires FO4AU and FO4NW) <sub>![required]</sub>  
   Re-implements parts of FO4AU that did not work in VR. Some parts of FO4AU are still broken even with this mod.
   * **Variant:** "No wild edits"
6. **[Buffout 4](https://www.nexusmods.com/fallout4/mods/47359)** (v1.28.6) <sub>![required]</sub>  
   Fixes engine bugs and adds a crash logger.
7. **[Buffout 4 NG with PDB support](https://www.nexusmods.com/fallout4/mods/64880)** (v1.13.1) <sub>![required]</sub>  
   Same as above, but for VR.
8. **[Multiple Floors Sandboxing](https://www.nexusmods.com/fallout4/mods/15608)** (v1.0) <sub>![required]</sub>  
   In locations with multiple storeys, NPCs walk only on the ground storey.
   This mod fixes that behaviour so NPCs walk on all storeys.
9. **[No Aggro Impact Landing (Power Armor)](https://www.nexusmods.com/fallout4/mods/9019)** (v1.0) <sub>![required]</sub>  
   If you wear power armour and fall from a height, you will create a shock wave that damages NPCs around you.
   Friendly NPCs damaged this way may become hostile, even if you do so by accident.
   This mod ensures that you do not accidentally turn friendly NPCs hostile this way.
10. **[Radio Reverb Fix](https://www.nexusmods.com/fallout4/mods/16563)** (v1) <sub>![recommended]</sub>  
    Applies reverb to your radio when applicable.
    * **Variant:** "Subtle" _or_ main file
11. **[Bird Fix](https://www.nexusmods.com/fallout4/mods/45429)** (v1) <sub>![required]</sub>  
    Fixes a bug where birds are _always_ flying into buildings for some reason.
    * **Note:** You can ignore the listed dependencies.
13. **TODO: My own custom patches!**

## 4.4 Performance<a name="performance"></a> <small><sup>[top ▲](#toc)</sup></small>
FO4VR is notorious for having sub-par performance.
The following mods help improve performance.

1. **[Insignificant Object Remover](https://www.nexusmods.com/fallout4/mods/9835)** (v1.0) <sub>![required]</sub>
   * (**TODO: Remove? I don't really care about the FPS.)
   * (**TODO: In the FOMOD, which variant?)
2. **[FAR - Faraway Area Reform](https://www.nexusmods.com/fallout4/mods/20713)** (v1.2) <sub>![required]</sub>
   * **Variant:** "Default Resolution"

## 4.5 Graphics<a name="graphics"></a> <small><sup>[top ▲](#toc)</sup></small>
1. **[Burst Impact Blast FX](https://www.nexusmods.com/fallout4/mods/57789)** (v9.51 + v0.952) (requires FO4AU, FO4FH, and FO4NW) <sub>![recommended]</sub>
   * **Variant:** main file _and_ "BIB-FX Fixed Bloatfly's too-large effect".
   * All options in the FOMOD installer are fine.
     If you're lazy, just spam "Next".
2. **[Visible Galaxy 4k and Framework](https://www.nexusmods.com/fallout4/mods/19127)** (v1.0) <sub>![required]</sub>
   * **Variant:** "Visible Galaxy"
3. **[Fallout 4 HD Overhaul 2k](https://www.nexusmods.com/fallout4/mods/65720)** (v1.01) <sub>![required]</sub>  
   FO4VR's default textures are too ugly for VR, and the high-resolution texture pack is (supposedly) too
   VRAM-consuming.
   This texture pack provides a nice balance.
   * **Variant:** All files in section "Main files"
   * **Note:** You can safely download files for which you do not own the required DLC
4. **[Vivid Fallout - All in One](https://www.nexusmods.com/fallout4/mods/25714)** (v1.9) <sub>![recommended]</sub>  
   Adds even nicer textures, but may have some performance impact.
   * **Variant:** "Best choice"
5. **[Water Enhanced](https://www.nexusmods.com/fallout4/mods/3281)** (v1) <sub>![required]</sub>  
   Improves water textures.
   * **Variant:** "2K Water"
6. **[Detailed Feral Ghouls](https://www.nexusmods.com/fallout4/mods/20555)** (v3.1) <sub>![recommended]</sub>
   * **Variant:** "Better Performance - Non ESP Version"
7. **[Classic Ghouls Redux](https://www.nexusmods.com/fallout4/mods/57362)** (v1) <sub>![optional]</sub>  
   Changes (non-feral) ghoul textures to look more like ghouls from Fallout 3.

## 4.6 Lighting<a name="lighting"></a> <small><sup>[top ▲](#toc)</sup></small>
(**TODO: Note source from which I stole this configuration.**)

1. **[Darker Nights](https://www.nexusmods.com/fallout4/mods/191)** (v1.11p6) <sub>![recommended]</sub>
   * **Variant:** main file _and_ "No Glow Fix for Far Harbor DLC".
2. **[PhyLight](https://www.nexusmods.com/fallout4/mods/25740)** (v1.1) <sub>![required]</sub>
   * **Variant:** "PhyDark (164)" _and_ "No Interior Dust or Fog"
3. **[Vanilla Eye Adaptation Fix - All DLC](https://www.nexusmods.com/fallout4/mods/52129)** (v1.1) (requires all DLC) <sub>![required]</sub>
   * **Variant:** the one with version 1.1
4. **[Fr4nsson's Light Tweaks](https://www.nexusmods.com/fallout4/mods/2139)** (v1.6) <sub>![required]</sub>
   * **Variant:** "plus Bloom Remover"
5. **[Interiors Enhanced - Darker Ambient Light and Fog](https://www.nexusmods.com/fallout4/mods/8768)** (v2.0) <sub>![required]</sub>
   * **Variant:** Depends on your DLC.

## 4.7 Sound<a name="sound"></a> <small><sup>[top ▲](#toc)</sup></small>
The sound is actually fine in VR.
However, it doesn't hurt to improve sound effects for VR, and to add more high-quality music. 

1. **[Faded Glory - A Post-Apocalyptic Soundscape](https://www.nexusmods.com/fallout4/mods/26014)** (v5-1) <sub>![optional]</sub>
2. **[Fallout Suite - Soundtrack Extension](https://www.nexusmods.com/fallout4/mods/15870)** (v1.1) <sub>![optional]</sub>
3. **[Bleak Beauty - A Fallout 4 Fan Made OST](https://www.nexusmods.com/fallout4/mods/9663)** (v1.2) <sub>![optional]</sub>
4. **[Musical Lore - Wasteland Edition (Soundtrack Mod By Nir Shor)](https://www.nexusmods.com/fallout4/mods/14531)** (v1.6) <sub>![optional]</sub>  
   Adds new high-quality songs to the game's radio.
5. **[Ambient Wasteland - Fallout 4 Edition](https://www.nexusmods.com/fallout4/mods/25343)** (v0.1) <sub>![recommended]</sub>  
   Adds a whole bunch of ambient, distant background sounds to make the world feel more lively.
6. **[Realistic Reverb and Ambience Overhaul - VR and FP](https://www.nexusmods.com/fallout4/mods/61140)** (v6) <sub>![recommended]</sub>  
   Tweaks sound levels in "Ambient Wasteland - Fallout 4 Edition" for VR.
   * **Variant:** "Realistic Reverb and Ambience Overhaul V6"
   * **Requires:** "Ambient Wasteland - Fallout 4 Edition"
7. **[Project Reality Footsteps FO4](https://www.nexusmods.com/fallout4/mods/35904)** (v1.7) <sub>![recommended]</sub>  
   Adds more different kinds of footstep sounds.
   * **Variant:** "BA2"
8. **[Not Great Not Terrible - Scarier Geiger Counter Sounds](https://www.nexusmods.com/fallout4/mods/45354)** (v1.0) <sub>![optional]</sub>  
   Replaces geiger counter sounds to be more intense.
   * **Variant:** "Quieter Version" _or_ "Main File"

## 4.8 UI<a name="ui"></a> <small><sup>[top ▲](#toc)</sup></small>
The UI in VR is unintuitive to navigate, and the key bindings shown in the UI are usually incorrect.
Unfortunately, there are currently no good UI mods for VR.
[FallUI](https://www.nexusmods.com/fallout4/mods/48758) (v2.2.1) sort of works, but suffers from a variety of bugs in
VR, like bad contrast between text and background, menus being too small, and some VR-only menus not being replaced at
all.
[MCM](https://www.nexusmods.com/fallout4/mods/21497) (v1.39) also doesn't work; mods that use MCM are fine, but you
can't configure them through MCM.

1. **[Full Dialog VR](https://www.nexusmods.com/fallout4/mods/28516/)** (v1.1) <sub>![recommended]</sub>
   In conversations, you usually have four response options.
   The game summarises these using keywords.
   This is annoying, because your character may say something completely different from what you expected.
   This mod replaces the keywords with the full line your character will say.
   * After installing, edit the mod's files, and remove the file `interface\MultiActivateMenu.swf`.
     This fixes a bug where no text is shown at all when talking with followers.

## 4.9 Gameplay<a name="gameplay"></a> <small><sup>[top ▲](#toc)</sup></small>
1. **[FRIK - Full Player Body with IK](https://www.nexusmods.com/fallout4/mods/53464)** (v0.58) <sub>![required]</sub>  
   Allows you to see your hands.
   Absolutely required for immersion.
   * **Variant:** "alpha 58" (**TODO: Verify this**)
   * **[Requires in-game configuration](#finishing-up)**
   * **Important:** Download this mod, but **keep it deactivated in MO2 for now**.
   * **Untested alternative:** [Idle Hands](https://www.nexusmods.com/fallout4/mods/42922)
3. **[Player Collision Options - nocollide actors](https://www.nexusmods.com/fallout4/mods/41866)** (v1.0) <sub>![required]</sub>  
   Normally, when you get close to an NPC in VR, the game will push you back. This is annoying and disorienting when you
   want to roleplay or pet your dog.
   This disables collisions between you and NPCs.
   * **Variant:** "nocollide actors"
5. **[Realistic Death Physics - No Animations](https://www.nexusmods.com/fallout4/mods/4371)** (v1.2) <sub>![recommended]</sub>  
   Merely "recommended" because there is a slightly increased chance that there's some physical glitching going on.
   The trade-off there is yours to make.
   * **Variant:** "ALL DLC version" if you have all DLC, or "No Animations" otherwise
   * (**TODO: Test variant "Vanilla Physics - No Animations"**) / (**TODO: Check required DLC**)
6. **[PipBoy VR light](https://www.nexusmods.com/fallout4/mods/29245)** (v1.1) <sub>![required]</sub>  
   In VR, the default Pip-Boy light (the "flashlight") is just a weak glow around you.
   I really liked the flashlight in Half-Life: Alyx.
   This mod changes the shape of the Pip-Boy's light to be like a flashlight, and does so with no performance overhead.
   I personally chose the small light because I want it to be scary, but you can choose any variant you want.
   * **Variant:** main file _and_ one optional file.
     (I chose "Gun style aimed Small Gobo".)
7. **[Everyone's Best Friend](https://www.nexusmods.com/fallout4/mods/13459)** (v3.0.0) <sub>![recommended]</sub>  
   Normally you can only have one follower, but Dogmeat really isn't comparable to the depth of the other companions.
   But Dogmeat is also really cute.
   This mods lets you have both Dogmeat and any other companion at the same time.
   * **Patch:** [EBF UFO4P compatibility fix](https://www.nexusmods.com/fallout4/mods/43409) (v2.1.0)
8. **[Splinterz - Breakable Wooden Doors](https://www.nexusmods.com/fallout4/mods/21521)** (v1.3) <sub>![optional]</sub>  
   Allows you to break doors.
   Pretty cool.
   * **Variant:** Depends on your DLC.

## 4.10 Combat<a name="combat"></a> <small><sup>[top ▲](#toc)</sup></small>
(**TODO: Source**)

1. **[See-Through-Scopes](https://www.nexusmods.com/fallout4/mods/9476)** (v2.5.3) <sub>![required]</sub>  
   Changes in-game scopes so they are see-through.
   Required for the next mod.
2. **[Better Scopes VR](https://www.nexusmods.com/fallout4/mods/61214)** (v0.9) <sub>![required]</sub>  
   This one is _absolutely_ required.
   Without this mod, when you look down a scope, your screen turns black and you get a full-screen 2D projection of what
   you can see through your scope.
   Absolutely horrible and nauseating.
   This mod removes that screen, and just lets you look through the actual scope.
   * **Variant:** main file only, not the optional file.
3. **[Bullet Time VATS VR](https://www.nexusmods.com/fallout4/mods/72502)** (vb1.1) (requires FO4FH and FO4NW) <sub>![required]</sub>  
   In vanilla, VATS is a gameplay mechanic that pauses combat and lets you select body parts to target, which you will
   then automatically shoot at.
   This sucks in VR, because you don't get to aim the gun and pull the trigger yourself.
   This mod replaces VATS with bullet time.
   * **[Requires in-game configuration](#finishing-up)**
4. **[Critical Hits Outside of VATS](https://www.nexusmods.com/fallout4/mods/12653)** (v1.1.3) <sub>![required]</sub>  
   The above Bullet Time mod actually disables VATS, and thus completely removes critical hits from the game.
   This mod allows you to score critical hits again, even outside of bullet time.
5. **[Hip-Fire Perk Replacers](https://www.nexusmods.com/fallout4/mods/40702)** (v1.2) <sub>![required]</sub>  
   In vanilla, hip-fire is when you shoot without aiming down the sights.
   In VR, hip-fire doesn't exist.
   As a result, hip-fire perks are useless.
   This mod makes those perks useful again.
   * **Variant:** Depends on your DLC.
7. **[Weapon Accuracy Redone for VR](https://www.nexusmods.com/fallout4/mods/40669)** (v1.0) <sub>![required]</sub>  
   In VR it's super annoying if you're clearly aiming at an enemy and then the game decides the shot didn't hit because
   of some random die.
   This mod reduces weapon spread and recoil to make accuracy in VR more rewarding.
   * **Variant:** Depends on your DLC.
9. **[Better Low Health](https://www.nexusmods.com/fallout4/mods/6018)** (v1.0) <sub>![recommended]</sub>  
   Your health bar is visible on the inside of your wrist, but that's also where you're holding your gun, so during
   combat you typically don't really know how much health you have left.
   The game shows some visual effects at 20% health left, but that's usually too late.
   This mod increases that threshold to 50%.
   * **Variant:** "50"
10. **[More Noticeable Hit Effect](https://www.nexusmods.com/fallout4/mods/6157)** (v1.0) <sub>![required]</sub>  
   I noticed that during fights I usually had no idea if bullets were flying past me or into me.
   This mod makes it much more noticeable when you are being hit.
   * **Variant:** "aMedium"

## 4.11 Difficulty / Survival<a name="difficulty-survival"></a> <small><sup>[top ▲](#toc)</sup></small>
Fallout 4 is not a difficult game, even at higher difficulties.
In VR, it only gets easier.
Mods in this category affect the difficulty.
Some (but not all) of them assume you play in Survival mode, which I recommend you do anyway.

1. **[Survival Options](https://www.nexusmods.com/fallout4/mods/14650)** (v1.7.1) <sub>![recommended]</sub>  
   Allows you to customise your survival mode experience. Lets you re-enable fast travel, manual saves, auto-saves, and
   change damage multipliers.
    * Recommended even for non-survival playthroughs! (**TODO: Config link**)
    * **[Requires in-game configuration](#finishing-up)**
2. **[JOURNEY](https://www.nexusmods.com/fallout4/mods/12685)** (v1.6.1) <sub>![recommended]</sub>  
   Re-enables a restricted form of fast travel.
   You can use this together with the above mod.
   * **[Requires in-game configuration](#finishing-up)**
3. **[Campsite](https://www.nexusmods.com/fallout4/mods/11734)** (v1.0.4) <sub>![recommended]</sub>  
   Lets you bring a tent with you so you can sleep anywhere.
4. **[Loot Logic and Reduction With optional Harvest Restrictions](https://www.nexusmods.com/fallout4/mods/21366)** (v1.5.3.1) <sub>![recommended]</sub>  
   Reduces loot found in containers. Otherwise you'll quickly find you'll have so much ammo and chems the game just
   totally isn't challenging anymore.
5. **[NPC Loot Drop rebalance](https://www.nexusmods.com/fallout4/mods/24163)** (v1.0) <sub>![recommended]</sub>  
   Reduces loot found on NPCs, in line with the above mod.
6. **[Backpacks of the Commonwealth](https://www.nexusmods.com/fallout4/mods/29447)** (v1.5.4) (requires FO4AU, FO4FH, and FO4NW) <sub>![recommended]</sub>  
   In survival, you have less carrying capacity and heavier items. These backpacks will come in use.
   * **Variant:** "1.5.4"
8. **[Dogmeat's Backpack](https://www.nexusmods.com/fallout4/mods/10111)** (v2.0) <sub>![recommended]</sub>  
   As above, but now for your companion.
9. **[Dogmeat's Backpacks of the Commonwealth](https://www.nexusmods.com/fallout4/mods/62037)** (v1.3) <sub>![recommended]</sub>  
   Re-balances the above mod to be in line with the one above that.
   * **Requires:** The two mods above this one.
11. **[Headshot Damage Multiplier](https://www.nexusmods.com/fallout4/mods/33546)** (v1.0) <sub>![recommended]</sub>
   * **Variant:** "x5"
   * (**TODO: Test this**)
11. **[Radiation Overhaul - 4x More Radiation Across the Wasteland](https://www.nexusmods.com/fallout4/mods/13790)** (v1.1) <sub>![optional]</sub>  
    Makes radiation actually dangerous.
    * **Variant:** Depends on your DLC.

## 4.12 Settlements<a name="settlements"></a> <small><sup>[top ▲](#toc)</sup></small>
I think Fallout 4's settlements are very flawed.
In VR, they are not necessarily more or less flawed than in non-VR, so the mods in this section are not VR-specific.
However, several of these mods require VR-specific tweaks.
That said, this entire section is recommended, because the VR experience is no worse than the non-VR experience with or
without these.
If you don't intend to engage with settlements at all, you can skip this section.

> [!CAUTION]
> If you install Sim Settlements, you **must** choose version 4.1.7.
> Newer versions do not work.

1. **[Sim Settlements](https://www.nexusmods.com/fallout4/mods/21872)** (v4.1.7) <sub>![recommended]</sub>  
   Completely changes the way settlements are built.
   Instead of you building everything, settlers will build and upgrade their own houses in designated locations.
   I especially like the "leaders" feature, where you can appoint a settlement leader who will oversee the placement of
   all buildings in the settlement.
   It just works.
   * **Variant:** "Three In One **v4.1.7**"
   * **[Requires in-game configuration](#finishing-up)**
   * **Untested alternative:** [Sim Settlements 2](https://www.nexusmods.com/fallout4/mods/47976)  
     There are guides out there on how to get Sim Settlements 2 working on FO4VR, but these have not been tested with
     this guide.
     I recommend you err on the side of caution and avoid Sim Settlements 2.
2. **[Leaders Of The Commonwealth](https://www.nexusmods.com/fallout4/mods/30495)** (v2) <sub>![recommended]</sub>  
   With basic Sim Settlements, only your followers are leaders.
   Especially at the start of the game, it's frustrating if your settlements can't grow because you don't have enough
   leaders for the number of settlements you find.
   This mod designates several unique settlers from the base game as leaders.
   * **Variant:** "Vanilla Looks No New npcs".
3. **[Salvage Beacons](https://www.nexusmods.com/fallout4/mods/18757)** (v1.0.4) <sub>![optional]</sub>  
   Carrying junk back to your settlement is frankly a waste of time.
   This lets you drop off your junk and whatnot in any container, then mark that container, and your settlers will take
   back your loot to your settlement.
4. **[IDEK's Logistics Station 2](https://www.nexusmods.com/fallout4/mods/48389)** (v2.1.3) <sub>![recommended]</sub>  
   I wasn't sure whether to make this recommended or required.
   In Fallout 4, you can connect your settlements using supply routes, which allows the settlements to share resources.
   Unfortunately, this feature is super annoying to use, hard to get right, and hard to manage.
   This mod automates most of that part:
   You just build one object, assign a settler, and the mod will handle all the routing.
   There's also a bunch of other really useful features which improve the stability of your trading routes.
   * **[Requires in-game configuration](#finishing-up)**
5. (**TODO: Local leader**)


# 5 Finishing up<a name="finishing-up"></a> <small><sup>[top ▲](#toc)</sup></small>
> [!WARNING]
> Make sure [FRIK](https://www.nexusmods.com/fallout4/mods/53464) remains disabled until you have exited the vault.

You should now have a good selection of mods from the previous selection installed.
You should have installed all required mods, probably several recommended mods, and maybe some optional mods.

The only thing that's left is to configure a few final mods.
Most mods don't need configuration, but a few do.
These mods can be configured after you've finished the prologue.
This section will take you through that process.

(**TODO: Make an easier overview.**)
The overall procedure is as follows:
1. [Read general tips.](#general-tips) (Section 5.1)
2. Launch the game.
3. [Configure controls.](#configure-controls) (Section 5.2)
4. Start a new game.
5. Play until you exit the vault.
6. [Configure mods.](#configure-mods) (Section 5.3)
7. Continue playing the game to your leisure.

## 5.1 General tips <small><sup>[top ▲](#toc)</sup></small>
(**TODO: Rephrase and restructure this.**)

* Always launch through MO2.
  Always use F4SEVR!
  (**TODO: Describe how to add F4SEVR in MO2**)
* Remove external gamepads before launching the game.
* Start your VR controllers before launching the game.
  If you start them too late, some buttons will not work, you'll notice this in the main menu when you try to scroll
  down.
  In that case, restart the game.
* In the main menu, if you select `Continue`, or select `Load` and then choose a save, and you notice nothing happens,
  pull the right trigger again (or whatever button you use to select).
  What happened is that there was a message saying you have changed your load order, asking for confirmation, but for
  some reason that message is invisible when in the main menu.
  If you want to see what the difference in load order is, then load the save, and then while in-game load that save;
  now the message will be visible.
* QuickSave is extremely unreliable and very often breaks mods/saves.
  AutoSave is somewhat unreliable and sometimes breaks mods.
  Therefore, manually save often, and avoid loading QuickSaves or AutoSaves.
  (Making an AutoSave or QuickSave by itself is not harmful.
  It's just that you shouldn't load them.)
  You can use the Survival Options mod mentioned earlier to replace Quick-Saves with Saves.
* Don't use your pipboy while the light is on!
  You may get a CTD otherwise.
  Some claim that Buffout4 fixes this, but in my game, it didn't, as I would continue to CTD.
* Don't swim, lol

## 5.2 Configure controls<a name="configure-controls"></a> <small><sup>[top ▲](#toc)</sup></small>
(**TODO**)

## 5.3 Configure mods<a name="configure-mods"></a> <small><sup>[top ▲](#toc)</sup></small>
(**TODO**)

### 5.3.1 FRIK <small><sup>[top ▲](#toc)</sup></small>
> [!WARNING]
> Make sure [FRIK](https://www.nexusmods.com/fallout4/mods/53464) remains disabled until you have exited the vault.

(**TODO**)

### 5.3.2 Bullet Time VATS VR <small><sup>[top ▲](#toc)</sup></small>
(**TODO**)

### 5.3.3 Survival Options <small><sup>[top ▲](#toc)</sup></small>
(**TODO**)

### 5.3.4 Journey <small><sup>[top ▲](#toc)</sup></small>
(**TODO**)

### 5.3.5 Sim Settlements <small><sup>[top ▲](#toc)</sup></small>
(**TODO**)

### 5.3.6 IDEK's Logistics Station 2 <small><sup>[top ▲](#toc)</sup></small>
(**TODO: Complete this section**)

There is an option to integrate this with Sim Settlements and with Salvage Beacons, but I didn't use those
integrations because I couldn't figure them out.


# 6 Conclusion <small><sup>[top ▲](#toc)</sup></small>
That's it!
I hope this guide was useful for you :-)


  [required]:    https://img.shields.io/badge/required-red?style=flat-square

  [recommended]: https://img.shields.io/badge/recommended-orange?style=flat-square

  [optional]:    https://img.shields.io/badge/optional-blue?style=flat-square

  [reddit]:      https://img.shields.io/badge/-%2300000000?style=flat-square&logo=reddit
