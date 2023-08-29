---
title: «Help» command
tags:
  - Command
  - Inline command
  - Version 1.0.0
---

# «Help» command

View info about any command that Mahiru has.

### Arguments

**command, c**  `string (optional)` — Command you need help with. If not passed, general info about Mahiru will be displayed.

**inline,i**  `boolean (optional)` — Whether you want to view info about inline or slash command.

### Examples

#### Default
+ `/help`
+ `/help gpt`
+ `/help --c: gif`

#### Inline
+ `@MahiruShiinaBot help`
+ `@MahiruShiinaBot help: waifu`
+ `@MahiruShiinaBot help: --command: song`