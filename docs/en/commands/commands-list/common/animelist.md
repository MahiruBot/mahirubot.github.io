---
tags:
  - Command
  - Inline command
  - Version 1.0.0
---

# Animelist

View your or someone's list of planned/watched/favorites anime.

### Arguments

**list, l**  `Literal[favorites, planned, watched]` — The list you want to view. This argument is only present in a default command, not inside the inline.

**user, u** `mention (optional)` — The user whose list you want to view.

### Examples

#### Default
+ `/animelist watched`
+ `/animelist --l: favorites --user: @jokelbaf`

#### Inline
+ `@MahiruShiinaBot animelist`[^1]
+ `@MahiruShiinaBot animelist: --u: jokelbaf`

[^1]: In inline mode `list` argument is not present. After you type **animelist** command, Mahiru will suggest you to choose the desired list from inline results.