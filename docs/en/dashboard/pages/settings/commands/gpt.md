---
title: GPT Settings
tags:
  - Dashboard
  - Settings
  - Version 1.0.0
---

# GPT Settings

Customize arguments for [`/gpt`](../../../../commands/commands-list/common/gpt.md) command. This allows you to avoid passing them every time you run the command. You can still override arguments configured here by passing them in the command. For example, if temperature in the Dashboard is set to `0.5` and you do `/gpt --msg: whatever --temperature: 1`, the temperature value used be Mahiru is `1`.

## Settings

#### Conversation
Whether to enable conversation mode or not. This setting won't work when using inline command. `gpt-3.5-turbo` is the only model supporting conversation mode.

#### Stream
Stream response in real time via message editing. If disabled, the message will remain "Loading..." and will be edited to the actual response once received it from the API.

#### Model
Text model which you wan to use by default.

#### API Key
Allows you to set your own API Key and remove daily tokens limit. You can get your API Key [here](https://platform.openai.com/account/api-keys). You have $18 free usage for 3 month. After the period ends or you reach $18 usage, you may want to create a new account and get a new API Key or pay and use the old one.

#### Max tokens
Limit max tokens used in request to API. This includes both your message tokens and ChatGPT's response tokens.

#### Temperature
Lower values for temperature result in more consistent outputs, while higher values generate more diverse and creative results.

#### Presence penalty
Positive values penalize new tokens based on whether they appear in the text so far, increasing the model's likelihood to talk about new topics.

#### Frequency penalty
Positive values penalize new tokens based on their existing frequency in the text so far, decreasing the model's likelihood to repeat the same line verbatim.