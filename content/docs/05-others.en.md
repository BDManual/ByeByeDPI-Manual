---
title: Other apps
weight: 8
---

## Other DPI Bypass Options

> [!CAUTION]
> Use any of these solutions at your own risk. The authors of this manual are not responsible for any consequences or potential harm caused by using the software mentioned here.

> [!TIP]
> ByeDPI or zapret? If you want devices on your local network to connect to your computer, use ByeDPI and follow the [instructions](features.en.md#distribute) on how to grant access to ByeByeDPI — the steps are almost the same.

### Android

#### Magisk Modules for Android (root required)

- [ZDT&D Magisk Module](https://github.com/GAME-OVER-op/ZDT-D) by GAME-OVER-op
- [zapret-magisk](https://github.com/ImMALWARE/zapret-magisk) by ImMALWARE
- [zaprett](https://github.com/egor-white/zaprett) by egor-white and the companion [zaprett-app](https://github.com/CherretGit/zaprett-app) by CherretGit

### Windows

#### zapret Builds

- [zapret-discord-youtube](https://github.com/Flowseal/zapret-discord-youtube) — zapret build by Flowseal (a simple, straightforward solution)
#### GUI Applications

- [goodbyeDPI-UI](https://github.com/Storik4pro/goodbyeDPI-UI) by Storik4pro — a frontend that works with zapret, ByeDPI, GoodbyeDPI, and SpoofDPI
- [ByeDPI Manager](https://github.com/romanvht/bdmanager) by romanvht — a small utility that simplifies using ByeDPI on Windows (compatible with some Windows 7 versions)

#### Original Utilities

- [zapret](https://github.com/bol-van/zapret) by bol-van
- [ByeDPI](https://github.com/hufrea/byedpi) by hufrea — theoretically, the version [byedpi-x86-cygwin.zip](https://github.com/hufrea/byedpi/issues/219#issuecomment-2559707231) can even run on Windows XP

#### Instructions for Original Utilities

> [!CAUTION]
> ByeDPI does not include automatic strategy selection — you need to find a working strategy yourself (for example, by searching in [ByeByeDPI](https://github.com/romanvht/ByeByeDPI) or using [ByeDPI Manager](https://github.com/romanvht/ByeDPIManager)).

- [zapret](https://github.com/bol-van/zapret-win-bundle?tab=readme-ov-file#quick-start)
- [ByeDPI](byedpi-guide-windows.en.md)

### Linux

##### Scripts for Automatic Installation

> [!CAUTION]
> These scripts are not recommended for general use. It is better to customize the original utilities yourself.

- [zapret.installer](https://github.com/Snowy-Fluffy/zapret.installer) by Snowy-Fluffy
- [zapret-discord-youtube-linux](https://github.com/Sergeydigl3/zapret-discord-youtube-linux) by Sergeydigl3
- [zapret4rocket](https://github.com/IndeecFOX/zapret4rocket) by IndeecFOX
- [Byedpi-Setup](https://github.com/fatyzzz/Byedpi-Setup) by fatyzzz

#### Original Utilities

- [zapret](https://github.com/bol-van/zapret) by bol-van
- [zapret in container](https://github.com/vernette/ss-zapret) with Shadowsocks and SOCKS5 by vernette
- [ByeDPI](https://github.com/hufrea/byedpi) by hufrea
- [ByeDPI container](https://github.com/hufrea/byedpi/tree/main/dist/docker) (official)
- [ByeDPI container](https://hub.docker.com/r/tazihad/byedpi) (unofficial) by tazihad
- [youtubeUnblock](https://github.com/Waujito/youtubeUnblock) by Waujito
  
#### Instructions for Original Utilities

> [!CAUTION]
> ByeDPI does not include automatic strategy selection — you need to find a working strategy yourself (for example, by searching in [ByeByeDPI](https://github.com/romanvht/ByeByeDPI) or using [ByeDPI Manager](https://github.com/romanvht/ByeDPIManager)).

- [zapret](https://github.com/bol-van/zapret/blob/master/docs/readme.en.md#desktop-linux-system)
- [ByeDPI](https://github.com/hufrea/byedpi/tree/main/dist/linux)

### On Router

#### OpenWrt

- [Original zapret ](https://github.com/bol-van/zapret/blob/master/docs/readme.en.md#openwrt)
- [zapret-openwrt](https://github.com/remittor/zapret-openwrt) — zapret with web interface
- [nfqws](https://github.com/Anonym-tsk/nfqws-keenetic) — a program based on zapret, with instructions for Keenetic, OpenWrt, Netcraze, and Padavan
- [ByeDPI for OpenWrt](https://github.com/DPITrickster/ByeDPI-OpenWrt)
- [ByeDPI + Redsocks guide](https://habr.com/ru/articles/856312/)
- [youtubeUnblock on OpenWrt](https://github.com/Waujito/youtubeUnblock)

> [!TIP]
> You can use the [ByeDPI package](https://github.com/DPITrickster/ByeDPI-OpenWrt) as a custom outbound proxy in [podkop](https://github.com/itdoginfo/podkop) to control traffic via sign-box. The guide can be read [here](https://github.com/StressOzz/Podkop-ByeDPI-OpenWRT/blob/main/readme.en.md).

#### Keenetic

- [nfqws](https://github.com/Anonym-tsk/nfqws-keenetic) — zapret-based program with instructions for Keenetic, OpenWrt, Netcraze, Padavan
- [nfqws guide on Habr](https://habr.com/ru/articles/834826/) — instructions for Keenetic

#### MikroTik

- [ByeDPI article with instructions](https://habr.com/ru/articles/838452/)
- [Containers](https://hub.docker.com/u/wiktorbgu) with tpws from zapret and ByeDPI (note: tpws does not support UDP)

### On a Home Server (always-on device)

- You can connect to ByeDPI deployed on your PC
- [Can connect](features.en.md#distribute) to a phone running ByeByeDPI
- [ByeDPI on single-board computers](https://habr.com/ru/articles/870254/)
- [youtubeUnblock on single-board computers](https://habr.com/ru/articles/871460/)
- [zapret in container](https://github.com/vernette/ss-zapret) with Shadowsocks and SOCKS5
- [zapret on single-board computers](https://habr.com/ru/articles/833508/)
- [ByeDPI container](https://github.com/hufrea/byedpi/tree/main/dist/docker) (official)
- [ByeDPI container](https://hub.docker.com/r/tazihad/byedpi) (unofficial)
- [ByeDPI on Synology](https://bafista.ru/ustanovka-byedpi-v-kontejner-docker-na-synology/) or [ByeDPI on TerraMaster](https://bafista.ru/ustanovka-byedpi-v-kontejner-docker-na-terramaster/)

### Mac

> [!CAUTION]
> Follow the instructions at your own risk!

> [!TIP]
> Setting up ByeDPI is easier on macOS — both container and native installation versions are available.

- [ByeDPI](https://github.com/hufrea/byedpi/blob/main/dist/bsd/README.md) by hufrea
- [zapret](https://github.com/bol-van/zapret/blob/master/docs/bsd.md#macos) by bol-van

#### ByeDPI Containers

- [ByeDPI container](https://github.com/hufrea/byedpi/tree/main/dist/docker) (official)
- [ByeDPI container](https://hub.docker.com/r/tazihad/byedpi) (unofficial) by tazihad

#### Native Installation

Follow these [instructions](https://github.com/hufrea/byedpi/tree/main/dist/linux) for installing **ByeDPI on Linux** as a reference.

Since the author does not have a macOS device, the following steps for macOS are **suggested but not tested**:

1. Install Xcode Command Line Tools

```
xcode-select --install
```

2.  Install Homebrew (macOS package manager)

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

3. Install Required Tools

```
brew install git gcc make binutils
```


4. Clone the Repository

```
git clone https://github.com/hufrea/byedpi.git
```

5. Navigate to the Directory

```
cd byedpi
```

6. Compile the Program

```
make
```

7. Make `ciadpi` Executable

```
chmod +x ciadpi
```

8. Run the Program

> [!WARNING]
> Do **not** include square brackets `[]` in the command.
> If the default strategy doesn't work, try others from the [list](ALL.TXT).

```
./ciadpi [strategy_used_on_your_phone_in_the_ByeByeDPI_app]
```

9. Test with Firefox

To check if ByeDPI is working, install [Firefox for macOS](https://www.mozilla.org/en-US/firefox/mac/) and configure it to use the SOCKS5 proxy provided by ByeDPI.  
If successful, you can use other apps like FoXray, [V2RayXS](https://github.com/tzmax/V2RayXS), or [nekoray](https://github.com/Mahdi-zarei/nekoray).

> [!CAUTION]
> Installation is now complete.
> For future runs, you must specify the full path to the executable, e.g.:
> `/Users/you/apps/byedpi/ciadpi strategy`

Adding ByeDPI to macOS Autorun

1. Create a LaunchAgent `.plist` File

```
nano ~/Library/LaunchAgents/com.user.ciadpi.plist
```

2. Paste and Modify the Following Template
  
>Replace `/FULL/PATH/TO/ciadpi` with the **full path** to the `ciadpi` executable, and replace the `-argumentX` lines with your actual strategy arguments.

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN"
  "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
  <!-- Unique service ID -->
  <key>Label</key>
  <string>com.user.ciadpi</string>

  <!-- Program with arguments -->
  <key>ProgramArguments</key>
  <array>
    <string>/FULL/PATH/TO/ciadpi</string>
    <string>-argument1 (strategy argument is the hyphenated part, e.g. -Ku)</string>
    <string>-argument2</string>
    <!-- Add more arguments as needed -->
  </array>

  <!-- Run at login -->
  <key>RunAtLoad</key>
  <true/>

  <!-- Restart automatically if it crashes -->
  <key>KeepAlive</key>
  <true/>
</dict>
</plist>
```

3. Set Permissions and Load the Service

```
chmod 644 ~/Library/LaunchAgents/com.user.ciadpi.plist
```

```
launchctl load ~/Library/LaunchAgents/com.user.ciadpi.plist
```

```
launchctl start com.user.ciadpi
```

4. To Unload or Remove

```
launchctl unload ~/Library/LaunchAgents/com.user.ciadpi.plist
```

```
rm ~/Library/LaunchAgents/com.user.ciadpi.plist
```

## iOS

On iOS, there is [Rumble](https://iklassika.ru/app.php?id=5833) — apparently, it is byedpi + hev-socks5-tunnel. The source code is available [here](https://github.com/RumbleOrg/Rumble). This application can only be installed if you have a developer certificate.

> One known issue is that the connect button sometimes fails; deleting the VPN application profile helps.

> [!CAUTION]
> There is no reliable information about the security of **Rumble**. Install the application at your own risk.

### Options for iOS users:

- Use a VPN — simple and requires no technical knowledge.
- Share access from an Android device running ByeByeDPI. See [this guide](features.en.md#sharing-internet-with-byebyedpi-local-proxy) for details.
- Use [router-based DPI bypass methods](#other-router)
- Use [home server solutions](#other-home-server) (e.g. a PC running ByeDPI).

> [!NOTE]
> If your ISP provides a static (white) IP, you can set up a VPN tunnel to your router and access the internet from your phone through the bypass-enabled network.

## “Standard Editor” - Is It Necessary

Creating a custom strategy (which is what the graphical editor is for) requires a solid understanding of how networks work and how each setting affects DPI bypass.  
This is all thoroughly explained in the [official documentation](https://github.com/hufrea/byedpi).

Anyone who has read and understood the documentation will not need the graphical editor — it only exposes a limited set of options and hides many arguments.

The “standard editor” is **not recommended**. Random guessing is a bad approach.

## Universal Strategy

If you're struggling to get things working, just use a VPN.
