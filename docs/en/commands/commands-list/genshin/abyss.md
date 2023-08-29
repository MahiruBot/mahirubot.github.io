---
title: «Genshin Abyss» command
tags:
  - Command
  - Inline command
  - Genshin
  - Image
  - Version 1.0.0
---

# «Genshin Abyss» command

View your or someone's Spiral Abyss statistics.

### Arguments

**user, u**  `mention (optional)` — User whose statistics you want to view. Leave empty to view your statistics.

**schedule, s** `Literal[current, previous] (optional)` — Whether you wan to view statistics for `current` _(default)_ or `previous` schedule.

### Examples

#### Default
+ `/genshin_abyss`
+ `/genshin_abyss @jokelbaf`
+ `/genshin_abyss --u: jokelbaf --s: previous`

#### Inline
+ `@MahiruShiinaBot genshin_abyss`
+ `@MahiruShiinaBot genshin_abyss: @jokelbaf`
+ `@MahiruShiinaBot genshin_abyss: --schedule: previous`