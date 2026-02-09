# Другое

1. [Клиенты YouTube](#клиенты)
2. [Проксирующие DNS](#proxy-dns)
3. [Другие варианты ускорения серверов](#other-options)
     - [На Android](#other-android)
     - [На Windows](#other-windows)
     - [На Linux](#other-linux)
     - [На роутере](#other-router)
     - [На домашнем сервере (постоянно включенном устройстве)](#other-home-server)
     - [На сервере](#other-vps)
     - [На Mac](#other-mac)
     - [На iOS](#other-iphone)
4. ["Стандартный редактор" - нужен ли?](#ui-editor)
5. [Универсальная стратегия](#universal)

## <a id="клиенты">Клиенты YouTube</a>

Если вас по каким-то причинам не устраивает оригинальное приложение YouTube, вот несколько альтернативных:

#### Для телевизоров и приставок

- [YouTube for Androuid TV](https://play.google.com/store/apps/details?id=com.google.android.youtube.tv) - официальное приложение YouTube для управления пультом. Требуется Android 7.0+
- [SmartTube](https://github.com/yuliskov/SmartTube) - единственный клиент с поддержкой прокси. Требуется Android 4.3+
- [TizenTube Cobalt](https://github.com/reisxd/TizenTubeCobalt) - улучшает качество просмотра YouTube за счет удаления рекламы и спонсорских вставок. Требуется Android 7.0+

#### YouTube с патчами

- YouTube ReVanced. [Revanced Manager](https://revanced.app/download) - приложение для удобного скачивания и обновления ReVanced и MicroG. [revanced.app](https://revanced.app/) - Официальный сайт ReVanced. Требуется Android 8.0+
- [Morphe](https://morphe.software/) - альтернативный проект патчей ReVanced. От разработчиков, создавших модификации YouTube и YT Music. Требуется Android 9.0+
- YouTube ReVanced Extended - если у вас проблемы с QUIC. Требуется Android 8.0+

> [!TIP]
> Для установки YouTube ReVanced, Morphe и YouTube ReVanced Extended рекомендуется патчить приложение самостоятельно:

- [YouTube ReVanced Manager](https://github.com/ReVanced/revanced-manager)
- [Morphe manager](https://github.com/MorpheApp/morphe-manager)
- [RVX Manager](https://github.com/inotia00/revanced-manager)

#### NewPipe и его вариации

- [NewPipe](https://github.com/TeamNewPipe/NewPipe/releases) - клиент для YouTube, который не использует каких-либо библиотек, зависящих от Google. Отсутствует функция авторизации в google аккаунт. Требуется Android 5.0+
- [BravePipe](https://github.com/bravenewpipe/NewPipe) - форк NewPipe с поддержкой Sponsorblock, улучшенными фильтрами поиска и сортировки. Есть импорт подписок с помощью Google Takeout. Требуется Android 4.4+ (не проверено)
- [PipePipe](https://github.com/InfinityLoop1308/PipePipe) - форк NewPipe с большим количеством сервисов, клиентских функций и исправлений ошибок. Требуется Android 5.0+
- [Tubular](https://github.com/polymorphicshade/Tubular) - форк NewPipe c поддержкой Sponsorblock и ReturnYouTubeDislike. Требуется Android 5.0+

#### SkyTube

- [SkyTube Extra](https://github.com/SkyTubeTeam/SkyTube) - простой и функциональный проигрыватель видео с YouTube. Поддерживает официальный плеер и Chromecast. Требуется Android 4.4+
- [SkyTube](https://github.com/SkyTubeTeam/SkyTube) - простое и функциональное свободное приложение для проигрывания видеороликов с YouTube, которое не требует Google Play Services для работы. Требуется Android 4.4+
- [SkyTube Legacy Extra](https://github.com/SkyTubeTeam/SkyTubeLegacy) - простой и функциональный проигрыватель видео с YouTube. Поддерживает официальный плеер и Chromecast. Требуется Android 4.0+
- [SkyTube Legacy](https://github.com/SkyTubeTeam/SkyTubeLegacy) - простое и функциональное свободное приложение для проигрывания видеороликов с YouTube, которое не требует Google Play Services для работы. Требуется Android 4.0+

#### Идейные клиенты, которые выступают за приватность

> [!WARNING]
> Для работы данных приложений требуются инстансы. Они могут быть заблокированы иначе чем YouTube и требовать [разблокировки](features.md#разблокировать-свои-ресурсы) отдельно.

- [FreeTube Android](https://github.com/MarmadileManteater/FreeTubeAndroid) - клиент YouTube, использующий Invidious API для передачи данных и видео с YouTube. Требуется Android 7.0+
- [LibreTube](https://github.com/libre-tube/LibreTube) - клиент, использующий [API Piped](https://github.com/TeamPiped/Piped) для отображения содержимого каналов и воспроизведения контента, не требует наличия учетной записи YouTube и сервисов Google.
- [Mini YouTube](https://github.com/monobogdan/selfeco) - клиент YouTube из состава приложений SelfEco. Использует Invidous API. **Требуется Android 2.2+**. Также существует [форк](https://github.com/tinelix/selfeco-plus), с заявленной поддержкой HTTP-прокси для YouTube, однако собирать приложение нужно самостоятельно.

#### Ещё варианты

- [VueTube](https://github.com/pixkk/VueTube) - клиент YouTube построенный на базе Vue. Есть поддержка Sponsorblock и ReturnYouTubeDislike. Требуется Android 5.0+ (возможно не поддерживается Android 12.1+)
- [Namida](https://github.com/namidaco/namida) - красивый и многофункциональный проигрыватель музыки и видео с поддержкой YouTube.
- [YT PRO](https://github.com/prateek-chaubey/YTPro) - легковесный парсер/оболочка m.youtube.com с продвинутыми функциями. Требуется Android 5.0+

#### Проприетарные программы

- [PureTuber](https://play.google.com/store/apps/details?id=free.tube.premium.advanced.tuber) – это клиент для YouTube, за основу которого был взят NewPipe. Новый интерфейс и добавлена возможность входа в google-аккаунт. Требуется Android 4.4+
- [GreenTuber](https://play.google.com/store/apps/details?id=by.green.tuber&hl=en) - YouTube с блокировщиком рекламы. Требуется Android 6.0+

## <a id="proxy-dns">Проксирующие DNS</a>

> [!CAUTION]
> Будьте осторожны при использовании различных DNS. Используйте только те DNS-сервера, в надёжности и безопасности которых вы уверены.

Чтобы использовать некоторые ресурсы, которые заблокированы извне можно использовать проксирующие DNS - они скрывают ваше местоположение от некоторых ресурсов.

В теории, такие DNS можно установить в ByeByeDPI в формате IPv4 и пропускать трафик к заблокированному ресурсу через ByeByeDPI, но это не сильно рационально. Лучшим вариантом будет установить DoH на уровне браузера. Не стоит использовать такие DNS для всей системы, так как, например, Comss DNS иногда не выдерживает нагрузки и отключается. Если такой DNS будет работать для всей системы - у вас пропадёт интернет.

Вот к чему можно получить доступ, используя [Comss DNS](https://www.comss.ru/page.php?id=7315): вы можете пользоваться ИИ-сервисами (ChatGPT и Sora, Microsoft Copilot, GitHub Copilot, xAI Grok, Google Gemini и Claude AI), или устанавливать обновления антивирусов, инсайдерские сборки и обновления Windows, а также играть в Brawl Stars и сетевые режимы Doom Eternal в России.

## <a id="other-options">Другие варианты ускорения серверов</a>

> [!CAUTION]
> Используйте любые решения на свой страх и риск. Авторы руководства не отвечают за последствия и возможный вред от использования любого программного обеспечения, которое упомянуто в данном мануале.

> [!TIP]
> ByeDPI или zapret? Если вы хотите, чтобы устройства внутри локальной сети могли подключаться к вашему компьютеру - используйте ByeDPI и читайте [инструкцию](features.md#distribute) по предоставлению доступа к ByeByeDPI - действия почти идентичные.

### <a id="other-android">На Android</a>

#### Модули Magisk для Android (нужен root)

- [ZDT&D Magisk Module](https://github.com/GAME-OVER-op/ZDT-D) от GAME-OVER-op
- [zapret-magisk](https://github.com/ImMALWARE/zapret-magisk) от ImMALWARE
- [zapret-pocket](https://github.com/sevcator/zapret-pocket) - форк модуля ImMALWARE от sevcator
- Приложение [zaprett-app](https://github.com/CherretGit/zaprett-app) от CherretGit и egor-white

#### NoDPI4Android

- [NoDPI4Android](https://github.com/GVCoder09/NoDPI4Android) от GVCoder09

### <a id="other-windows">На Windows</a>

#### Сборки zapret

- [zapret-discord-youtube](https://github.com/Flowseal/zapret-discord-youtube) сборка zapret от Flowseal (простое решение без излишеств).

#### Приложения с графическим интерфейсом

- [CDPI UI](https://github.com/Storik4pro/cdpiui) от Storik4pro. Менеджер для популярных утилит модификации трафика.
- [ByeDPI Manager](https://github.com/romanvht/bdmanager) от romanvht. Небольшая утилита, упрощающая работу с ByeDPI на Windows (подходит [для Windows 7](https://github.com/BDManual/ByeDPIManager-Manual/blob/main/win7.md)).
- [goodbyeDPI-UI](https://github.com/Storik4pro/goodbyeDPI-UI) от Storik4pro. Комбайн для zapret, ByeDPI, GoodbyeDPI и SpoofDPI.

#### Оригинальные утилиты

- [zapret](https://github.com/bol-van/zapret) от bol-van
- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea (в теории версия [byedpi-x86-cygwin.zip](https://github.com/hufrea/byedpi/issues/219#issuecomment-2559707231) способна работать даже на Windows XP)
- [NoDPI](https://github.com/GVCoder09/NoDPI) от GVCoder09

#### Инструкции к оригинальным утилитам

> [!CAUTION]
> В ByeDPI нет подбора стратегий - найти рабочую стратегию необходимо самостоятельно (например, при помощи подбора в [ByeByeDPI](https://github.com/romanvht/ByeByeDPI) или [ByeDPI Manager](https://github.com/romanvht/ByeDPIManager)).

- [zapret](https://github.com/bol-van/zapret?tab=readme-ov-file#%D0%B1%D1%8B%D1%81%D1%82%D1%80%D1%8B%D0%B9-%D1%81%D1%82%D0%B0%D1%80%D1%82)
- [ByeDPI](byedpi-guide-windows.md)

### <a id="other-linux">На Linux</a>

##### Скрипты для автоматической установки

> [!CAUTION]
> Данные скрипты не рекомендуются для использования. Настраивайте оригинальные утилиты

- [zapret.installer](https://github.com/Snowy-Fluffy/zapret.installer) от Snowy-Fluffy
- [zapret-discord-youtube-linux](https://github.com/Sergeydigl3/zapret-discord-youtube-linux) от Sergeydigl3
- [zapret4rocket](https://github.com/IndeecFOX/zapret4rocket) от IndeecFOX
- [Byedpi-Setup](https://github.com/fatyzzz/Byedpi-Setup) от fatyzzz

#### Оригинальные утилиты

##### zapret

- [zapret](https://github.com/bol-van/zapret) от bol-van
- [zapret в контейнере](https://github.com/vernette/ss-zapret) c Shadowsocks и SOCKS5 от vernette

##### zapret2

- [zapret2](https://github.com/bol-van/zapret2/tree/master) от bol-van
- [zapret2 в контейнере](https://github.com/vernette/ss-zapret2) c Shadowsocks и SOCKS5 от vernette

##### byedpi

- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea
- [byedpictl](https://github.com/maximilionus/byedpictl) от maximilionus. Небольшая утилита для управления ByeDPI. Также содержит HevSocks5Tunnel.
- [контейнер с ByeDPI](https://github.com/hufrea/byedpi/tree/main/dist/docker) (официальный)
- [контейнер с ByeDPI](https://hub.docker.com/r/tazihad/byedpi) (неофициальный) от tazihad
- [контейнер с ByeDPI с автоподбором стратегий](https://hub.docker.com/r/vindibona/byedpi-orchestrator) от vindibona

##### B4

- [B4](https://github.com/DanielLavrushin/b4) от DanielLavrushin

##### youtubeUnblock

- [youtubeUnblock](https://github.com/Waujito/youtubeUnblock) от Waujito

##### NoDPI

- [NoDPI](https://github.com/GVCoder09/NoDPI) от GVCoder09

##### SpoofDPI

- [SpoofDPI](https://github.com/xvzc/SpoofDPI) от xvzc

#### Инструкции к оригинальным утилитам

> [!CAUTION]
> В ByeDPI нет подбора стратегий - найти рабочую стратегию необходимо самостоятельно (например, при помощи подбора в ByeByeDPI).

- [zapret](https://github.com/bol-van/zapret?tab=readme-ov-file#%D0%B1%D1%8B%D1%81%D1%82%D1%80%D1%8B%D0%B9-%D1%81%D1%82%D0%B0%D1%80%D1%82)
- [ByeDPI](https://github.com/hufrea/byedpi/tree/main/dist/linux)

### <a id="other-router">На роутере</a>

#### OpenWrt

##### zapret

- [Оригинальный zapret](https://github.com/bol-van/zapret/blob/master/docs/quick_start.md)
- [zapret‐openwrt](https://github.com/remittor/zapret-openwrt) - пакеты zapret и zapret2 с интерфейсом от remittor
- [Пакет zapret](https://github.com/spvkgn/zapret-openwrt) от spvkgn собранный под OpenWrt

##### zapret2

- [Оригинальный zapret2](https://github.com/bol-van/zapret2/tree/master)
- [zapret‐openwrt](https://github.com/remittor/zapret-openwrt) - пакеты zapret и zapret2 с интерфейсом от remittor
- [Пакет zapret2](https://github.com/spvkgn/zapret2-openwrt) от spvkgn собранный под OpenWrt
- [zapret2 от RouteRich](https://github.com/routerich/packages.routerich) **подходит только для aarch64_cortex-a53** - zapret2 с интерфейсом. Информация о пакете и его использовании в группе RouteRich в telegram

##### byedpi

- [ByeDPI для OpenWrt](https://github.com/DPITrickster/ByeDPI-OpenWrt)
- [ByeDPI + Redsocks](https://habr.com/ru/articles/856312/)

##### youtubeUnblock

- [youtubeUnblock](https://lsetc.ru/ustanovka-youtubeunblock-na-openwrt/)

##### B4

- [B4](https://github.com/DanielLavrushin/b4) от DanielLavrushin

> [!TIP]
> Можно использовать [пакет ByeDPI](https://github.com/DPITrickster/ByeDPI-OpenWrt) в качестве outbound'a в [podkop](https://github.com/itdoginfo/podkop), чтобы управлять трафиком через sign-box. Гайд можно прочитать [здесь](https://github.com/DPITrickster/Podkop-ByeDPI-OpenWRT)

#### Keenetic

- [nfqws-keenetic](https://github.com/Anonym-tsk/nfqws-keenetic) - сборка nfqws ориентированная на Keenetic. Есть инструкция для Keenetic / OpenWrt / Netcraze / Padavan
- [nfqws2-keenetic](https://github.com/nfqws/nfqws2-keenetic) - сборка nfqws2 ориентированная на Keenetic. Есть инструкция для Keenetic / OpenWrt / Netcraze / Padavan
- [B4](https://github.com/DanielLavrushin/b4) от DanielLavrushin
- [youtubeUnblock](https://github.com/Waujito/youtubeUnblock?tab=readme-ov-file#entware) от Waujito
- [zapret](https://github.com/AlexFBG/zapret)
- [nfqws](https://habr.com/ru/articles/834826/) - программа из состава zapret. Инструкция для Keenetic

#### MikroTik

- [ByeDPI](https://habr.com/ru/articles/838452/) - статья с инструкцией
- [Контейнеры](https://hub.docker.com/u/wiktorbgu) с tpws из состава zapret и ByeDPI от wiktorbgu. В tpws нет возможности использовать UDP
- [контейнер с ByeDPI с автоподбором стратегий](https://hub.docker.com/r/vindibona/byedpi-orchestrator) от vindibona

> [!WARNING]
> Необходимая [информация](https://gist.github.com/wiktorbgu/b27828bc789d9e751c18503d0ee86675) о запуске nfqws1 и nfqws2 на MikroTik

- [Контейнер с nfqws1 из zapret1](https://hub.docker.com/r/wiktorbgu/nfqws-mikrotik) от wiktorbgu
- [Контейнер с nfqws2 из zapret2](https://hub.docker.com/r/wiktorbgu/nfqws2-mikrotik) от wiktorbgu

### <a id="other-home-server">На домашнем сервере (постоянно включенном устройстве)</a>

##### byedpi

- Можно подключаться к ByeDPI, который будет развёрнут на вашем ПК
- [Можно подключаться](features.md#distribute) к телефону, на котором запущен ByeByeDPI
- [ByeDPI на одноплатном компьютере](https://habr.com/ru/articles/870254/)
- [контейнер с ByeDPI](https://github.com/hufrea/byedpi/tree/main/dist/docker) (официальный)
- [контейнер с ByeDPI](https://hub.docker.com/r/tazihad/byedpi) (неофициальный) от tazihad
- [ByeDPI на Synology](https://bafista.ru/ustanovka-byedpi-v-kontejner-docker-na-synology/) или [ByeDPI на TerraMaster](https://bafista.ru/ustanovka-byedpi-v-kontejner-docker-na-terramaster/)

##### youtubeUnblock

- [youtubeUnblock на одноплатном компьютере](https://habr.com/ru/articles/871460/)

##### zapret

- [zapret в контейнере](https://github.com/vernette/ss-zapret) c Shadowsocks и SOCKS5
- [zapret2 в контейнере](https://github.com/vernette/ss-zapret2) c Shadowsocks и SOCKS5
- [zapret на одноплатном компьютере](https://habr.com/ru/articles/833508/)

### <a id="other-vps">На сервере</a>

- [zapret](https://github.com/bol-van/zapret) от bol-van
- [zapret2](https://github.com/bol-van/zapret2/tree/master) от bol-van
- [zapret в контейнере](https://github.com/vernette/ss-zapret) c Shadowsocks и SOCKS5 от vernette
- [zapret2 в контейнере](https://github.com/vernette/ss-zapret2) c Shadowsocks и SOCKS5 от vernett
- [zapret4rocket](https://github.com/IndeecFOX/zapret4rocket) от IndeecFOX

### <a id="other-mac">На Mac</a>

> [!CAUTION]
> Выполняйте инструкции на свой страх и риск!

- [ByeDPI](https://github.com/hufrea/byedpi) от hufrea
- [zapret](https://github.com/bol-van/zapret/blob/master/docs/bsd.md#macos) от bol-van
- [NoDPI](https://github.com/GVCoder09/NoDPI) от GVCoder09
- [SpoofDPI](https://github.com/xvzc/SpoofDPI) от xvzc

#### Контейнеры

- [контейнер с ByeDPI](https://github.com/hufrea/byedpi/tree/main/dist/docker) (официальный)
- [контейнер с ByeDPI](https://hub.docker.com/r/tazihad/byedpi) (неофициальный) от tazihad
- [контейнер с NoDPI](https://github.com/GVCoder09/NoDPI?tab=readme-ov-file#run-in-docker) от GVCoder09

#### Нативная установка ByeDPI

[Инструкция](https://github.com/hufrea/byedpi/tree/main/dist/linux) по установке ByeDPI *на Linux*

Так как автор инструкции не имеет устройства с MacOS, он может только предположить, что необходимо выполнить следующие шаги:

- Установите инструменты командной строки Xcode

```
xcode-select --install
```

-  Установите Homebrew (менеджер пакетов для macOS)

```
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
```

- Установите необходимые инструменты

```
brew install git gcc make binutils
```

- Склонируйте репозиторий

```
git clone https://github.com/hufrea/byedpi.git
```

- Перейдите в папку

```
cd byedpi
```

- Скомпилируйте

```
make
```

- Сделайте исполняемым  `ciadpi`

```
chmod +x ciadpi
```

- Запустите

> [!WARNING]
> Аргументы указываются без квадратных скобок. Если стратегия по умолчанию не работает — перебирайте другие из [списка](ALL.TXT)

```
./ciadpi [стратегия, которая работает на телефоне в приложении ByeByeDPI в вашей сети]
```

Чтобы проверить работу ByeDPI, [установите Firefox](https://www.mozilla.org/en-US/firefox/mac/) и проверьте работу сервисов там, подключившись к SOCKS5-прокси ByeDPI. Если всё хорошо работает - в последствии можно будет использовать приложения по типу FoXray, [V2RayXS](https://github.com/tzmax/V2RayXS), [nekoray](https://github.com/Mahdi-zarei/nekoray).

> [!CAUTION]
> На данном этапе установка завершена.
> При последующих запусках необходимо указывать путь до `ciadpi`, например: `/Users/you/apps/byedpi/ciadpi стратегия`

Чтобы добавить в автозапуск

- Создайте файл LaunchAgent

```
nano ~/Library/LaunchAgents/com.user.ciadpi.plist
```

- Вставьте следующий код, заменив `ПОЛНЫЙ_ПУТЬ` на абсолютный путь до `ciadpi`, и укажите стратегии:

```
<?xml version="1.0" encoding="UTF-8"?>
<!DOCTYPE plist PUBLIC "-//Apple//DTD PLIST 1.0//EN" "http://www.apple.com/DTDs/PropertyList-1.0.dtd">
<plist version="1.0">
<dict>
  <!-- Уникальный идентификатор службы -->
  <key>Label</key>
  <string>com.user.ciadpi</string>

  <!-- Аргументы запуска -->
  <key>ProgramArguments</key>
  <array>
    <string>/ПОЛНЫЙ_ПУТЬ/ciadpi</string>
    <string>аргумент1 (это часть с стратегии с дефисом, например, `-Ku`)</string>
    <string>аргумент2</string>
    <!-- При необходимости добавьте другие -->
    <!-- <string>аргумент</string> -->
  </array>

  <!-- Запуск при входе в систему -->
  <key>RunAtLoad</key>
  <true/>

  <!-- Перезапуск при падении -->
  <key>KeepAlive</key>
  <true/>
</dict>
</plist>
```

- Исправьте разрешения и загрузите службу

```
chmod 644 ~/Library/LaunchAgents/com.user.ciadpi.plist
```

```
launchctl load ~/Library/LaunchAgents/com.user.ciadpi.plist
```

```
launchctl start com.user.ciadpi
```

Чтобы удалить, выполните:

```
launchctl unload ~/Library/LaunchAgents/com.user.ciadpi.plist
```

```
rm ~/Library/LaunchAgents/com.user.ciadpi.plist
```

## <a id="other-iphone">На iOS</a>

На iOS есть Rumble - судя по всему, это byedpi + hev-socks5-tunnel. Исходный код находится [здесь](https://github.com/RumbleOrg/Rumble). Для использования его необходимо собрать (требуется сертификат разработчика).

> Из известных проблем пока что отваливающаяся кнопка подключения, помогает удаление профиля VPN приложения.

> [!CAUTION]
> Нет никакой достоверной информации о безопасности **Rumble**. Устанавливайте приложение на свой страх и риск.

Другие варианты для пользователей iOS:

- Использовать VPN. Не требует особых навыков, усилий и знаний
- Раздать доступ к ByeByeDPI с Android-устройства. Данный вариант подойдёт, если есть устройство на Android с настроенным ByeByeDPI. Подробная инструкция [здесь](features.md#раздача-интернета-с-byebyedpi-локальный-прокси)
- Использовать решения по [обходу DPI на роутере](#other-router)
- Использовать решения по [обходу DPI на домашнем сервере](#other-home-server) (в качестве сервера может выступать ПК)

> [!NOTE]
> Если приобрести белый IP у провайдера, то можно будет настроить VPN-туннель до роутера и выходит в интернет с телефона через роутер с настроенным средством обхода

## <a id="ui-editor">"Стандартный редактор" - нужен ли?</a>

Чтобы разрабатывать стратегию (а настройки в графическом редакторе это и есть данный процесс), необходимо разбираться в работе сетей и понимать за что отвечает каждый пункт настроек досконально изучив [документацию](https://github.com/hufrea/byedpi). Тем, кто изучил документацию, не нужен графический редактор, потому что он не отображает всех аргументов, а делает это лишь частично.

"Стандартный редактор" **не нужен**. Тыкать наугад - плохая тактика.

## <a id="universal">Универсальная стратегия</a>

Если вам показалась сложной настройка или у вас ничего не работает - используйте VPN. Или смотрите VK Видео и Rutube - это отличные платформы.
