---
title: Problems and Solutions
weight: 6
---

## Recently everything worked, but now it doesn't {#not-working-now}

First, try changing DNS in ByeByeDPI or in the system settings. If working DoT or DoH is already configured in the system, select system DNS in ByeByeDPI. More options are described on the [DNS](/en/docs/dns/) page.

Then clear ByeByeDPI data and reboot the device. If the problem occurs only in a specific application, such as YouTube, clear its data and update the client to the latest version.

If nothing changes, run [strategy selection again](/en/docs/start/#adjusting-the-settings). If the website opens in a browser added to the [whitelist](/en/docs/strategies/#whitelist-blacklist), the issue is most likely with the application client rather than the ByeByeDPI strategy.

## Proxy selection crashes {#crash-proxy-test}

<img src="/images/image-12.png" width="200" alt="Crash message">

If the selection crashes during testing - update the application to version >1.5.2.

## All strategies show 0% during testing {#only-0}

Set a different DNS over TLS.

Stop the application, clear its data and reboot the device.
Try changing the port, for example to 1082.
If nothing helps - try clearing all ByeByeDPI data, uninstalling the app and reinstalling it.
Increase timeouts in the strategy selection settings.

## Strategies have the same low percentage {#equally-low-percentage}

Update ByeByeDPI to the latest version. If the problem persists - set a different DNS over TLS.

If Android version is 9 or below - this is normal: test on a newer Android version on the same network and transfer the strategy to a device with older Android.

If Android 10 or newer - there's a chance that IP-based blocking and ByeByeDPI won't help.

## No permission to activate VPN {#permission}

The problem is that ByeDPI gave an error.

If when trying to connect you see the message **No permission to activate VPN**:

<img src="/images/photo_2025-02-26_12-50-33.jpg" width="200" alt="Permission error">

Go to device settings -> "Connections" -> "VPN"

<img src="/images/Pasted image 20250305194232.png" width="200" alt="VPN settings">

If you see that an app is constantly running in VPN mode - disable this app so there's no VPN connection.
Make sure no app is set to "Always on".

<img src="/images/photo_2025-02-26_13-02-02.jpg" width="200" alt="VPN connection status">

## Works only on Wi-Fi or only on mobile internet, or only with one provider {#only-one-case}

Each network needs its own strategy. When connecting to a different network, perform [strategy selection again](/en/docs/start/#adjusting-the-settings). Once a working strategy is found, pin it and label it for the corresponding network.

Also try disabling [network acceleration](#simultaneously-wi-fi-mobile-web) in Wi-Fi settings.

## An app or website doesn't work when ByeByeDPI is running {#something-is-not-working}

If an app works without ByeByeDPI but stops working after it is enabled, use the [application whitelist or blacklist](/en/docs/strategies/#whitelist-blacklist) so that an unsuitable strategy does not process its traffic.

If some websites don't work, like `kremlin.ru` - use two browsers: add one to the [whitelist](/en/docs/strategies/#whitelist-blacklist) (where ByeByeDPI will work), and don't add the other one (where ByeByeDPI won't work).
If you don't like the two-browser option, use [per-site routing methods](/en/docs/routing/#split-routing).

## Telegram or WhatsApp does not work

For some users, Telegram and WhatsApp are blocked by IP address. ByeByeDPI cannot bypass this type of blocking, so selecting ByeByeDPI strategies or domain lists is not a solution.

As a separate option for Telegram, you can try this [solution from the discussion](https://t.me/byebyedpi_group/1434765/1479012).

If the app works without ByeByeDPI but fails only after it is enabled, exclude its traffic using the [application whitelist or blacklist](/en/docs/strategies/#whitelist-blacklist).

## Can ByeByeDPI bypass an allowlist

No. With this type of blocking, access remains available only to a small list of approved websites and IP addresses. Traffic cannot reach other addresses, so ByeByeDPI cannot help.

A VPN or proxy works only if its server remains reachable. If a connection to that server cannot be established, changing SNI or a ByeByeDPI strategy will not help.

The implementation may vary between networks and regions, but trying different ByeByeDPI strategies is not a way to bypass an allowlist.

## Doesn't work with SmartTube {#smarttube}

> [!CAUTION]
> If Android version is 9 or lower, you probably won't be able to set up SmartTube to work correctly with ByeByeDPI.

If your device has Android 10 or newer, update SmartTube to the latest version, try different network engines in SmartTube settings, try configuring SmartTube in proxy mode according to [this instruction](#no-vpn).
If none of these actions helped, reboot the device and perform [strategy selection](/en/docs/start/#adjusting-the-settings) again.

### Error 403

This error is related exclusively to SmartTube's operation. Users [complained](https://github.com/yuliskov/SmartTube/issues/3606) about this problem a long time ago. Updating or reinstalling SmartTube might help.

## Internet disappears on TV when ByeByeDPI starts {#internet-is-lost}

Use the [whitelist](/en/docs/strategies/#whitelist-blacklist) or [per-site routing](/en/docs/routing/#split-routing). But first check that the TV box has internet at all (Wi-Fi or Ethernet cable connected).
If Android version is higher than 9 - you can configure SmartTube and ByeByeDPI in [proxy mode](/en/docs/routing/#vpn-proxy-modes).

## No audio in Discord {#ds-no-voice}

Perform selection for these domains:

```
discord.com
discordapp.com
discord.gg
discord.media
discordapp.net
discordstatus.com
dis.gd
discordcdn.com
```

Instructions for selecting your own domains are [here](/en/docs/strategies/#unlock-more-services).
In **selection settings** enable **extended log**:

<img src="/images/image-14.png" width="200" alt="Extended log option">

One of the main points is the response from the `discord.gg` domain.

> [!WARNING]
> The strategy must be able to handle UDP traffic for voice chat to work.

## High percentage, but doesn't work at all {#high-not-work}

Try **updating** the YouTube client.

If you accidentally enabled IPv6 - disable it

<img src="/images/Pasted image 20250305213514.png" width="200" alt="IPv6 settings">

Check in the selection settings the number of requests to the domain: should be at least 5.

- Go to **Selection settings** (gear icon in the top right)

   <img src="/images/image-3.png" width="200" alt="Selection settings">

- Change **Number of requests to domain** to 5

   <img src="/images/image-4.png" width="200" alt="Number of requests">

- Return to **Command selection (Beta)** and click the "Start selection" button

   <img src="/images/image-5.png" width="200" alt="Start selection button">

Try adding a browser to the [whitelist](/en/docs/strategies/#whitelist-blacklist) and opening YouTube there. If it works - the problem is with the YouTube client.
Try using YouTube Revanced Extended with QUIC disabled:
Settings → Extended → Other → disable quic.

<img src="/images/Pasted image 20250305214109.png" width="200" alt="QUIC settings">

If this is happening on a TV and you have Android 11 or higher - try SmartTube with okHttp engine:
**SmartTube** or **SmartTube Beta** (latest versions). Settings → Player → Network engine: **okHTTP**.

## Cannot use VPN mode on my device {#no-vpn}

### SmartTube

If your device's Android version is higher than 9 - you can try configuring SmartTube and ByeByeDPI in proxy mode:

- Switch VPN mode to proxy mode. In _Proxy_ settings specify (if not previously specified in the command line):
```
Address: 127.0.0.1  
Port: 1080
```
- Go to settings in SmartTube:
```
General → Internet censorship →
Address: 127.0.0.1, Port: 1080, Name and password: empty, Type: socks.
Player → Network engine: okHTTP, Video profile: 2K, Maximum buffer size.
```

### Firefox

If the SmartTube method didn't work for some reason:
- Switch VPN mode to proxy mode. In _Proxy_ settings specify (if not previously specified in the command line):
```
Address: 127.0.0.1  
Port: 1080
```
- Download `Firefox`, install the `ZeroOmega--Proxy SwitchyOmega V3` extension and follow [the instructions](/en/docs/routing/#extension). To make watching YouTube more comfortable, you can download the `SponsorBlock` extension.

## Very low percentages (above zero) {#low-interest-rates}

There's a chance DNS is being hijacked. Specify your own DoT (DNS-over-TLS) in the system:

<img src="/images/Pasted image 20250305220140.png" width="200" alt="DoT settings 1">

<img src="/images/Pasted image 20250305220209.png" width="200" alt="DoT settings 2">

Reboot your device and perform [strategy selection again](/en/docs/start/#adjusting-the-settings).

Verified DoT can be found [here](https://dnsprivacy.org/public_resolvers/).

## Cannot update or import settings {#digital-signatur}

Update 1.4.2 added digital signature. To update from older versions to 1.4.2 and above, a clean installation is required (uninstall the old version, install the new one).

It is impossible to export settings from version 1.4.1 and older and import them to 1.4.2 and newer. If you want to extract some information from a settings file, you can open it with any text editor.

## ByeByeDPI turns off by itself {#abnormal-shutdown}

- You need to disable any power-saving modes for ByeByeDPI in battery settings.
- Disable various optimizers.
- Check auto-start settings and allow auto-start for ByeByeDPI:
   <img src="/images/Pasted image 20250416221348.png" width="200" alt="Auto-start settings">
- Check if there's an app that can automatically start VPN mode (like NUM).
- Check if there's an app that constantly uses VPN mode (more about this [here](#permission)).

> [!WARNING]
> The **NUM** app can automatically enable VPN

To disable VPN startup in NUM, go to:

```
Settings -> Bypass blocking -> Uncheck auto-connect if it's checked
```

If none of the above helped, try switching from VPN mode to Proxy mode. If the connection doesn't drop in Proxy mode and the proxy works - the problem is in VPN mode on your device: either an app is occupying the connection (like NUM or VPNDialogs), or VPN can't be enabled on your device.

## Unlimited traffic is being spent on YouTube {#spend-traffic}

ByeByeDPI is not a VPN, but when using it, unlimited YouTube traffic gets spent. This happens because YouTube is being slowed down via DPI and your traffic is tracked via DPI (for example, so you have unlimited YouTube access). However, when using ByeByeDPI and other packet modifiers, DPI doesn't detect that you're watching YouTube. Therefore, if you're hiding from blocking DPI, you're also hiding from the DPI that prevents charging for YouTube.

Don't expect tech support to tell you that you can pay for unlimited YouTube use with a VPN - it won't work. Since ByeByeDPI is not a VPN. Even with unlimited VPN, when using ByeByeDPI, traffic will be spent.

For DPI, traffic from ByeByeDPI in VPN mode and Proxy mode is no different. Read more in [Modes and routing](/en/docs/routing/#vpn-proxy-modes).

## Percentages are not displayed {#invisible-percentage}

If during selection you see this:

<img src="/images/photo_2025-02-18_23-13-15.jpg" width="200" alt="No percentages">

This is a very rare display error. Try switching the theme to dark. If that doesn't help: enable extended log and after selection finishes, check the "Commands with success above 50%" list from top to bottom.

## Doesn't work with Wi-Fi and mobile internet on simultaneously {#simultaneously-wi-fi-mobile-web}

Try disabling network acceleration in Wi-Fi settings:

<img src="/images/Pasted image 20250416222036.png" width="200" alt="Network acceleration">

## Error parsing the package {#error-parsing-the-package}

If Android version is less than 6.0, nothing can be done about this error. If Android version is 6.0 or higher, use a third-party file manager, for example: FX File Manager, [Amaze File Manager](https://github.com/TeamAmaze/AmazeFileManager), [Material Files](https://github.com/zhanghai/MaterialFiles), [Fossify File Manager](https://github.com/FossifyOrg/File-Manager).

## No YouTube tiles on TV home screen {#no-tiles-on-tv}

Try adding the Home app or another app responsible for the **home screen** to the [whitelist](/en/docs/strategies/#whitelist-blacklist).

## DoT or DoH doesn't work in ByeByeDPI {#only-dns-ipv4}

DoT and DoH cannot be entered directly in the application's DNS field. Configure them at the system level, then select system DNS in ByeByeDPI or leave the DNS field empty. Strategy testing uses system DNS regardless of the value in this field.

## Doesn't work on Yandex TV running YaOS {#yaos}

YaOS TV often has problems. Check if YouTube works in the browser: if it does - the problem is with the client. Some users fixed it by installing [YouTube for Android TV 1.3.11](https://www.apkmirror.com/apk/google-inc/youtube-for-android-tv-android-tv/youtube-for-android-tv-android-tv-1-3-11-release/youtube-android-tv-1-3-11-android-apk-download/) and updating on top of the latest [YouTube for Android TV](https://www.apkmirror.com/apk/google-inc/youtube-for-android-tv-android-tv/).

You can also try alternative client [TizenTube Cobalt](https://github.com/reisxd/TizenTubeCobalt). If YaOS is based on Android 10+ - you can try [SmartTube](https://github.com/yuliskov/SmartTube) with ByeByeDPI in VPN mode or connect it in [proxy mode](#no-vpn).

## Doesn't work on TV at all / Can't install app due to WebOS/Tizen {#not-working-tv}

If you tried all [clients](/en/docs/youtube-clients/) and YouTube does not work in a browser or in [proxy](#no-vpn) mode with the extension enabled, the problem is in the firmware. Configure the bypass on a [router](/en/docs/alternatives/#other-router) or [set it up on a PC](https://github.com/BDManual/ByeDPIManager-Manual/blob/main/smarttv.md) and use the PC as a gateway for TV traffic.

## Failed to start VPN {#unable-to-start}

<img src="/images/vpn_failed_ru.jpg" width="200" alt="VPN failed message">

Check that the strategy is written correctly. If you can't - use a different strategy.

## Doesn't work on sbertv / saluttv {#sber}

Check if YouTube works in the browser, after adding the browser to the whitelist first. If it works - install the latest version of the official [YouTube](https://www.apkmirror.com/apk/google-inc/youtube-for-android-tv-android-tv/) client.

If the problem persists - there's a chance that special [configuration](/en/docs/sbox/) of the TV is required.
