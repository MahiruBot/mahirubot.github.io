---
title: Команда «Imgtotext»
tags:
  - Команда
  - Встроенная команда
  - Версия 1.0.0
---

# Команда «Imgtotext»

Получить любой текст с любого изображения и отправить его в чат. Полезно в сочетании с командой `/gpt`, когда вам нужно что-то спросить о тексте на изображении.

### Аргументы

**url, u** `ссылка (опционально)` — Ссылка на изображение, с которого вы хотите получить текст. Если аргумент не указан, Махиру попросит вас отправить изображение в виде файла.

???+ warning "Предупреждение"

    При отправке изображения в виде файла не забудьте отключить его сжатие. В ПК-клиенте: снимите галочку со **«Сжать изображение»**. В мобильном клиенте: нажмите кнопку **«:octicons-paperclip-24:»**, затем кнопку **«:octicons-file-24: Файл»** и выберите изображение из галереи.

### Примеры

#### Обычная команда
+ `/imgtotext`
+ `/imgtotext https://example.com/image.png`

#### Встроенная команда
+ `@MahiruShiinaBot imgtotext: https://example.com/image.png`
+ `@MahiruShiinaBot imgtotext: --url: https://example.com/image.png`