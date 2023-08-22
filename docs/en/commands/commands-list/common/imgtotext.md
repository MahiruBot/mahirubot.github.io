---
tags:
  - Command
  - Inline command
  - Version 1.0.0
---

# Imgtotext

Read any text from any image and send it to the chat. Works good in combination with `/gpt` command when you need to ask something about text in an image.

### Arguments

**url, u** `url (optional)` — Url to the image you want to read text from. If not passed, Mahiru will ask you to send your image as a file.

???+ warning "Warning"

    When sending image as a file remember to disable image compression. In PC client: remove tick from **«Compress the image»** checkbox. In mobile client: Click **«:octicons-paperclip-24:»** button, then click **«:octicons-file-24: File»** button and select your image from the gallery.

### Examples

#### Default
+ `/imgtotext`
+ `/imgtotext https://example.com/image.png`

#### Inline
+ `@MahiruShiinaBot imgtotext: https://example.com/image.png`
+ `@MahiruShiinaBot imgtotext: --url: https://example.com/image.png`