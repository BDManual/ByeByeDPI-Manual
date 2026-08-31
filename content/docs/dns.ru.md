---
title: DNS
weight: 3
---

## Зачем настраивать DNS

Перехват или нестабильная работа DNS может мешать открытию сайтов и подбору стратегий. Проверить используемые DNS-серверы можно на [browserleaks.com/dns](https://browserleaks.com/dns).

На Android 9 и новее рекомендуется настроить DNS over TLS на уровне системы. Если рабочий DoT или DoH уже настроен в операционной системе, в ByeByeDPI лучше выбрать системный DNS.

> [!NOTE]
> Поле DNS в ByeByeDPI принимает DNS в формате IPv4. DoT и DoH следует настраивать на уровне системы или приложения, которое их поддерживает. При подборе стратегий используется системный DNS.

## Если DoT или DoH настроить нельзя

Если нет возможности или желания настраивать DoT или DoH, попробуйте указать другой DNS в ByeByeDPI либо выбрать системный DNS.

Обычные DNS-запросы не шифруются и хуже защищены от перехвата или подмены, чем DoT и DoH.

## DNS over TLS

Укажите в системе частный DNS:

<img src="/images/dns-01.png" width="200">

<img src="/images/dns-02.png" width="200">

Обычные серверы:

- `dns.google`
- `one.one.one.one`
- `dns.quad9.net`
- `dot.sb`
- `unfiltered.adguard-dns.com`
- `dns.adguard-dns.com`

## DNS over HTTPS

Обычные серверы:

- `https://dns.google/dns-query`
- `https://cloudflare-dns.com/dns-query`
- `https://dns.quad9.net/dns-query`
- `https://doh.dns.sb/dns-query`
- `https://doh.opendns.com/dns-query`
- `https://dns.adguard-dns.com/dns-query`

DoH обычно настраивается в браузере или отдельном приложении. Android не предоставляет единую системную настройку DoH, аналогичную системному частному DNS для DoT.

## Нестабильность DNS в России

У части пользователей в России DNS-серверы Google, Cloudflare и некоторые другие, включая DoH и DoT, могут работать нестабильно или быть недоступны.

Если перестали открываться сайты или появилась ошибка DNS, попробуйте другой сервер из списка. Если рабочий DoH или DoT уже настроен в операционной системе, выберите в ByeByeDPI системный DNS.

> [!WARNING]
> Некоторые DNS-серверы фильтруют рекламу, взрослый контент или другие категории сайтов. Это может выглядеть как проблема ByeByeDPI.

## Проксирующие DNS {#proxying-dns}

Проксирующие DNS отличаются от обычных резолверов: они могут помочь с географическими ограничениями отдельных сервисов, например нейросетей. Они не заменяют ByeByeDPI и не обходят блокировки по белым спискам.

DoH-серверы для сервисов с географическими ограничениями:

- `https://xbox-dns.ru/dns-query`
- `https://dns.comss.one/dns-query`
- `https://dns.malw.link/dns-query`

DoT-серверы для сервисов с географическими ограничениями:

- `xbox-dns.ru`
- `dns.comss.one`
- `dns.malw.link`

> [!CAUTION]
> Используйте только те DNS-серверы, которым доверяете. Проксирующий DNS может быть нестабилен, поэтому не стоит без необходимости назначать его для всей системы: при отказе сервера может пропасть доступ к сайтам.

Подробнее о возможностях Comss DNS можно прочитать на [странице проекта](https://www.comss.ru/page.php?id=7315).

Дополнительные публичные списки:

- [DNS Privacy Project](https://dnsprivacy.org/public_resolvers/#dns-over-tls-dot)
- [Провайдеры DNS в AdGuard Knowledge Base](https://adguard-dns.io/kb/ru/general/dns-providers/)
- [DNSCrypt Public Resolvers](https://dnscrypt.info/public-servers/)
- [DNS over HTTPS в документации curl](https://github.com/curl/curl/wiki/DNS-over-HTTPS)
