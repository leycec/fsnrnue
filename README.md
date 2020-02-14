Fate/stay night [Réalta Nua] Ultimate Edition
=============================================

This repository [unofficially hosts GitHub-managed downloads][releases] for the
[Fate/stay night \[Réalta Nua\] Ultimate
Edition](forums.nrvnqsr.com/showthread.php/8229) – a pair of third-party 32-
and 64-bit Windows installers automating both the installation and patching of
the [Réalta
Nua](https://typemoon.fandom.com/wiki/Fate/stay_night#R.C3.A9alta_Nua) variant
of the seminal Japanese visual novel [*Fate/stay
night*](https://typemoon.fandom.com/wiki/Fate/stay_night).

## but what?

[Current releases][releases] include:

* **[Linux Lutris installer][installer-remote].**
* **[64-bit Windows
  installer](https://github.com/leycec/fsnrnue/releases/download/2019.03.19/fsnrnue-2019.03.19-64.zip).**
* **[32-bit Windows
  installer](https://github.com/leycec/fsnrnue/releases/download/2019.03.19/fsnrnue-2019.03.19-32.zip).**

## but how?

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
   * **Linux:**
     1. _(Recommended)_ **[Install *Wine
        Staging*](https://wiki.winehq.org/Wine-Staging).** See also
        instructions for:
        * [Debian-based distributions (e.g.,
          Ubuntu)](https://www.linuxuprising.com/2019/09/how-to-install-wine-staging-development.html).
     1. **[Install *Lutris*][lutris].**
     1. **[Click this *Lutris installer link*][installer-remote],** which
        automates the installation process by both downloading *and* running
        this installer with [Lutris][lutris]. Command-line aficionados may also
        manually run this installer under the command line:
        1. [Download this YAML file][installer-local].
        1. Open a terminal to the directory containing this YAML file.
        1. Copy-and-paste this command into the terminal:

               lutris -i fate-stay-night-realta-nua-ultimate-edition.yml

   * **Windows,** follow the [official Ultimate Edition
     instructions](forums.nrvnqsr.com/showthread.php/8229).
   * **macOS is currently unsupported,** as [Lutris][lutris] is currently
     Linux-specific. In theory, porting our [Lutris-specific
     installer][installer-local] to [PlayOnMac][playonmac]
     *should* be feasible if non-trivial. If someone does so, please submit an
     [issue](https://github.com/leycec/fsnrnue/issues) or [pull
     request](https://github.com/leycec/fsnrnue/pulls) and we'll update these
     instructions accordingly.

We strongly recommend:

* *Not* installing the **OP Patch** (i.e., the patch adding opening movies
  bundled with the PS Vita version) during the Ultimate Edition installer.
  These movies contain heavy spoilers – particularly for Heaven's Feel, the
  final route and grand finale. All remaining patches are spoiler-free.
* *Not* enabling the *Display* → *Aspect Ratio* → *Wide* option, which
  currently suffers a variety of unresolved issues.

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

## but who?

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


[lutris]:    https://lutris.net
[playonmac]: https://www.playonmac.com
[releases]:  https://github.com/leycec/fsnrnue/releases
[installer-local]:  /lutris/fate-stay-night-realta-nua-ultimate-edition.yml
[installer-remote]: /lutris/fate-stay-night-realta-nua-ultimate-edition.yml
