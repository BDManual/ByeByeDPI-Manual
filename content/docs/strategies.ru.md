---
title: Стратегии и списки
weight: 4
---

## Белый и чёрный списки {#whitelist-blacklist}

_Белый_ список - выбранные приложения **будут работать** через ByeByeDPI, все остальные будут работать в обход ByeByeDPI.
**Черный** список - выбранные приложения **НЕ будут работать** через ByeByeDPI, все остальные будут работать через ByeByeDPI.

> [!TIP]
> Почему списки **важны**? Некоторые приложения (например, Телеграм) могут не работать или работать некорректно.
> Плюсом ко всему, чем **меньше трафика** проходит через ByeByeDPI, тем **меньше** заряда батареи **тратится**.
> На некоторых телевизорах (приставках) без настройки белого списка может **совсем не работать интернет**.

## Редактор командной строки {#command-line-editor}

<img src="/images/cmd.png" width="200">

В разделе **Редактор командной строки** находится список **Аргументов командной строки** (стратегий), которые применялись ранее.

<img src="/images/list_strategies.png" width="200">

> [!WARNING]
> Будьте внимательны: длина списка ограничена, если список переполнится - самые старые стратегии пропадут

Над списком есть строка `Список стратегий`, которая позволяет управлять историей стратегий. При нажатии на строку появляется меню с двумя опциями:

- `Удалить незакреплённые` - удаляет все стратегии, которые не закреплены.

- `Очистить историю` - удаляет абсолютно все стратегии из истории.
> [!CAUTION]
> Эти действия **необратимы**!

Если **нажать** на стратегию - появится меню:

<img src="/images/list_menu.png" width="200">

- Действие **Применить** - применит команду (сделает её текущим _Аргументом командной строки_)

   <img src="/images/list_apply.png" width="200">

- Действие **Закрепить** - закрепит стратегию сверху списка

   <img src="/images/strategy_pinned.png" width="200">

- Действие **Переименовать** - позволяет дать имя стратегии или переименовать её

   <img src="/images/strategy_rename.png" width="200">

- Действие **Редактировать** - редактирует стратегию на месте (без необходимости сохранять её как другую).    
- Действие **Копировать** - скопирует стратегию в буфер обмена
- Действие **Удалить** - удалит стратегию из списка (истории)

Под активной стратегией есть 2 кнопки - `Очистить` и `Вставить`. 

При нажатии на кнопку `Очистить` - поле для ввода очистится, никакой стратегии не будет применено.

При нажатии на кнопку `Вставить` - в поле вставится содержимое буфера обмена.

## Свой список команд (стратегий) {#my-list}

