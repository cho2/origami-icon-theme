<p align="center">
  <img src="https://raw.githubusercontent.com/LelCP/origami-icon-theme/master/preview.png" alt="preview"/>
</p>

Origami icon theme is available in two variants:

 - Origami (for Geeko / Geeko Darker)
 - Origami-dark (for Geeko Dark)

## Installation on openSUSE

`sudo zypper in origami-icon-theme`

## Installation

`sudo make install` 

## Hardcoded icons

Some software uses an absolute path instead of the icon name in a .desktop file or in the source code which makes them unthemable.

### Hardcoded application icons

To deal with hardcoded application icons we recommend using [hardcode-fixer](https://github.com/Foggalong/hardcode-fixer). Origami supports most of the applications in the [list](https://github.com/Foggalong/hardcode-fixer/blob/master/tofix.csv). If [hardcode-fixer](https://github.com/Foggalong/hardcode-fixer) doesn't support your favorite app yet, please open an issue [here](https://github.com/Foggalong/hardcode-fixer/issues) or edit your .desktop file manually.

### Hardcoded tray icons

To fix hardcoded tray icons Origami supports [Hardcode-Tray](https://github.com/bil-elmoussaoui/Hardcode-Tray) script. A list of supported applications is available [here](https://github.com/bil-elmoussaoui/Hardcode-Tray/tree/master/data/database).

**NOTE:** To get Origami to work right with Hardcode-Tray, use the hardcode-tray option `--conversion-tool RSVGConvert`:

```
sudo -E hardcode-tray --conversion-tool RSVGConvert --size 22 --theme Origami
```

**Size recommendations:**
- Unity 22px
- KDE 22px
- GNOME 16px ([see](https://github.com/LelCP/origami-icon-theme#manual-fixes) for more info)
- XFCE 22px ([see](https://github.com/LelCP/origami-icon-theme#manual-fixes) for more info)
- Pantheon 24px
- Cinnamon 16px


![hardcode-tray](http://i.imgur.com/6hFm6aj.png)

**BUG on KDE with libappindicator**: Some applications have wrong rendering by default on KDE. For solve this run application with Unity environment option.

For example:
```
XDG_CURRENT_DESKTOP=Unity wire-desktop

```
See more info [here](https://bugs.kde.org/show_bug.cgi?id=366062) and please vote for this bug.

## KDE colorscheme

Support for monochrome icons for KDE colorscheme is now available:
- Origami - for dark plasma theme & light color scheme
- Origami Dark - for dark plasma theme & color scheme
- Origami Light - for light plasma theme & color scheme

![kde-color-scheme](http://i.imgur.com/oM1qhQH.png)

**NOTE:** Non-KDE apps don't support KDE colorscheme on the system tray, but you can replace color manually.

## Manual fixes

<details>
![Cinnamon Arc-Dark theme fix](http://i.imgur.com/XXejgtD.png)

To deal with blurred panel icons, increase the panel size up to 30px in `Systems Settings` → `Panel` (see [screenshot](https://i.imgur.com/oToRBYv.png)).
</details>

<details>
<summary>For Xfce users</summary>

Here are a few recommendations for Xfce users.

#### Thunar File Manager

Go to `Edit` → `Preferences...`. Click on `Side Pane` tab. Under `Side Pane`, look for `Icon Size` and set to `Very Small`.

![thunar-prefecences](http://i.imgur.com/Iu1TIEa.png)

#### Notification Area

Go to `Settings Manager` → `Panel` → `Items` tab. Select `Notification Area` item and click on `Edit currently selected item` button. Under `Appearance` set the following options:

- Set `Maximum icon size (px)` to `24`
- Uncheck `Show frame`

![xfce4-notification-area](http://i.imgur.com/MopCZBZ.png)
</details>

<details>
<summary>For elementary/Pantheon users</summary>
- With light wallpaper we recommend use non-transparency wingpanel:

```
gsettings set org.pantheon.desktop.wingpanel use-transparency false
```

</details>

## Icon request

- Application name
- Icon name (see desktop-file option **Icon** on `/usr/share/applications`)
- Original icon image
- Small description and/or a link to the official webpage

## Contribute

We welcome user contributions. If you don't know where to start, we've compiled a list of things we would like to see in your pull request:

- new icons for missing applications
- symbolic links to an existing icon
- resolving open issues
- spelling, grammar, phrasing
- improvements to our scripts

Inside [tools/work](tools/work) you will find a step-by-step guide, an environment, and tools that will help you:

- [create a new icon](tools/work#create-a-new-icon) from template
- [make a symlink to an existing icon](tools/work#make-symlinks-to-an-existing-icon)
- [edit an existing icon](tools/work#edit-an-existing-icon)
- convert your icon to all variants of the theme

We are waiting for your pull requests and would love to see this icon theme become as complete as possible.

## Donate

Donate to awesome people over on Papirus for creating base of this icon theme :)

<span class="paypal"><a href="https://www.paypal.me/varlesh" title="Donate to Papirus project using Paypal"><img src="https://www.paypalobjects.com/webstatic/mktg/Logo/pp-logo-100px.png" alt="PayPal donate button" /></a></span>

BTC: `1HwE62Zb8PyyY1XAR6Ykweix2ht8NAjvf5`

## License

GNU LGPL v3.0
