---
title: Команда «Animelist»
tags:
  - Команда
  - Встроенная команда
  - Версия 1.0.0
---

# Команда «Animelist»

Посмотреть список запланированного/просмотренного/избранного аниме.

### Аргументы

**list, l**  `Литерал[favorites, planned, watched]` — Список который вы хотите просмотреть. Этот аргумент применим только для обычной команды, он отсутствует во встроенной.

**user, u** `упоминание (опционально)` — Пользователь, чей список вы хотите просмотреть.

### Примеры

#### Обычная команда
+ `/animelist watched`
+ `/animelist --l: favorites --user: @jokelbaf`

#### Встроенная команда
+ `@MahiruShiinaBot animelist`[^1]
+ `@MahiruShiinaBot animelist: --u: jokelbaf`

[^1]: Во встроенной команде аргумент `list` отсутствует. После того как вы напишите команду **animelist**, Махиру предложит выбрать вам список из результатов встроенного запроса.