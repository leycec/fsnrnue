![Fate/stay night \[Réalta Nua\]](https://user-images.githubusercontent.com/217028/74502954-3ada0500-4ee7-11ea-849e-1ef29f34b512.jpg)

Fate/stay night [Réalta Nua] Ultimate Edition… for Linux!
=========================================================

This repository officially hosts the [Lutris-based **Linux**
installer][ultimate-lutris] for *[Fate/stay night \[Réalta Nua\] Ultimate
Edition][ultimate-bl]* – a fan-driven third-party application automating the
installation, patching, and execution of the *[\[Réalta Nua\]
variant](https://typemoon.fandom.com/wiki/Fate/stay_night#R.C3.A9alta_Nua)* of
the [seminal Japanese visual novel *Fate/stay
night*](https://typemoon.fandom.com/wiki/Fate/stay_night).

> ⚠️

> This repository does *not* officially host **Windows** installers for
> *[Fate/stay night \[Réalta Nua\] Ultimate Edition][ultimate-bl]*. If you are
> a **Windows** user and currently having issues under **Windows**, please
> [direct bug reports to the upstream forum discussion][ultimate-bl] at the
> [Beast's Lair][beasts-lair]. Thanks – and sorry for the confusion! 😅

## Downloads

[Current downloads hosted at this repository][releases] include:

* [Lutris-based][lutris] Linux installers: <sup>*see [installation
  instructions below](#installation)*</sup>
  * _(Recommended)_ **[One-click installer][installer-remote],** automatically
    installing *[Fate/stay night \[Réalta Nua\] Ultimate Edition][ultimate-bl]*
    via [lutris.net browser integration](https://lutris.net/faq#url-handler).
  * **[Offline installer][installer-local],** suitable for manually
    installing *[Fate/stay night \[Réalta Nua\] Ultimate Edition][ultimate-bl]*
    via the `lutris -i` command-line option.
* _(Unofficial)_ **[32-bit Windows
  installer](https://github.com/leycec/fsnrnue/releases/download/2019.03.19/fsnrnue-2019.03.19-32.zip).**
* _(Unofficial)_ **[64-bit Windows
  installer](https://github.com/leycec/fsnrnue/releases/download/2019.03.19/fsnrnue-2019.03.19-64.zip).**

## Installation

1. **Get _Fate/stay night [Réalta Nua]_.** Sadly, all versions of *Fate/stay
   night* (including the most recent *[Réalta Nua]* release) are unavailable
   for purchase and [thus constitute
   abandonware](https://en.wikipedia.org/wiki/Abandonware). Instead:
   1. Search for these exact terms: [`nyaa "Fate/stay night [Realta Nua] for
      Windows"`](https://www.google.com/search?q=nyaa+%22Fate%2Fstay+night+%5BRealta+Nua%5D+for+Windows%22&oq=nyaa+%22Fate%2Fstay+night+%5BRealta+Nua%5D+for+Windows%22)
   1. Click on the topmost hit. <sup>...*probably*</sup>
   1. Download the 6.4GB directory `"Fate stay night Realta Nua/"` containing
      these six files:
      * `Fate.rar`.
      * `Fate Crack.rar`.
      * `Heaven's Feel.7z`.
      * `Heaven's Feel Crack.rar`.
      * `Unlimited Blade Works.rar`.
      * `Unlimited Blade Works Crack.rar`.
1. If your current platform is:
   * **Windows:**
     1. First, follow [steps 1, 2, and 3 *only* of the "Fate/Stay Night VN
        Installation Guide
        VII."](https://www.reddit.com/r/fatestaynight/comments/7qh6ho/fatestay_night_vn_installation_guide_vii)
     1. Then follow the [official Ultimate Edition instructions][ultimate-bl].
   * **Linux:**
     1. **[Install *Lutris*][lutris].**
     1. **Install _Fate/stay night \[Réalta Nua\] Ultimate Edition_** with
        either:
        * *(Recommended)* [**Our one-click installer**][installer-remote],
          automating installation by transparently downloading and running this
          installer under *[Lutris][lutris].*
        * **Our offline installer,** manually runnable at the command line as
          follows:
          1. [Download this file][installer-local].
          1. Open a terminal to the directory containing that file.
          1. Copy-and-paste this command into that terminal:

                 lutris -i fate-stay-night-realta-nua-ultimate-edition.yml

   * **macOS is currently unsupported,** as [Lutris][lutris] is currently
     Linux-specific. In theory, porting our [Lutris-specific
     installer][installer-local] to [PlayOnMac][playonmac]
     *should* be feasible but non-trivial. If someone does so, please submit an
     [issue](https://github.com/leycec/fsnrnue/issues) or [pull
     request](https://github.com/leycec/fsnrnue/pulls) and we'll update these
     instructions accordingly.

## Configuration

We strongly recommend:

* **Enabling the *Patch* → *Options* → *Skip movies in-game* option.** Consider
  watching these movies either online or via the **_Extras_** title option
  available after successfully completing the Prologue. Attempting to play
  movies usually raises fatal exceptions (e.g., at the fade-to-white Prologue
  ending) with error messages resembling one or more of:
  * `0009:fixme:gstreamer:mpeg_splitter_sink_query_accept Unsupported subtype {e436eb84-524f-11ce-9f53-0020af0ba770}.`
  * `00:15:24 ==== An exception occured at movie.tjs(210)[(function) open], VM ip = 81 ====`
  * `00:15:25 exception: (object 0x1184E098:0x1184E098)"Cannot convert the variable type ((void) to Object)"`
* **Disabling the *Patch* → *Vita Additions* → *Play Vita OP in-game* option.**
  In addition to raising fatal exceptions, Vita movies also contain heavy
  spoilers – especially for Heaven's Feel, the final route and grand finale.
  (All remaining patches are spoiler-free.)
* **Enabling the *Display* → *Aspect Ratio* → *Standard* option** (i.e., the
  default) rather than the **_Wide_** option, which is known to be error-prone.

## Usage

Lastly, note these [undocumented keyboard
shortcuts](https://www.reddit.com/r/fatestaynight/comments/42vvy4/keyboard_shortcutshotkeys_for_fatestay_night_vn):

Key | Action
--- | ---
Space/Enter | Next line (& pause auto-read)
Down/Up Arrow | Next/Previous
A | Auto-read (toggle)
R | Review history/previous page
F | Fast skip to next scene or choice
Ctrl | Fast skip pages/scenes (hold)
S | Save menu
L | Load menu
Q | Quick Save/Load (for F1-F9)
F1-F9 | Quick load specific save data slot
Esc | Menu
Backspace | Show background (hide text)
Alt+Enter | Toggle fullscreen
C | Config

## FAQ

#### It doesn't even start, though?

Startup failures are *almost* always due to **corrupt patch downloads.** If
you see any of the following at startup, the Ultimate Edition installer failed
to properly download one or more patches for you:

* An untranslated GUI error message entitled with indecipherable Japanese kanji
  and text resembling:

  > ☐☐☐☐☐☐
  > file://./c/program/files/fate☐stay night[realta
  > nua] ultimate edition/patch.xp3 ☐☐ XP3 ☐☐☐☐
  > ☐☐☐☐☐☐☐☐☐

    ![startup-gui-error-corrupt-patch](https://user-images.githubusercontent.com/217028/94880506-a19a3780-0452-11eb-9bd8-146338027136.png)

* A translated GUI error message entitled "Script exception raised Read error"
  with text resembling:

  > Script exception raised
  > file://./c/program files/fate／stay night[realta
  > nua] ultimate edition/patch.xp3 is not XP3 archive or
  > unsupported.

* A log error message containing lines resembling:

```
16:22:47 ==== An exception occured at initialize.tjs(214)[(top level script) global], VM ip = 694 ====
16:22:47 -- Disassembled VM code --
16:22:47 #(214) if(Storages.isExistentStorage("Config.tjs"))
16:22:47 00000687 const %1, *70	// *70 = (string)"Config.tjs"
16:22:47 00000690 gpd %2, %-2.*71	// *71 = (string)"Storages"
16:22:47 00000694 calld %3, %2.*72(%1)	// *72 = (string)"isExistentStorage"
16:22:47 -- Register dump --
16:22:47 %-7=(object)(object 0x00FA1778:0x00FA1778)  %-6=(string)"type"  %-5=(int)28  %-4=(void)
16:22:47 %-3=(void)  %-2=(object)(object 0x0032F684:0x00000000)
16:22:47 %-1=(object)(object 0x00F800E0:0x00F800E0)  %0=(void)  %1=(string)"Config.tjs"
16:22:47 %2=(object)(object 0x00F9DB28:0x00000000)  %3=(void)
16:22:47 %4=(object)(object 0x00FA6968:0x00000000)  %5=(object)(object 0x00FAA650:0x00000000)
16:22:47 %6=(string)"Win32"  %7=(string)")"  %8=(object)(object 0x00FA6968:0x00000000)
16:22:47 ---------------------------------------------------------------------------------------------

16:22:47 trace : startup.tjs(27)[(top level script) global] <-- startup
```

#### Nice magic words you wizardperson. What are these "log error messages"?

**Okay.** We're gonna have to take you back to the year... *1979.* Apparently,
people were actually alive back then. We know this, because 1979 was the year
[Bourne shell and thus effectively POSIX and UNIX-as-we-all-know-it-today was
bourne][unix-bourne]. Get it, *bourne*? <sup>Yes. I'll stop now.</sup>

Because you want to know how to get Lutris logs, you're probably using the
default UNIX shell under most Linux distributions: either [Bash (Bourne-Again
Shell)][unix-bash] or [zsh][unix-zsh]. Both historically descend from [Bourne
shell][unix-bourne], which means the answer here is the same. In either case:

1. Open a command-line (CLI) terminal.
1. To log output from our **online installer**, copy-and-paste this command:

        lutris 2>& ohgodeverythingbroke.log

1. To log output from our **offline installer**, copy-and-paste this command:

        lutris -i fate-stay-night-realta-nua-ultimate-edition.yml 2>& ohgodeverythingbroke.log

Log error messages will now appear in the file `ohgodeverythingbroke.log`. When
reporting issues to our [issue tracker][issue-tracker], please either:

* **Copy-and-paste** the contents of that file into your issue.
* **Upload** that entire file as an attachment with your issue.

Please be patient. Sakura will attend to your "needs" shortly.

#### Okay. I am indeed seeing this exception, I think?

**Great!** Well, not great – but things could be worse. You could be Shiro in
any of the Dead Ends you're about to compulsively read just to collect all of
the Taiga Dojo stamps just to unlock a ridiculous hot springs bath scene.
<sup>Totally worth it.</sup>

So, we've confirmed the Ultimate Edition installer failed to properly download
one or more patches for you. (We are shocked Pikachu face.) These patches are
now locally corrupt and *must* be:

1. **Manually redownloaded** from either:
   * _(Recommended)_ [**A monstrous 1.75GB password-protected Mediafire-hosted
     zipfile containing every patch**][patches-mediafire], including patches
     you really didn't want but will end up enabling anyway just because you
     downloaded them. Yup, password-protected! Gotta keep out the riff-raff.
     The password is:
     * `ObviouslyFate`
   * [Google Drive links listed under the **Mandatory patches** section of the
     original release notes for the Ultimate Edition][ultimate-bl]. Google
     Drive links are subject to questionable download quotas and thus
     frequently fail, which only begs the question: "Google, y u make billions
     but still such a cheapskate?"
1. **Manually extracted and copied** into the
   `fate-stay-night-realta-nua-ultimate-edition/drive_c/Program
   Files/Fate／stay night[Realta Nua] Ultimate Edition/` subdirectory to which
   the Ultimate Edition previously installed itself, overwriting each existing
   corrupt patch.

If you're unsure which corrupt patches need to be replaced, either blindly
replace *all* of them or:

* Inspect the aforementioned subdirectory for 0-byte filenames prefixed by
  `patch_`: e.g.,

```
$ ls -l $HOME/Games/fate-stay-night-realta-nua-ultimate-edition/drive_c/Program Files/Fate／stay
night[Realta Nua] Ultimate Edition/
total 4.8G
drwxr-xr-x  3 leycec leycec 4.0K Feb 14 01:23 .
drwxr-xr-x 11 leycec leycec 4.0K Feb 14 00:50 ..
drwxr-xr-x  2 leycec leycec 4.0K Feb 14 01:23 savedata
-rw-r--r--  1 leycec leycec 940M Feb 14 01:02 bgimage.xp3
-rw-r--r--  1 leycec leycec 137M Feb 14 01:03 bgm.xp3
-rw-r--r--  1 leycec leycec  200 Feb 14 01:17 config.ksc
-rw-r--r--  1 leycec leycec 4.8M Feb 14 01:03 data.xp3
-rw-r--r--  1 leycec leycec  13M Feb 14 01:03 etc.xp3
-rwxr-xr-x  1 leycec leycec 4.3M Feb 14 01:17 Fate.exe
-rw-r--r--  1 leycec leycec 300M Feb 14 01:03 fgimage.xp3
-rw-r--r--  1 leycec leycec  18M Feb 14 01:17 Flowchart.pdf
-rw-r--r--  1 leycec leycec  51M Feb 14 01:03 image.xp3
-rw-r--r--  1 leycec leycec    0 Feb 14 01:01 patch_decensor.xp3
-rw-r--r--  1 leycec leycec 1.3K Feb 14 01:32 patches.json
-rw-r--r--  1 leycec leycec 167M Feb 14 01:01 patch_h.xp3
-rw-r--r--  1 leycec leycec  15M Feb 14 00:55 patch_lang_english.xp3
-rw-r--r--  1 leycec leycec 120M Feb 14 00:55 patch.xp3
-rw-r--r--  1 leycec leycec  49K Feb 14 01:17 README-patch.html
-rw-r--r--  1 leycec leycec 8.1M Feb 14 01:03 rule.xp3
-rw-r--r--  1 leycec leycec 344M Feb 14 01:04 sound.xp3
-rw-r--r--  1 leycec leycec  23K Feb 14 01:17 supported_games.png
-rwxr-xr-x  1 leycec leycec  37M Feb 14 01:17 uninstall.exe
-rw-r--r--  1 leycec leycec  77M Feb 14 01:05 video.xp3
-rw-r--r--  1 leycec leycec 2.6G Feb 14 01:17 voice.xp3
-rw-r--r--  1 leycec leycec 1.1K Feb 14 01:17 xp3filter.tjs
```

* Run *Fate/stay night* from the command line and search for text in the
  terminal buffer resembling:

```
01:36:36 (info) Trying to read XP3 virtual file system information from : file://./c/program files/fate^stay night[realta nua] ultimate edition/patch_decensor.xp3
01:36:36 (info) Failed.
01:36:36 ==== An exception occured at initialize.tjs(197)[(function) KAGLoadScript], VM ip = 16 ====
```

In both cases, the decensor patch (i.e., `patch_decensor.xp3`) is corrupt and
must be manually redownloaded. It would be the decensor patch, wouldn't it?

![shocked Pikachu face](https://user-images.githubusercontent.com/217028/126600245-125ac88c-7d1d-4f5d-8ae7-091a015a6d90.png)

#### That's also not what I'm seeing.

…that's not even a question. You can tell because there's no question mark.

#### I'm seeing an error at "initialize.tjs(245)"?

Are you receiving an error resembling `"==== An exception occured at
initialize.tjs(245)[(top level script) global], VM ip = 840 ===="`? If yes,
then we're all on the same page, which is nice.

Did you also install the optional Vita patch? If:

* **Yes,** then [please reinstall *without* that
  patch](https://github.com/leycec/fsnrnue/issues/9).
* **No,** then continue to the next question.

#### I see something about Vulkan and `dxvk` in those logs and a black screen on startup, I think?

Do you see log errors resembling the following?

```
info: Game: Fate.exe
info: DXVK: v1.7.1-2-g743f309
info: Built-in extension providers:
info: Win32 WSI
info: OpenVR
warn: OpenVR: Failed to locate module
info: Required Vulkan extension VK_KHR_surface not supported
terminate called after throwing an instance of 'dxvk :: DxvkError'
Game is considered exited.
Initial process has exited.
All monitored processes have exited.
Exit with returncode 768
```

No? Then how about these:

```
info:  Game: Fate.exe
info:  DXVK: v1.7.3-4-g03f11baf
info:  Built-in extension providers:
info:    Win32 WSI
info:    OpenVR
warn:  OpenVR: Failed to locate module
info:  Enabled instance extensions:
info:    VK_KHR_get_surface_capabilities2
info:    VK_KHR_surface
info:    VK_KHR_win32_surface
warn:  Skipping Vulkan 1.0 adapter: llvmpipe (LLVM 11.0.0, 256 bits)
warn:  DXVK: No adapters found. Please check your device filter settings and Vulkan setup.
```

If so, **great!** Well, not great – but things could be worse. You could always
be running Windows, which is like a real-life Dead End you inflict on yourself.

First, let's refresh your faded memories of obscure APIs and acronyms:

* **[Vulkan][vulkan]** is the official replacement for
  [OpenGL](https://en.wikipedia.org/wiki/OpenGL), a popular cross-platform
  GPU-accelerated 3D rendering API. So, [Vulkan][vulkan] = OpenGL 2.0. Sorta.
  Close enough.
* **[DXVK](dxvk)** is a [Vulkan][vulkan]-based Linux-specific translation layer
  that internally converts Windows-specific DirectX 9, 10, and 11 GPU logic
  into equivalent [Vulkan][vulkan] logic.

Next, let's inspect the warnings and errors in the above error message:

* The `"warn: OpenVR: Failed to locate module"` line is safely ignorable. That
  just means you don't have a virtual reality (VR) headset connected, which is
  fine. VR's nice and all, but that's not really what we're going for here.
* The `"info: Required Vulkan extension VK_KHR_surface not supported"` and
  `"warn:  DXVK: No adapters found. Please check your device filter settings
  and Vulkan setup."` lines are where your troubles start. **Your
  [Vulkan][vulkan] and/or [DXVK][DXVK] installation is broken.** That's bad,
  because it means you won't be able to run any GPU-accelerated
  [Vulkan][vulkan] games. Thankfully, *Fate/stay night* is so old that it runs
  on decades-old potato PCs manufactured by RadioShack; it doesn't really
  benefit from GPU acceleration. Still, your system has an unresolved "oh shit"
  issue that will needlessly complicate your life until you finally fix it.

You have two options here:

* (*Recommended*) **Disable [Vulkan][vulkan] for *Fate/stay night*.** This is
  the easy way:
  1. Run *Lutris*.
  1. Right-click the *Fate/stay night* entry.
  1. Click the *Configure* menu item.
  1. Click the *Runner options* tab.
  1. Disable the *Enable DXVK/VKD3D* setting.
  1. Click *Save.*
  1. You're done. *Praise Ilya!*
* **Fix your broken [Vulkan][vulkan] and [DXVK][dxvk] installation.** This is
  the hard way, but you probably want to do this eventually *anyway*, because
  something has gone super-hyper-mega wrong on your system. Do this (in order):
  1. **Reinstall your video drivers.** This should *always* be the first thing
     you do when hitting Vulkan and DXVK issues.
  1. **Reinstall [Vulkan][vulkan] and [DXVK][dxvk].** Although instructions for
     installing, configuring, and enabling [Vulkan][vulkan] and [DXVK][dxvk] in
     Lutris vary by platform, the workflow always remains the same:
     1. Verify [**your hardware supports Vulkan and
        DXVK**][lutris-vulkan-requirements].
     1. Install [**Vulkan drivers**][lutris-vulkan-install].
     1. Download [**DXVK**][dxvk-releases]. Note that [DXVK 1.9.1][dxvk-1.9.1]
        has been verified to work with *Fate/stay night.* If you prefer
        dangerously experimenting with other DXVK versions, download either:
        * (*Recommended*) The precompiled **release binary tarball** of your
          choice (e.g., `dxvk-1.9.1.tar.gz` for DXVK 1.9.1).
        * The uncompiled **source code tarball** of your choice. Unless you use
          a bleeding-edge rolling-released source-friendly Linux distribution
          like Arch or Gentoo Linux, <sup>...which you don't, because you're
          reading this</sup> you do *not* want to walk this dark road. To quote
          @kaasknak: "You could also compile the binaries yourself if you want
          to but I didn't feel like installing a gigabyte worth of dependencies
          for that." You were warned but you're still doing this anyway, aren't
          you!?!?
     1. Extract the **DXVK tarball you just downloaded** into your
        user-specific Lutris DXVK subdirectory (defaulting to
        `~/.local/share/lutris/runtime/dxvk`): e.g.,

            tar -xvzf dxvk-1.9.1.tar.gz -C ~/.local/share/lutris/runtime/dxvk

     1. Run **Lutris.**
     1. Right-click *Fate/stay night.*
     1. Click *Configure.*
     1. Click the *Runner Options* tab.
     1. Check the *Show advanced options* checkbox at the lower left.
     1. Enter the basename of the directory you just extracted (e.g.,
        `dxvk-1.9.1` for DXVK 1.9.1) into the edit box to the right of the
        *DXVK version* label, replacing the prior contents of that box if any.
     1. Click *Save*.
     1. Rejoice as your CPU and GPU fans run as quiet as Sakura on a bad night
        out at the Shirou's.

When in doubt, just disable [Vulkan][vulkan] and [DXVK][dxvk].

#### I see a white screen but hear music playing on startup, maybe?

Do you see a log error resembling the following?

```
13:39:14 (info) Changing screen mode succeeded
13:39:14 ==== An exception occured at mainwindow.tjs(1029)[(property setter) fullScreen], VM ip = 837 ====
13:39:14 -- Disassembled VM code --
13:39:14 #(1029) 			windowSizeMenu.enabled	= !fullScreen;	//	EBhETCY̐ݒ̓EBhE\̂Ƃ̂
13:39:14 00000831 gpd %1, %-2.*97	// *97 = (string)"fullScreen"
13:39:14 00000835 lnot %1
13:39:14 00000837 gpd %2, %-2.*98	// *98 = (string)"windowSizeMenu"
13:39:14 -- Register dump --
13:39:14 %-6=(int)1  %-5=(int)-1  %-4=(void)  %-3=(int)1  %-2=(object)(object 0x009EE4E0:0x00000000)
13:39:14 %-1=(object)(object 0x059CC2B0:0x059CC2B0)  %0=(void)  %1=(int)0
13:39:14 %2=(object)(object 0x04E5F4B0:0x04E5F4B0)  %3=(int)0  %4=(int)1080
13:39:14 %5=(object)(object 0x04E5F4B0:0x04E5F4B0)  %6=(real)644  %7=(real)644
13:39:14 -------------------------------------------------------------------------------------------------
13:39:14 tXN[[hɈڍsł܂ł : Member "windowSizeMenu" does not exist
```

If so, **wonderful!** Well, not wonderful – but things could be worse. You
could always be using a decades-old AMD Athlon(tm) II X2 240 CPU like @leycec,
which is like a real-life Bad End the chip shortage inflicts on you.

Unfortunately, you probably need to disable [Vulkan][vulkan] and [DXVK][dxvk]
in Lutris. See the prior FAQ entry for detailed instructions, please.

#### I'm seeing the game freeze whenever I use the menu bar, I guess?

**That's horrible.** But you're not alone. So, that's great. I guess?

For dark reasons beyond all carnal human knowledge, <sup>I blame Nasu.</sup>
*Fate/stay night* is not playing ball with your Linux windowing system.
Circumvent this by isolating the game to a **windowed virtual desktop**
(instead of running the game full-screened):

1. Run *Lutris.*
1. Right-click the *Fate/stay night* entry.
1. Click the *Configure* menu item.
1. Click the *Runner options* tab.
1. Enable the *Windowed (virtual desktop)* setting.
1. Click *Save.*

Behold! A usable menu bar. Yes, it is beautiful. Yes, it is sad.

#### I'm seeing a "The file …Fate.exe could not be found" error?

Are you receiving an error resembling this dialog box:

![The file …Fate.exe could not be found](https://user-images.githubusercontent.com/49215755/121794332-c2787680-cbf6-11eb-9cb8-2c52492102df.png)

You might also be seeing a wall of milk-curdling command-line errors like:

```
0024:err:module:import_dll Library advapi32.dll (which is needed by L"C:\\windows\\system32\\rpcrt4.dll") not found
0024:err:module:import_dll Library ucrtbase.dll (which is needed by L"C:\\windows\\system32\\rpcrt4.dll") not found
0024:err:module:import_dll Library rpcrt4.dll (which is needed by L"C:\\windows\\system32\\setupapi.dll") not found
0024:err:module:import_dll Library ucrtbase.dll (which is needed by L"C:\\windows\\system32\\setupapi.dll") not found
0024:err:module:import_dll Library ucrtbase.dll (which is needed by L"C:\\windows\\system32\\version.dll") not found
0024:err:module:import_dll Library version.dll (which is needed by L"C:\\windows\\system32\\setupapi.dll") not found
0024:err:module:import_dll Library setupapi.dll (which is needed by L"C:\\windows\\system32\\user32.dll") not found
0024:err:module:import_dll Library ucrtbase.dll (which is needed by L"C:\\windows\\system32\\user32.dll") not found
0024:err:module:import_dll Library ucrtbase.dll (which is needed by L"C:\\windows\\system32\\version.dll") not found
0024:err:module:import_dll Library version.dll (which is needed by L"C:\\windows\\system32\\user32.dll") not found
0024:err:module:import_dll Library user32.dll (which is needed by L"C:\\windows\\system32\\start.exe") not found
0024:err:module:LdrInitializeThunk Importing dlls for L"C:\\windows\\system32\\start.exe" failed, status c0000135
------------------------------------------------------
warning: Note: command /home/user/.local/share/lutris/runners/wine/lutris-6.10-2-x86_64/bin/wine vc_redist.x86.exe /q returned status 53. Aborting.
------------------------------------------------------
Monitored process exited.
Initial process has exited (return code: 256)
All monitored processes have exited.
Exit with returncode 256
```

You were probably trying to run [**our one-click
installer**][installer-remote], right? If:

* **Yes,** then [please run **our offline installer** instead](Installation).
  While inconvenient, [our offline installer is hosted directly at this
  repository](Installation) and thus guaranteed to include [bug fixes not yet
  accepted by Lutris moderators into our one-click
  installer](https://github.com/leycec/fsnrnue/issues/11) – including the fix
  for this bug. The cost of convenience is indeed costly.
* **No,** then continue to the next question.

#### That's also not what I'm seeing, though?

Then here's what we're going to do:

1. Run *Lutris.*
1. Right-click the *Fate/stay night* entry.
1. Click the *Show logs* menu item.
1. Copy the contents of the displayed log to the clipboard.
1. [Paste those contents into a new
   issue of our issue tracker](https://github.com/leycec/fsnrnue/issues/new).

We'll get you sorted right out. Promise.

## Authors

Authoritative credit for the Ultimate Edition and bundled patches goes entirely
to the [Beast's Lair fandom](http://forums.nrvnqsr.com) – notably:

* Project leads:
  * **Jacktheinfinite101.**
  * **Quibi.**
  * **Kotonoha.**
* The Cast:
  * **Jacktheinfinite101:** Lead editor, programming, some image editing.
  * **Quibi:** Lead programmer, installer creation.
  * **Koto:** Lead translator, text editing, some image editing.
  * **Hintay:** Additional programming.
  * **Anonamous:** Additional programming.
  * **uyjulian:** Krkrz development.
  * **Waku Waku:** Lead image editor, programming consultant, PS2 resources,
    legacy project.
  * **ニサンカタンソ:** Additional programming.
  * **NM64:** Audio editing, beta testing, media assets.
  * **SmilingWolf:** Upscaled image assets.
  * **Hyarion:** Initial translation of Fate H alts.
  * **MeruP:** Programming.
  * **Terrafire:** Script comparisons.
  * **Dallas Hickan:** Additional image editing.
  * **GameCreater32:** Custom voice replay icons, supplemental tools.
  * **Commander Rase:** Beta Testing.
  * **Thryfe:** Beta Testing.
  * **Inuhanyou:** Beta Testing.
  * **SkitZoFrenic:** Beta Testing.
  * **Ownsin:** Beta Testing.
  * **UnlimitedBladeWorks:** Beta Testing.
  * **Taka-jun, ArchDemon, Tjm, and puKKa from Mirror Moon:** Original
    translation.
  * **bishopcruz and Annonymous:** First H uncensor patch.
  * **Himeros and Belldandy100:** Second H uncensor patch.
  * **[/u/dumbyoyo](https://www.reddit.com/user/dumbyoyo):** Keyboard
    shortcuts.
  * Special thanks to [any other BL members](http://forums.nrvnqsr.com) who
    helped out.

This Linux support's for you, stalwart Nasuverse heroes.

## See Also

If you enjoy this, you might also enjoy:

* [*Ao no Kanata no Four Rhythm* (Aokana)… for Linux!][leycec-aokana], a suite
  of [Lutris installers][lutris] automating patching, installation, and
  execution for the fan-produced native Linux port of the [shounen sports
  chuunibyou][chuuni] visual novel *[Aokana][nekonyan-aokana]*.
* [*The Legend of Heroes: Trails of…* for Linux!][leycec-kiseki], [Lutris
  installers][lutris] automating patching and execution of fully translated and
  voiced [SoraVoice][kiseki-soravoice] variants of the [legendary *Kiseki*
  (i.e., *Trails*, *Legend of Heroes*,『英雄伝説 …の軌跡』) Japanese
  role-playing franchise][kiseki].

[beasts-lair]: https://forums.nrvnqsr.com
[chuuni]: https://forums.fuwanovel.net/topic/1820-chuuni-what-is-this-genre
[dxvk]: https://github.com/doitsujin/dxvk
[dxvk-releases]: https://github.com/doitsujin/dxvk/releases
[dxvk-1.9.1]: https://github.com/doitsujin/dxvk/releases/download/v1.9.1/dxvk-1.9.1.tar.gz
[kiseki]: https://en.wikipedia.org/wiki/Trails_(series)
[kiseki-soravoice]: https://github.com/ZhenjianYang/SoraVoice
[installer-local]: /lutris/fate-stay-night-realta-nua-ultimate-edition.yml
[installer-remote]: https://leycec.github.io/fsnrnue/lutris/installer_redirect.html
[issue-tracker]: https://github.com/leycec/fsnrnue/issues
[leycec-aokana]: https://github.com/leycec/aokana-linux
[leycec-kiseki]: https://github.com/leycec/kiseki-linux
[lutris]: https://lutris.net
[lutris-vulkan-requirements]: https://github.com/lutris/docs/blob/master/HowToDXVK.md
[lutris-vulkan-install]: https://github.com/lutris/docs/blob/master/InstallingDrivers.md
[lutris-dxvk-video]: https://youtu.be/X6Vk_J3p2KA
[nekonyan-aokana]: https://nekonyansoft.com/shop/product/22
[patches-mediafire]: https://www.mediafire.com/file/047tv8akannrti3/patch.zip/file
[playonmac]: https://www.playonmac.com
[releases]: https://github.com/leycec/fsnrnue/releases
[ultimate-bl]: https://forums.nrvnqsr.com/showthread.php/8229
[ultimate-lutris]: https://lutris.net/games/fatestay-night
[unix-bash]: https://en.wikipedia.org/wiki/Bash_(Unix_shell)
[unix-bourne]: https://en.wikipedia.org/wiki/Bourne_shell
[unix-zsh]: https://en.wikipedia.org/wiki/Z_shell
[vulkan]: https://en.wikipedia.org/wiki/Vulkan_(API)
