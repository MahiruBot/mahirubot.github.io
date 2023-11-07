---
title: Команда «Mangalist»
tags:
  - Команда
  - Встроенная команда
  - Версия 1.0.0
---

# Команда «Mangalist»

Посмотреть список запланированной/прочитанной/избранной манги.

### Аргументы

**list, l**  `Литерал[favorites, planned, read]` — Список который вы хотите просмотреть. Этот аргумент применим только для обычной команды, он отсутствует во встроенной.

**user, u** `упоминание (опционально)` — Пользователь, чей список вы хотите просмотреть.

### Примеры

#### Обычная команда
+ `/mangalist watched`
+ `/mangalist --l: favorites --user: @jokelbaf`

#### Встроенная команда
+ `@MahiruShiinaBot mangalist`[^1]
+ `@MahiruShiinaBot mangalist: --u: jokelbaf`

[^1]: Во встроенной команде аргумент `list` отсутствует. После того как вы напишите команду **mangalist**, Махиру предложит выбрать вам список из результатов встроенного запроса.