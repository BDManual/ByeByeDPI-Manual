> [!WARNING]
> It's easier to set up [ByeDPI manager](https://github.com/romanvht/ByeDPIManager) - it handles ByeDPI and ProxiFyre. Otherwise it will be your job to route the traffic into ByeDPI proxy server.

Here's what you need to have:
1. ByeByeDPI (obviously) with correct settings.
2. A working strategy for your domain(s).

Open [this link](https://github.com/spvkgn/byedpi), go to **Releases** and download byedpi-16-x86_64-w64.zip.

In the disk C:, make a directory called _byedpi_ and extract all the files from the archive.

Open _service_install_ in Notepad and in line `set svc_bin="\"%cd%\ciadpi.exe\"` replace everything after it with your strategy so it looks like this:

<img src="images/Pasted image 20250321232408.png" width="700">

Save the file.

Launch the file you edited with administrator privileges. Confirm all the dialogs until the commandline shows up.

It should look like this:

<img src="images/Pasted image 20250321232617.png" width="700">

Press any key to close the commandline.

You can use either [Proxy SwitchyOmega 3](https://chromewebstore.google.com/detail/proxy-switchyomega-3-zero/pfnededegaaopdmhkdmcofjmoldfiped?hl=ru&utm_source=ext_sidebar) or [FoxyProxy](https://chromewebstore.google.com/detail/foxyproxy/gcknhkkoolaabfmlnjonogaaifnjlfnp?hl=ru&utm_source=ext_sidebar) for Chromium-based browsers. For Firefox - [ZeroOmega--Proxy SwitchyOmega V3](https://addons.mozilla.org/ru/firefox/addon/zeroomega/?utm_source=addons.mozilla.org&utm_medium=referral&utm_content=search).
You can see [this page](features.en.md#extension) for setting them up.

Also, Firefox has proxy settings built-in.

> [!TIP]
> It is advised to use the strategy that spoofs UDP connection. Otherwise it will be necessary to disable QUIC in browser.

Instruction made by **karlosu**
