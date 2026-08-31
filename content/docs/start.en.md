---
title: Start
weight: 2
aliases:
  - /docs/
---

## What is a ByeByeDPI?

> _**[ByeByeDPI](https://github.com/romanvht/ByeDPIAndroid/blob/master/README-en.md)**_  is an **Android** application that locally runs _[ByeDPI](https://github.com/hufrea/byedpi)_ and routes all traffic through it.

The app requires **Android 6** or newer.
It works **only** on Android devices, Android TV, and some firmware based on Android.

**There is no version** for iOS, TizenOS, WebOS, Windows, macOS, Linux, FreeBSD, etc.  
If your system cannot run ByeByeDPI and you do not want to use a VPN or proxy, consider the [alternatives](/en/docs/alternatives/). This page also lists zapret modules for Magisk.

> [!IMPORTANT]
> The app is **not a VPN**!
> While ByeByeDPI uses VPN mode on Android to route traffic, the application does **not** transmit data to a remote server. The app does not encrypt traffic and does not hide your IP address.

You can learn more about blocking mechanisms here:

- [Zapret official documentation](https://github.com/bol-van/zapret/blob/master/docs/readme.en.md)
- [Evolving Censorship Evasion Strategies](https://geneva.cs.umd.edu/papers/geneva_ccs19.pdf)
- [Censorship research publications](https://ntc.party/c/censorship-research-publications/22)

## How to use ByeByeDPI?

To get started, you need to download the app. The application uses the standard filename extension `apk`.

> [!NOTE]
> The releases contain files for different architectures. If you do not know your processor architecture, download `universal`.

> [!WARNING]
> The application is **completely free**. The author is not responsible if you transfer money to third parties for the application. The developer is also not responsible for versions downloaded from unofficial sources.
> You should **download** the application **only** from the official repository:  
> The latest available version is **[here](https://github.com/romanvht/ByeDPIAndroid/releases)**.

Since ByeByeDPI operates differently from VPNs, the application **requires some configuration**.

### Before adjusting the settings

Check DNS before testing strategies. DNS hijacking or an unstable resolver can prevent websites from opening and distort test results.

Regular and proxying resolvers, DoT/DoH setup, system mode, and troubleshooting are described on the [DNS](/en/docs/dns/) page.

### Adjusting the settings {#adjusting-the-settings}

Proper settings are required for ByeByeDPI to work effectively:

- Allow notifications to be displayed.

   <img src="/images/settings-1.jpg" width="200">

- Before clicking **Connect**, go to the **main settings** in ByeByeDPI (the gear icon in the top right).

   <img src="/images/settings-2.jpg" width="200">

- Activate the ‘Use command line settings’ toggle.

   <img src="/images/settings-3.jpg" width="200">

-  Go to **Proxy test (Beta)**[^1]

   <img src="/images/settings-4.jpg" width="200">

- Go to the **Selection Settings** (gear icon in the top right).

   <img src="/images/settings-5.jpg" width="200">

- Change **Number of queries to domain** to 5.

   <img src="/images/settings-6.jpg" width="200">

- Remove the ‘Add the nearest GoogleVideo for testing’ toggle.

  -  <img src="/images/settings-7.jpg" width="200">

- Add a list of domains to be tested.

   <img src="/images/settings-8.jpg" width="200">

> [!WARNING]
> If you need to test a list of domains, write each domain on a new line. Do **NOT** separate the list with commas or other characters. Domains should be separated by **NEW LINES** only.

   <img src="/images/settings-19.jpg" width="200">

- Go back to **Proxy Test (Beta)** and click the ‘Start Testing’ button.

   <img src="/images/settings-10.jpg" width="200">

- Wait for the selection to complete. If successful, a list called ‘Commands with more than 50% success probability’[^2]. If the test fails, the solution can be found [here](/en/docs/problems/#crash-proxy-test).

   <img src="/images/settings-20.jpg" width="200">

- Click on the strategy with the highest percentage (numbered 1), and select ‘Apply’ from the menu that appears.

   <img src="/images/settings-13.jpg" width="200">

- Return to the main settings in ByeByeDPI.
- Under **Application Filter**, select **White List** mode([more about lists](/en/docs/strategies/#whitelist-blacklist))

   <img src="/images/settings-18.jpg" width="200">

- Under **Select Applications**, check the boxes for the applications that should work via ByeByeDPI (those whose domains you tested in the Proxy Test).

   <img src="/images/settings-14.jpg" width="200">

- Go to the main screen and press the **Connect** button.

   <img src="/images/settings-15.jpg" width="200">

- After clicking **Connect**, give the application permission to connect.

   <img src="/images/settings-16.jpg" width="200">

- Run the **required application** and check its functionality.
- ***If everything works well, the setup is complete.***

---

- If there are any issues with the operation of the desired application: go to **Proxy test (Beta)**
- It should store the result of the **previous test**.
- Click on strategy number 2 and select ‘Apply’ from the menu that appears.

   <img src="/images/settings-21.jpg" width="200">

- Tap the **Connect** button again and test the application.
- Go through the strategies in order of increasing number (or decreasing percentages) until you’re satisfied with the application’s performance.

[^1]: Proxy Test is still in development. There may be errors. **Strategies are not generated automatically** — they are always the same. In the current implementation, the selection process does not actually choose anything. It merely checks the performance of a set of strategies that have been preconfigured by the developer.

[^2]: The percentages shown in the strategy test are not a direct indicator of performance; they reflect the number of successful responses from domains. You can enable their display in the test settings. Even if a strategy doesn’t show 100% success, it may still work (e.g., 30% success). Therefore, it's worth testing strategies one by one, starting from the highest percentage.
