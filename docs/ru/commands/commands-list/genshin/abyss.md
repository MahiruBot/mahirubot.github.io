---
title: Команда «Genshin Abyss»
tags:
  - Команда
  - Встроенная команда
  - Геншин
  - Изображение
  - Версия 1.0.0
---

# Команда «Genshin Abyss»

Просмотр статистики Витой Бездны.

### Аргументы

**user, u**  `упоминание (опционально)` — Пользователь, чью статистику вы хотите посмотреть. Оставьте аргумент пустым для просмотра своей статистики.

**schedule, s** `Литерал[current, previous] (опционально)` — Фаза. Может быть `current` (текущей) _(по умолчанию)_ либо `previous` (предыдущей).

### Примеры

#### Обычная команда
+ `/genshin_abyss`
+ `/genshin_abyss @jokelbaf`
+ `/genshin_abyss --u: jokelbaf --s: previous`

#### Встроенная команда
+ `@MahiruShiinaBot genshin_abyss`
+ `@MahiruShiinaBot genshin_abyss: @jokelbaf`
+ `@MahiruShiinaBot genshin_abyss: --schedule: previous`