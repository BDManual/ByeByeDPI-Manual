---
title: Features
weight: 3
---

## Whitelisting and blacklisting

*White list*: selected applications will route traffic through ByeByeDPI, while all others will bypass it.
**Black list** : selected applications will NOT route traffic through ByeByeDPI, while all others will.

> [!TIP]
> Why are these lists important? Some apps (like Telegram) may not function properly or may not work at all when DPI bypass is applied.
> Additionally, the less traffic that passes through ByeByeDPI, the less battery power will be consumed.
> On some TVs or set-top boxes, internet access may not work at all without whitelisting.

## Command line editor

<img src="/images/features-1.jpg" width="200">

The Command Line Editor section contains a list of Command Line Arguments (strategies) that have been applied previously.

<img src="/images/features-2.jpg" width="200">

> [!WARNING]
> Be careful: the list length is limited. If the list overflows, the oldest strategies will be removed.

Clicking on a strategy will open a menu with the following options:

<img src="/images/features-3.jpg" width="200">

- **Apply action**: applies the command (sets it as the current Command Line Argument).

   <img src="/images/features-4.jpg" width="200">

- **Pin action**: pins the strategy to the top of the list.

   <img src="/images/features-5.jpg" width="200">

- **Rename action**: allows you to rename the strategy.

   <img src="/images/features-6.jpg" width="200">

- **Copy action**: copies the strategy to the clipboard.
- **Delete action**: removes the strategy from the list (history).

## Display all commands in the test as clickable

> [!TIP]
> What is this setting useful for?
> If you don’t want to wait for the selection to finish because the test has already shown high (50% or more) percentages for several strategies, or if you’re experiencing a selection failure but some strategies in the test show high (50% or more) percentages, this setting can help.

This option can be found in the **Proxy Test (Beta)** settings.

Go to **"Proxy Test (Beta)"**[^1]

 <img src="/images/settings-4.jpg" width="200">

- Open **Proxy Test Settings** (gear icon in the top-right).

   <img src="/images/settings-5.jpg" width="200">

- Activate the toggle **Display all commands in the test as clickable**

   <img src="/images/features-7.jpg" width="200">

Now, even if the Proxy Test is interrupted, the list of strategies will be displayed as clickable.

<img src="/images/features-9.jpg" width="200">

Clicking on a strategy will open a menu with these options:

<img src="/images/features-10.jpg" width="200">

- **Apply action**: applies the command (sets it as the current Command Line Argument).

   <img src="/images/features-4.jpg" width="200">

- **Copy action**: copies the strategy to the clipboard.

## Your list of commands (strategies)

