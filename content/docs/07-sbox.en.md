---
title: SberBOX/SlimBox
weight: 7
---

## Device identification

### Android 9 devices

- SberBox:
  - SBDV-00001, SBDV-00002 (all modifications)
  - SBDV-00004, SBDV-00004C
- OKKO SmartBox (with SberBox firmware)
- SberBoxTime
- SberBoxTop
- SberPortal
- Sber TV (except Android 13 models)

### Android 13 devices

- SBDV-00004V (updated)
- SBDV-00004Р (updated)
- SBDV-00005
- SBDV-00006 (SberBox 2)

## Setup instructions

### Android 13 instructions

> ⚠️ These devices only support connection via computer

#### Enabling developer mode

- Open Android settings
- Go to: Device settings → About device
- Find **Build OS** and tap on it several times until a message appears saying developer mode is activated
- Go back and go to **For developers**
- Enable **Debug over Wi-Fi**
- Remember the displayed *IP address* and *port*

#### Connecting via ADB AppControl

- Install [ADB AppControl](https://adbappcontrol.com/ru/#download) on your computer
- Enter the *IP address* and *port* from the device settings
- Click the **Wi-Fi** icon to connect
- In the **Console** tab, execute commands:

```
shell pm grant io.github.romanvht.byedpi android.permission.WRITE_SECURE_SETTINGS
shell appops set io.github.romanvht.byedpi WRITE_SETTINGS allow
shell appops set io.github.romanvht.byedpi ACTIVATE_VPN allow
```

### Android 9 instructions

#### Preparation via Sber Studio

- Sign in to [developers.sber.ru/studio](https://developers.sber.ru/studio/settings/devices) with your Sber ID
- Click "**+ add**" and specify:
- Serial number (16 characters from settings), Note: all letters are uppercase, O is the digit 0
- Device type (for OKKO select "OKKO Smart Box")
- Enable **ADB feature**

#### 2A. Via ADB TV (easy way)

- Install [ADB TV](https://adbappcontrol.com/tv/download/?r=latest&lang=ru)
- In the **Console** tab execute:

```
pm grant io.github.romanvht.byedpi android.permission.WRITE_SECURE_SETTINGS
appops set io.github.romanvht.byedpi WRITE_SETTINGS allow
appops set io.github.romanvht.byedpi ACTIVATE_VPN allow
```

#### 2B. Via computer

- Install [ADB AppControl](https://adbappcontrol.com/ru/#download)
- Enter the device's *IP address* and *port* 5555
- In the **Console** tab execute:

```
shell pm grant io.github.romanvht.byedpi android.permission.WRITE_SECURE_SETTINGS
shell appops set io.github.romanvht.byedpi WRITE_SETTINGS allow
shell appops set io.github.romanvht.byedpi ACTIVATE_VPN allow
```

## Troubleshooting

### ADB won't turn on:

- Check the *device type* and *serial number*
- Make sure the device is on the network
- Check your *Sber ID*

### Connection problems:

- Check the *IP address* (may change)
- Devices must be on the same network
- Check router settings

## Alternative method for YouTube

### ByeByeDPI setup

- In ByeByeDPI:
  - Settings (gear icon top right)
    - Mode: *Proxy*
    - Port: *1080*
  - On the main screen press the large **Start** button

### SmartTube setup

- Install the **arm64_v8a** version of [SmartTube](https://github.com/yuliskov/SmartTube/releases/latest)
- In SmartTube settings:
  - General → Internet censorship
  - Enable "Use web proxy"
    - Name: *127.0.0.1*
    - Port: *1080*
    - Type: *SOCKS*
  - Click **Test** and **OK**
