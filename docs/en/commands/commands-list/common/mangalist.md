---
tags:
  - Command
  - Inline command
  - Version 1.0.0
---

# Mangalist

View your or someone's list of planned/read/favorites manga.

### Arguments

**list, l**  `Literal[favorites, planned, read]` — The list you want to view. This argument is only present in a default command, not inside the inline.

**user, u** `mention (optional)` — The user whose list you want to view.

### Examples

#### Default
+ `/mangalist read`
+ `/mangalist --l: favorites --user: @jokelbaf`

#### Inline
+ `@MahiruShiinaBot mangalist`[^1]
+ `@MahiruShiinaBot mangalist: --u: jokelbaf`

[^1]: In inline mode `list` argument is not present. After you type **mangalist** command, Mahiru will suggest you to choose the desired list from inline results.