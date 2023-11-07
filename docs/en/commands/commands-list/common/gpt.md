---
title: «GPT» command
tags:
  - Command
  - Inline command
  - Version 1.0.0
---

# «GPT» command

Ask ChatGPT a question or even make a conversation with one of the most popular OpenAI's text models!

**Available models:**

| Model Name       | Max Tokens | Price per 1000 tokens                           | Supports Conversation | Recommended           |
| ---------------- | ---------- | ----------------------------------------------- | --------------------- | --------------------- |
| gpt-4[^1]        | 8000       | USD 0.03 (prompt)<br> USD 0.06 (completion)     | :material-check: Yes  | :material-check: Yes  |
| gpt-3.5-turbo    | 4000       | USD 0.0015 (prompt)<br> USD 0.0020 (completion) | :material-check: Yes  | :material-check: Yes  |
| text-davinci-003 | 4000       | USD 0.0200                                      | :material-close: No   | :material-close: No   |

### Arguments

???+ tip "Configuring ChatGPT via Dashboard"

    You can configure ChatGPT in Mahiru's Dashboard in order to avoid passing all arguments every
    time you use `/gpt` command. After configuring arguments in the Dashboard you will still be able
    to pass any argument when using this command and it will override the configured value. 

**message, msg**  `string` — Your message to ChatGPT. May contain question, request etc.

**model, m** `Literal[gpt-3.5-turbo, ...] (optional)` — Text model which you wan to use.

**max-tokens, m-t** `number (optional)` — Limit max tokens used in request to API. This includes both your `message` tokens and ChatGPT's response tokens.

**temperature, t** `[0.0, 2.0] (optional)` — Lower values for temperature result in more consistent outputs, while higher values generate more diverse and creative results.

**presence-penalty, p-p** `[-2.0, 2.0] (optional)` — Positive values penalize new tokens based on whether they appear in the text so far, increasing the model's likelihood to talk about new topics.

**frequency-penalty, f-p** `[-2.0, 2.0] (optional)` — Positive values penalize new tokens based on their existing frequency in the text so far, decreasing the model's likelihood to repeat the same line verbatim.

**conversation, c** `boolean (optional)` — Whether to enable conversation mode or not. This argument can not be set to `true` when using inline command. `gpt-3.5-turbo` is the only model supporting conversation mode.

**stream, s** `boolean (optional)` — Stream response in real time via message editing. If set to `false`, the message will remain **"Loading..."** and will be edited to the actual response once received it from the API.

### Examples

#### Default
+ `/gpt Who is Mahiru Shiina?`
+ `/gpt --message: How large is the Moon? --t: 0.7 --p-p: 1.5`
+ `/gpt --msg: Write me an example of HTTP request in TypeScript. --stream: true`

#### Inline
+ `@MahiruShiinaBot gpt: Tell me about the anime called "Classroom of Elite".`
+ `@MahiruShiinaBot gpt: --msg: Write me a SQL SELECT query. --s: true`
+ `@MahiruShiinaBot gpt: --msg: Give me a recipe of a pancake. --model: gpt-4`

[^1]: GPT-4 Is not available for free public use yet. In order to use it you must set you own [API Key](../../../dashboard/pages/settings/commands/gpt.md#api-key) which supports GPT-4.