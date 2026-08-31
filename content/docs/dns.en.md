---
title: DNS
weight: 3
---

## Why configure DNS

DNS hijacking or an unstable resolver can prevent websites from opening and interfere with strategy testing. You can check which resolvers are in use at [browserleaks.com/dns](https://browserleaks.com/dns).

On Android 9 and newer, it is recommended to configure DNS over TLS at the system level. If working DoT or DoH is already configured in the operating system, select system DNS in ByeByeDPI.

> [!NOTE]
> The DNS field in ByeByeDPI accepts an IPv4 DNS address. Configure DoT and DoH at the system level or in an application that supports them. Strategy testing uses system DNS.

## If DoT or DoH is not an option

If you cannot or do not want to configure DoT or DoH, try another DNS address in ByeByeDPI or select system DNS.

Regular DNS queries are not encrypted and are less protected against interception or modification than DoT and DoH.

## DNS over TLS

Configure a private DNS hostname in the system:

<img src="/images/dns-1.jpg" width="200">

<img src="/images/dns-2.jpg" width="200">

Regular resolvers:

- `dns.google`
- `one.one.one.one`
- `dns.quad9.net`
- `dot.sb`
- `unfiltered.adguard-dns.com`
- `dns.adguard-dns.com`

## DNS over HTTPS

Regular resolvers:

- `https://dns.google/dns-query`
- `https://cloudflare-dns.com/dns-query`
- `https://dns.quad9.net/dns-query`
- `https://doh.dns.sb/dns-query`
- `https://doh.opendns.com/dns-query`
- `https://dns.adguard-dns.com/dns-query`

DoH is usually configured in a browser or a separate application. Android does not provide a single system-wide DoH setting equivalent to Private DNS for DoT.

## DNS instability in Russia

For some users in Russia, Google, Cloudflare, and some other DNS resolvers, including DoH and DoT, may be unstable or unavailable.

If websites stop opening or you see a DNS error, try another resolver. If working DoH or DoT is already configured in the operating system, select system DNS in ByeByeDPI.

> [!WARNING]
> Some resolvers filter advertising, adult content, or other website categories. This may look like a ByeByeDPI problem.

## Proxying DNS {#proxying-dns}

Proxying DNS differs from a regular resolver: it may help with geographic restrictions imposed by individual services, such as AI services. It does not replace ByeByeDPI and cannot bypass an allowlist.

DoH resolvers for services with geographic restrictions:

- `https://xbox-dns.ru/dns-query`
- `https://dns.comss.one/dns-query`
- `https://dns.malw.link/dns-query`

DoT resolvers for services with geographic restrictions:

- `xbox-dns.ru`
- `dns.comss.one`
- `dns.malw.link`

> [!CAUTION]
> Use only resolvers you trust. A proxying resolver may be unstable, so avoid setting it system-wide unless necessary: if it goes down, access to websites may stop working.

Read more about Comss DNS on the [project page](https://www.comss.ru/page.php?id=7315).

Additional public lists:

- [DNS Privacy Project](https://dnsprivacy.org/public_resolvers/#dns-over-tls-dot)
- [DNS providers in the AdGuard Knowledge Base](https://adguard-dns.io/kb/general/dns-providers/)
- [DNSCrypt Public Resolvers](https://dnscrypt.info/public-servers/)
- [DNS over HTTPS in the curl documentation](https://github.com/curl/curl/wiki/DNS-over-HTTPS)