> [!IMPORTANT]
> Использовать свой список стратегий нужно **только в случае**, если в результате автоподбора небольшой процент ответа от доменов. Если вы видите, что у стратегий одинаковый (невысокий) процент ответа - решение [тут](/docs/problems/#equally-low-percentage)

Результаты автоподбора вас не устроили.
Вы где-то нашли команды (стратегии), но проверять каждую вручную очень глупое и утомительное занятие.

В таком случае: 
- Перейдите в пункт **«Подбор команд (Beta)»**[^1]

     <img src="/images/point_to_podbor.png" width="200">

- Перейдите в **настройки Подбора** (шестерёнка справа сверху)

   <img src="/images/proxytest_settings.png" width="200">

- Активируйте переключатель **Свой список стратегий**

   <img src="/images/setting_custom_strat.png" width="200">

- Нажмите на пункт **Список стратегий**

- Откроется окно

   <img src="/images/window_custom_strat.png" width="200">

- В данное окно необходимо ввести свой список стратегий

> [!IMPORTANT]
> Каждая новая стратегия должна быть на **новой строке**. Команды (стратегии) **нельзя** разделять какими-либо символами (запятые, точки и т.д.) - стратегии разделяются **новой строкой**

- После ввода стратегий, нажмите **OK**

   <img src="/images/custom_strat.png" width="200">

- Вернитесь в пункт **Подбор стратегий (Beta)** и нажмите на кнопку «Начать проверку». После этого начнётся проверка стратегий, которые вы вставили в список

- Дождитесь окончания проверки и действуйте дальше как при [стандартной настройке](/docs/start/#setting). Если подбор вылетает - решение [здесь](/docs/problems/#crash-proxy-test).

## Списки доменов для подбора {#domain-list}

Перейдите в раздел меню: **Списки**.

<img src="/images/point_to_domains.png" width="200">

В приложение вшиты несколько списков доменов для подбора стратегий.

<img src="/images/domain_list.png" width="200">

<img src="/images/domain_list_menu.png" width="200">

На данный момент в приложении реализованы несколько списков *(нажмите на каждый, чтобы открыть и посмотреть)*:
<details>
<summary>Cloudflare</summary>

```
cloudflare.net
cloudflare.com
cloudflarecn.net
cloudflare-ech.com
```

</details>
<details>
<summary>Discord</summary>

```
dis.gd
discord.co
discord.gg
discord.app
discord.com
discord.dev
discord.new
discord.gift
discord.gifts
discord.media
discord.store
discord.design
discordapp.com
discordcdn.com
discordsez.com
discordsays.com
discordmerch.com
discordpartygames.com
discordactivities.com
stable.dl2.discordapp.net
discord-attachments-uploads-prd.storage.googleapis.com
```

</details>

<details>
<summary>General</summary>

```
rutracker.org
nyaa.si
rutor.org
nnmclub.to
speedtest.net
ookla.com
```

</details>

<details>
<summary>Googlevideo</summary>

```
rr1---sn-4axm-n8vs.googlevideo.com
rr1---sn-gvnuxaxjvh-o8ge.googlevideo.com
rr1---sn-ug5onuxaxjvh-p3ul.googlevideo.com
rr1---sn-ug5onuxaxjvh-n8v6.googlevideo.com
rr4---sn-q4flrnsl.googlevideo.com
rr10---sn-gvnuxaxjvh-304z.googlevideo.com
rr14---sn-n8v7kn7r.googlevideo.com
rr16---sn-axq7sn76.googlevideo.com
rr1---sn-8ph2xajvh-5xge.googlevideo.com
rr1---sn-gvnuxaxjvh-5gie.googlevideo.com
rr12---sn-gvnuxaxjvh-bvwz.googlevideo.com
rr5---sn-n8v7knez.googlevideo.com
rr1---sn-u5uuxaxjvhg0-ocje.googlevideo.com
rr2---sn-q4fl6ndl.googlevideo.com
rr5---sn-gvnuxaxjvh-n8vk.googlevideo.com
rr4---sn-jvhnu5g-c35d.googlevideo.com
rr1---sn-q4fl6n6y.googlevideo.com
rr2---sn-hgn7ynek.googlevideo.com
rr1---sn-xguxaxjvh-gufl.googlevideo.com
```

</details>

<details>
<summary>Social</summary>

```
snapchat.com
snap.com
linkedin.com
facebook.com
fb.com
fb.me
fbcdn.net
messenger.com
meta.com
instagram.com
static.cdninstagram.com
proton.me
medium.com
x.com
twitter.com
soundcloud.com
telegram.org
whatsapp.com
```

</details>

<details>
<summary>Youtube</summary>

```
youtu.be
youtube.com
i.ytimg.com
i9.ytimg.com
yt3.ggpht.com
yt4.ggpht.com
googleapis.com
jnn-pa.googleapis.com
googleusercontent.com
signaler-pa.youtube.com
youtubei.googleapis.com
manifest.googlevideo.com
yt3.googleusercontent.com
```

</details>

Каждый отдельный список можно добавить в проверку стратегий, отметив его (квадратик справа от списка). 
При нажатии на список открывается меню:

<img src="/images/domain_popup_menu.png" width="200">

- **Редактировать** - редактировать список (добавить/убрать домены). Не рекомендуется делать с встроенными списками.
- **Копировать** - скопировать список в буфер обмена.
- **Удалить** - удалить список. **КРАЙНЕ** не рекомендуется делать с встроенными доменами.

Также к этим спискам можно добавить пользовательские. Для этого нажмите на строку сверху "Добавить список". Появится меню:

<img src="/images/domain_custom_menu.png" width="200">

В строку `Название списка` введите название вашего списка.

В строку `Домены, каждый с новой строки` введите домены необходимого сервиса, каждый с новой строки.

После этого сохраните пользовательский список кнопкой ОК.

> [!TIP]
> Помните, крупные сайты и ресурсы для своей корректной работы могут требовать достаточно большое количество доменов.

Домены для различных сервисов можно найти [здесь](https://www.netify.ai/resources/applications), в этом [репозитории](https://github.com/v2fly/domain-list-community) или на этом [сайте](https://iplist.opencck.org/).

Если вы хотите сами выяснить какие домены используются: в этой [статье](https://itdog.info/analiziruem-trafik-i-opredelyaem-domeny-kotorye-ispolzuyut-sajty-i-prilozheniya/) подробно рассказывается про сниффинг трафика на различных устройствах и системах.

## Разблокировать свои ресурсы {#unlock-more-services}

Как уже было сказано, по умолчанию подбор стратегий проверяет стратегии на доменах ютуб и гуглвидео. Это можно изменить, чтобы проверять стратегии под ваши ресурсы:

- Перейдите в **настройки подбора**.

     <img src="/images/proxytest_settings.png" width="200">
    
     <img src="/images/domain_list.png" width="200">
    
- Выберите необходимые списки. При необходимости добавьте пользовательские, как описано [тут](#domain-list).

- После этого ищите стратегию [аналогичным образом](/docs/start/#setting), которым искали стратегию для YouTube.

> [!WARNING]
> Если у всех стратегий 0% - скорее всего ресурс заблокирован по IP и ByeByeDPI здесь ничем не сможет помочь.

## Экспорт и импорт настроек {#export-import}

Чтобы экспортировать или импортировать настройки, зайдите в **_основные настройки ByeByeDPI_** (шестерёнка справа внизу):

<img src="/images/point_to_settings_1.png" width="200">

- Нажмите на три точки в верхнем правом углу

   <img src="/images/dots.png" width="200">

> [!WARNING]
> С версии 1.4.2 используется другой формат файла. Настройки с более старых версий не получится импортировать.

- Выберите экспорт/импорт в зависимости от того что вам нужно (экспорт или импорт). Все настройки экспортируются в файл в формате `json`. При импорте необходимо указать данный файл.

   <img src="/images/export_import.png" width="200">

[^1]: Подбор команд находится в разработке. Могут быть ошибки. **Стратегии не генерируются автоматический** - они всегда одни и те же. В текущей реализации подбор по сути ничего не подбирает - он просто проверяет работу набора стратегий, которые были добавлены в него разработчиком.
