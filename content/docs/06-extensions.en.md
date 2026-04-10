---
title: Advanced Settings
weight: 5
---

> [!WARNING]
> These settings are **exclusive** to the ByeByeDPI program! They should not be taken as byedpi arguments and inserted into other programs.
> Also, don't share such settings with other people online, as their values **strongly depend** on the ByeByeDPI program settings.

> [!CAUTION]
> These settings are intended for users who understand the tool. If you don't understand what auto-selection, strategies, parameters, flags are, etc - don't blindly click around. This page won't help you.

### SNI of fake packet

In the auto-selection settings, there's a function to change the SNI for the fake packet. By default it's set to `google.com`, but it can be changed to any other.

Changing it makes sense if you've carefully thought out the bypass method and are sure that your filter checks packets for SNI from the "Whitelist".

> [!CAUTION]
> Don't change SNI to a host from the blocked list (for example, youtube.com or googlevideo.com) - this will only make the filter understand that you're DEFINITELY trying to access something blocked.

Built-in strategies automatically pick up SNI from settings. If you want your strategy to support this feature - you should specify the `{sni}` parameter for the `-n` flag, like this:

```
-n {sni}
```

Then [pass](03-features.md) the modified strategy to auto-selection.

### Replacing proxy lists {#replace-proxy-lists}

In byedpi, there are filtering functions that accept various lists: `-H` and `-j`.

To pass domain/subnet lists to them, you need to insert them according to byedpi rules, like this:

```
-H:"domain1.com domain2.com domain3.com domain4.com domain5.com ..."
```

With a large list of domains, this option can be inconvenient. ByeByeDPI (from version 1.7.3) adds a custom parameter `{list}`.

> [!TIP]
> This parameter works for both auto-selection and command line. If you apply such a strategy - it will be converted to one that byedpi can read before sending.

To use it, you need to specify the ID (name, for example Cloudflare from built-in) of the domain/subnet list from [auto-selection settings](03-features.md). You can create your own list and specify its name. It should look like this:

```
-H:"{list:Cloudflare}"
```
or
```
-j:"{list:subnets}"
```
The second will work ONLY if you have a subnet list named `subnets` in the [domain settings](03-features.md) section.
