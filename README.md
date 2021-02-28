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
     1. _(Recommended)_ **[Install *Wine
        Staging*](https://wiki.winehq.org/Wine-Staging).** See also
        instructions for:
        * [Debian-based distributions (e.g.,
          Ubuntu)](https://www.linuxuprising.com/2019/09/how-to-install-wine-staging-development.html).
     1. **[Install *Lutris*][lutris].**
     1. **Install _Fate/stay night \[Réalta Nua\] Ultimate Edition_** with
        either:
        * *(Recommended)* **[Our one-click installer][installer-remote],**
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

#### That's what I'm seeing, I think?

**Great!** Well, not great – but things could be worse. You could be Shiro in
any of the Dead Ends you're about to compulsively read just to collect all of
the Taiga Dojo stamps just to unlock a ridiculous hot springs bath scene.
<sup>Totally worth it.</sup>

So, we've confirmed the Ultimate Edition installer failed to properly download
one or more patches for you. These patches are locally corrupt and *must* be
[manually redownloaded from Google Drive links listed under the **Mandatory
patches** section of the original release notes for the Ultimate
Edition][ultimate-bl] into the
`fate-stay-night-realta-nua-ultimate-edition/drive_c/Program Files/Fate／stay
night[Realta Nua] Ultimate Edition/` subdirectory to which the Ultimate Edition
previously installed itself, overwriting each existing corrupt patch.

If you're unsure which corrupt patches need to be redownloaded, either blindly
redownload *all* of them or:

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

#### That's also not what I'm seeing.

…that's not even a question. You can tell because there's no question mark.

#### I'm seeing an error at "initialize.tjs(245)"?

Are you receiving an error resembling `"==== An exception occured at
initialize.tjs(245)[(top level script) global], VM ip = 840 ===="`? If yes,
then we're all on the same page, which is nice.

Did you also install the optional Vita patch? If:

* **Yes,** then [please try reinstalling *without* that
  patch](https://github.com/leycec/fsnrnue/issues/9).
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

#### I see something about Vulkan and `dxvk` in those logs, I think?

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
* The `"info: Required Vulkan extension VK_KHR_surface not supported"` line is
  where your troubles start. **Your [Vulkan][vulkan] installation is broken.**
  That's bad, because it means you won't be able to run any GPU-accelerated
  [Vulkan][vulkan] games. Thankfully, *Fate/stay night* is so old that it runs
  on decades-old potato PCs manufactured by RadioShack and doesn't really
  benefit from GPU acceleration at all.

You have two options here:

* (*Recommended*) **Disable [Vulkan][vulkan] for *Fate/stay night*.** This is
  the easy way:
  1. Run *Lutris*.
  1. Right-click the *Fate/stay night* entry.
  1. Click the *Configure* menu item.
  1. Click the *Runner options* tab.
  1. Disable the *Enable DXVK/VKD3D* setting.
  1. You're done. *Praise Ilya!*
* **Fix your broken [Vulkan][vulkan] and [DXVK][dxvk] installation.** This is
  the hard way, but you probably want to do this eventually *anyway*.
  Instructions for properly installing and configuring [Vulkan][vulkan] and
  [DXVK][dxvk] vary by platform. For example, users on Arch-based Linux distros
  should:
  1. Follow [the Vulkan installation instructions at the Arch
     Wiki](https://wiki.archlinux.org/index.php/Vulkan#Installation).
  1. Follow [the Wine installation instructions at the Arch
     Wiki](https://wiki.archlinux.org/index.php/wine#Installation). **Note:
     install `wine-staging` rather than `wine`.** Always use Wine Staging,
     which is the bleeding-edge version of Wine that provides [DXVK][dxvk].
     Never use standard Wine, which is the obsolete version of Wine that
     provides literally nothing.
  1. Watch [this YouTube video walking you through DXVK configuration under
     Lutris with Wine
     Staging](https://forums.lutris.net/t/how-to-setup-dxvk-on-lutris/1704).

When in doubt, just disable [Vulkan][vulkan] and [DXVK][dxvk].

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
[kiseki]: https://en.wikipedia.org/wiki/Trails_(series)
[kiseki-soravoice]: https://github.com/ZhenjianYang/SoraVoice
[installer-local]: /lutris/fate-stay-night-realta-nua-ultimate-edition.yml
[installer-remote]: https://leycec.github.io/fsnrnue/lutris/installer_redirect.html
[leycec-aokana]: https://github.com/leycec/aokana-linux
[leycec-kiseki]:  https://github.com/leycec/kiseki-linux
[lutris]: https://lutris.net
[nekonyan-aokana]: https://nekonyansoft.com/shop/product/22
[playonmac]: https://www.playonmac.com
[releases]: https://github.com/leycec/fsnrnue/releases
[ultimate-bl]: https://forums.nrvnqsr.com/showthread.php/8229
[ultimate-lutris]: https://lutris.net/games/fatestay-night
[vulkan]: https://en.wikipedia.org/wiki/Vulkan_(API)