> [!IMPORTANT]
> You should use your custom list of strategies only if the auto-selection results in low percentages, and you see no strategies with the highest percentages hitting the ceiling (for more on this, see [here](problems.en.md#equally-low-percentage)).

If you’re unsatisfied with the results of the auto-selection and have found commands (strategies) elsewhere, but checking each one manually is tedious, you can follow these steps:

- Go to **"Proxy Test (Beta)"**[^1]

 <img src="/images/settings-4.jpg" width="200">

- Open **Proxy Test Settings** (gear icon in the top-right).

   <img src="/images/settings-5.jpg" width="200">

- Activate the switch **Use custom command lists**

   <img src="/images/features-11.jpg" width="200">

- Tap on **Command lists**

   <img src="/images/features-12.jpg" width="200">

- A window will open

   <img src="/images/features-13.jpg" width="200">

- In this window you should enter your list of commands (strategies)

> [!IMPORTANT]
> Each new strategy must be on a new line. Commands (strategies) cannot be separated by commas, periods, or any other symbols. They should only be separated by new lines.

- After entering your strategies, press **OK**.

   <img src="/images/features-14.jpg" width="200">

- Return to **Proxy Test (Beta)** and click on the ‘Start Testing’ button.

 <img src="/images/settings-10.jpg" width="200">

- After that, it will start checking the strategies you have inserted into the list

   <img src="/images/features-15.jpg" width="200">

- Wait for the selection to complete, then proceed with the [standard setup](start.en.md#setting). If there is a crash, the solution is [here](problems.en.md#crash-proxy-test).

## Exporting and importing settings

To export or import settings, go to the main settings in **ByeByeDPI** (gear icon in the top-right):

   <img src="/images/settings-2.jpg" width="200">

- Click on the three dots in the top-right corner.

   <img src="/images/features-16.jpg" width="200">

> [!WARNING]
> You cannot export settings from version 1.4.1 or older and import them into version 1.4.2 or newer.

- Select **Export** or **Import**, depending on your needs (save settings or load settings). Settings are exported in `json` format. When importing, you will need to specify the file.

   <img src="/images/features-17.jpg" width="200">

## Methods of launching

### Classic launch

The classic way to launch the application is by pressing the **Connect** button.

 <img src="/images/features-18.jpg" width="200">

> [!TIP]
> Some may find this method inconvenient, so there are other options available.

### Launching through the control centre

- Open your **Control Centre** and find **Edit** (or similar).

   <img src="/images/features-19.jpg" width="200">

- You will see inactive elements. Find ByeByeDPI among them, click, and drag it to the main elements

   <img src="/images/features-20.jpg" width="200">

- Don’t forget to save your changes.

   <img src="/images/features-21.jpg" width="200">

- You can now launch ByeByeDPI directly from the Control Centre.

   <img src="/images/features-64.jpg" width="200">

### Context menu

If you press the ByeByeDPI icon, a context menu will appear, allowing you to quickly toggle the application on and off.

<img src="/images/features-22.jpg" width="500">

### Widget

By default, the application does not include widget functionality. However, it’s possible to create a widget:

- Some launchers allow you to create widgets from quick menu items.

   <img src="/images/features-30.jpg" width="500">

- If your launcher doesn’t support this, you can use the `Shortcut Maker` (or similar) app.

> [!IMPORTANT]
> Use **ToggleActivity** for the widget.

## VPN and Proxy modes

> [!CAUTION]
> **Proxy mode** can only be used if you are connecting through a proxy client.

> [!TIP]
> Why use Proxy mode?
> Proxy mode is useful if you want to run other applications in VPN mode simultaneously (e.g., AdGuard, etc.) or if you want to use a proxy client (e.g., ZeroOmega extension for point-proxying sites in the browser).

In **VPN mode**, traffic is **forced** through ByeByeDPI. In **Proxy mode**, a local **SOCKS proxy** is created.

The local proxy is also created in VPN mode, and you can connect to it using a proxy client when ByeByeDPI is in _whitelist_ mode.

The proxy is raised in any mode, but in VPN mode the client of this proxy is ByeByeDPI.

Schematic representation of VPN-mode operation (HevSocks5Tunnel and ByeByeDPI direct traffic to the Internet):

<img src="/images/Pasted image 20250227230752.png" width="500">

In Proxy mode, the user needs to connect the proxy client itself to a proxy to access the Internet:

<img src="/images/Pasted image 20250227231212.png" width="500">

### HTTP-proxy mode

This mode will proxy HTTPS or any TCP traffic other than HTTP.

By default, ByeByeDPI runs a local SOCKS proxy. Some proxy clients cannot work with this protocol. If needed, you can activate **HTTP-proxy mode** by enabling the HTTP proxy switch.

<img src="/images/features-31.jpg" width="500">

> [!NOTE]
> Another way to activate this mode is by using the `-G` or `--http-connect` arguments (these are interchangeable).
>
> Example strategy:
> `--http-connect -d1 -s0+s -d3+s -s6+s -d9+s -s12+s -d15+s -s20+s -d25+s -s30+s -d35+s -At,r,s -s1 -o1+s -s-1`

## Split routing for sites (domains)

> [!TIP]
> Why use split routing?
> DPI traversal can disrupt sites that function normally without it. For example: `mfa.gov.tr`.

### Native method

To make ByeByeDPI process only specific domains, add the `--hosts` (`-H`) argument to your strategy and list the domains you want:

```
# From ByeDPI documentation

-H, --hosts <file|:string>
    Limit the scope of parameters to a list of domains
    Domains must be separated by a new line or a space
```

### ‘Whitelist’ for domains

If you specify a host list before finalizing the group with (_-A_), the strategy for that group will only interact with domains in the list.

Example strategy:

```
-H:"roblox.com discord.com discord.gg" -o1+s -d3+s -a2
```

> [!NOTE]
> The brackets are necessary due to the peculiarities of the parsing mechanism.

> [!TIP]
> It is not necessary to use whitelisting in this mode.

### ‘Blacklist’ for domains

In some cases, you may need to restrict ByeByeDPI from processing traffic for specific domains, such as `mfa.gov.tr` and `geliyoo.com`. To prevent ByeByeDPI from processing these domains, add them to a separate group at the beginning of the strategy with `-H:"mfa.gov.tr geliyoo.com" -An`. In simple words, this part means: if the domain is `mfa.gov.tr` or `geliyoo.com` - do nothing. **It's important** not to forget _-A_ with the right parameter after the list.

Example strategy:

```
-H:"mfa.gov.tr geliyoo.com" -An -o1+s -d3+s -a2
```

---

> [!TIP]
> In the strategy, you can specify the path to the text file containing the domains. To do this, you need to give ByeByeDPI permission to access the files.
> The contents of the fake packages can be specified in the same way.

Example strategy:

`-Ku -a10 -An -Kt,h -H /storage/emulated/0/Documents/domain.txt -s1 -q1 -Art -f-1 --md5sig -r1+s -An`

### Browser extension

An alternative method for point-to-point routing is using a browser proxy extension. Here's an example using the `Firefox` browser with the `ZeroOmega--Proxy SwitchyOmega V3` extension installed, but you can use any similar extension and browser with extension support.

- First, activate proxy mode in ByeByeDPI **or** **remove the browser from the whitelist** in which you will install the extension.
- Install the extension and be sure to grant it permission to work in private windows (this is necessary for the proxy to function properly). Click the **Add** button.

   <img src="/images/features-32.jpg" width="200">

- Then, open the list of extensions and click on **ZeroOmega**.

   <img src="/images/features-33.jpg" width="200">

- Navigate to the options tab.

   <img src="/images/Pasted image 20250302113330.png" width="200">

- In the **Proxy** tab, configure the connection settings: protocol (ByeByeDPI's default is SOCKS5), the address and port of the proxy (which you can find in ByeByeDPI settings). For example:

```
Protocol: SOCKS5
Server: 127.0.0.1
Port: 1080
```

- After setting up the connection, don’t forget to apply the changes by clicking **Apply changes**.

   <img src="/images/Pasted image 20250302114111.png" width="200">

- Next, go to the **Auto Switch** tab and add **Switch rules**. For example, I added:

```
Condition Type: Host Wildcard
Condition Details: *.discord.com
Profile: proxy
```

- Remember to save the changes by clicking **Apply changes**.

   <img src="/images/features-36.jpg" width="200">

- Try accessing the desired resource. It **may not open** immediately. Change ZeroOmega’s mode to `auto switch` mode.

   <img src="/images/features-37.jpg" width="200">

   <img src="/images/features-38.jpg" width="200">

- Refresh the page to load the resource. For instance, if you open a video, it may not start playing immediately. In this case, go to the extension settings.

   <img src="/images/features-39.jpg" width="200">

- In `auto switch` mode, the extension will notify you if any domains cannot be reached.

   <img src="/images/features-40.jpg" width="200">

- Open the _failed resources_ tab, change their profile to **proxy**, and add them.

   <img src="/images/features-41.jpg" width="200">

-  After refreshing the page, everything should work.

   <img src="/images/features-42.jpg" width="200">

- In the settings, it now looks something like this:

   <img src="/images/features-43.jpg" width="200">

## Internet distribution with ByeByeDPI (local proxy)

Suppose you have an **iPhone** _(or another device on which you can install a proxy client)_ and an Android 6.0+ phone _(or another device running ByeByeDPI)_.

ByeByeDPI is installed on the Android device, and a working strategy is selected. On the **iPhone** _(or other device)_, install a proxy client that supports **SOCKS5** (for example, **Happ** is suitable for both iOS and Android).

To share access to ByeByeDPI, both devices _(you can connect more than one device, but for simplicity, let's assume it's just one device)_ must be on the same local network. You can either connect both devices to the same access point or share your phone’s access point. The main thing is that both devices are on the same local network.

Next, in the ByeByeDPI settings, set the address and port to `0.0.0.0` and `1080`.

> [!CAUTION]
> If you want Roblox (and other apps) to continue working on the device running ByeByeDPI, **do not activate Proxy mode**. Otherwise, you will need to install a proxy client on the device with ByeByeDPI as well. To understand why this happens and why you can still connect from another device even if ByeByeDPI is in VPN mode, read [here](#vpn-proxy).

<img src="/images/features-44.jpg" width="200">

<img src="/images/features-45.jpg" width="200">

Launch ByeByeDPI.

Afterward, determine the IP address of the device running ByeByeDPI in the local network. You can use the [Android Network Tools](https://github.com/stealthcopter/AndroidNetworkTools) application. When you enter this application, the ip address will be written:

<img src="/images/Pasted image 20250426111432.png" width="200">

The ip of the device can also be found in the network settings or by using the [Ning](https://github.com/csicar/Ning) app.

> [!TIP]
> For those in the know: If you will be connecting often, set a **static IP** for your phone.

Then, open the proxy client on the **iPhone** _(or other device)_. This example uses **Happ**.

> [!WARNING]
> There's no separate app tunneling on the iPhone. You will need to add your own routes.
> In some regions, such as Russia, the ability to connect to SOCKS proxies may have been removed from Happ (in that case, use another client).

To add a connection:

<img src="/images/features-46.jpg" width="200">

<img src="/images/features-47.jpg" width="200">

> [!IMPORTANT]
> **SOCKS5** or **SOCKS protocol** should be used
> NOT Shadowsocks.

<img src="/images/features-48.jpg" width="200">

Enter the IP of the device running ByeByeDPI (which you obtained using _Android Network Tools_) and the port specified in ByeByeDPI. After entering the details, be sure to save the changes.

> [!IMPORTANT]
> The proxy server that ByeByeDPI creates does not require a username or password, leave those fields blank in the proxy client.

<img src="/images/features-49.jpg" width="200">

If the proxy client has a test connection feature, use it.

<img src="/images/features-50.jpg" width="200">

> [!NOTE]
> If there is no response, there is no connection: ByeByeDPI may be turned off, incorrect data may be entered, or the devices may be on different networks.

Afterward, specify the applications that ByeByeDPI should work with on the **iPhone** _(or other device)_.

<img src="/images/features-51.jpg" width="200">

<img src="/images/features-52.jpg" width="200">

<img src="/images/features-53.jpg" width="200">

Once done, you can launch the app and start using Roblox.

<img src="/images/features-54.jpg" width="200">

Proxy Clients for Various Devices and Systems:

- **iPhone**: `Happ`, `FoXray`, `Shadowrocket`, `Sockswitch-Shadowsocks Client`, `Potatso Lite`
- **Windows**: you can use browser extensions, e.g. `ZeroOmega--Proxy SwitchyOmega V3` (the algorithm of setting [here](#extension) - the only difference: you need to enter not `127.0.0.1`, but ip of the device with ByeByeDPI running) or use applications: [nekoray](https://github.com/MatsuriDayo/nekoray/), proxifier, [proxifyre](https://github.com/wiresock/proxifyre), Happ, [sockscap64](https://www.sockscap64.com/homepage/) (for older Windows).
- **MacBook**: FoXray, [V2RayXS](https://github.com/tzmax/V2RayXS) (for old macbooks), [nekoray](https://github.com/Mahdi-zarei/nekoray).
- **Other Android devices**: `Happ`, [nekobox](https://github.com/MatsuriDayo/NekoBoxForAndroid), proxifier for Android, [SocksDroid](https://github.com/bndeff/socksdroid) (requires Android 5.0+), [SocksTun](https://github.com/heiher/sockstun), for older versions of Android ProxyDroid (root required).

## Autorun ByeByeDPI on application startup

There is no built-in feature to launch ByeByeDPI automatically when you start any application, and it’s not currently planned. However, you can achieve this functionality using the **MacroDroid** app.

> [!WARNING]
> Make sure to remove any restrictions on opening applications when running in the background.

The start/stop activity in ByeByeDPI is **ToggleActivity**.
It should look like this:

<img src="/images/features-55.jpg" width="400">

You can also create a condition, for example, if VPN is enabled and Discord is closed, **ToggleActivity** will be triggered.

<img src="/images/features-56.jpg" width="400">

## Settings for working with AdGuard

Switch ByeByeDPI to **Proxy mode**.

<img src="/images/features-58.jpg" width="200">

Add ByeByeDPI to AdGuard’s **exceptions** under the **Manage Applications** tab.
In AdGuard itself, go to the centre tab, and after that search for ByeByeDPI, and simply cut off its filtering.

<img src="/images/features-59.jpg" width="200">

After that go to settings -> filtering -> network -> proxy. Switch it on, and then enter the same proxy values that are specified in ByeByeDPI, necessarily in SOCKS5 mode.

<img src="/images/features-60.jpg" width="200">
<img src="/images/features-61.jpg" width="200">
<img src="/images/features-62.jpg" width="200">
<img src="/images/features-63.jpg" width="200">

Then, enable the proxy in AdGuard.

> [!WARNING]
> If AdGuard says "Failed to connect to proxy" when checking, it’s fine—**the proxy is actually working**!

> [!IMPORTANT]
> You may need to add ByeByeDPI to AdGuard's exceptions in another way:
> Go to AdGuard -> settings -> basic-> advanced-> advanced-> low-level settings-> excluded applications
> And add the ByeByeDPI application ID:
> `io.github.romanvht.byedpi`


## Unlock more services

Go to **Selection Settings**, disable the ‘Add the nearest GoogleVideo to testing’ option, and enable the ‘Use your domain list’ option. Insert your list of domains to test.

<img src="/images/features-65.jpg" width="200">

Afterward, search for the strategy [in a similar manner](start.en.md#setting) as before.

> [!WARNING]
> If all strategies show 0%, the resource is likely blocked by IP, and ByeByeDPI cannot help.

> [!TIP]
> Large sites and services may require many domains to function correctly.

For example, here are the domains for Discord:

```
dis.gd
discord.co
discord.com
discord.design
discord.dev
discord.gg
discord.gift
discord.gifts
discord.media
discord.new
discord.store
discord.tools
discord-activities.com
discordactivities.com
discordapp.com
discordapp.net
discordmerch.com
discordpartygames.com
discordsays.com
discordstatus.com
airhorn.solutions
airhornbot.com
bigbeans.solutions
watchanimeattheoffice.com
```

As you can see, Discord requires more than just `discord.com` to work properly.

For more domain lists, check this [repository](https://github.com/v2fly/domain-list-community) .

To identify domains used by a service, you can follow this [guide](https://itdog.info/analiziruem-trafik-i-opredelyaem-domeny-kotorye-ispolzuyut-sajty-i-prilozheniya/)(couldn't find one in English. If you know something, write in the issue) goes into detail about sniffing traffic on various devices and systems.
For Android, I recommend using **PCAPdroid**. For PC, you can use the browser's developer tools to inspect network traffic.

## Auto-update

The application does not implement an auto-update feature. To enable automatic updates for ByeByeDPI, use [Obtainium](https://github.com/ImranR98/Obtainium).

- Install Obtainium.
- Tap on ‘Add App’.
	 <img src="/images/Pasted image 20250324070345.png" width="200">
- Add the ByeByeDPI repository: `https://github.com/romanvht/ByeDPIAndroid/releases`
	 <img src="/images/Pasted image 20250324070448.png" width="200">
- Addendum added
	 <img src="/images/Pasted image 20250324070610.png" width="200">
- To change the auto-update settings, you must change the Obtainium settings.

[^1]: Team selection is in development. There may be errors. **Strategies are not generated automatically** - they are always the same. In the current implementation, the selection does not actually select anything - it just checks the performance of a set of strategies that have been added to it by the developer.
