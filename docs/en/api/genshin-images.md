# Genshin Images API

Mahiru provides you with a cool images API which you can use after connecting your Genshin account. It allows you to create direct links to Genshin images which are updated in real-time.

## URL Structure

The base URL of Genshin Images API is:
```yaml
https://mahiru.one/g/
```

URL structure looks like this:
```yaml
https://mahiru.one/g/{userId}/{method}
```

- **userId** – Telegram ID of the user whose image you want to access. You can get it [here](../dashboard/pages/settings/for-developers.md).

- **method** – The method you want to use. See the table below for the list of all available methods. 

## Methods

Each method corresponds to a specific genshin command. See the list of all commands that have methods in Genshin Images API below.

Some methods always require authentication. Read about it in [Privacy and Security](#privacy-and-security) section.

| Method        | Command                                                                   | URL Structure                                     | Requires authentication |
| ------------- | ------------------------------------------------------------------------- | ------------------------------------------------- | ----------------------- |
| `profile`     | [`genshin_profile`](../commands/commands-list/genshin/profile.md)         | `https://mahiru.one/g/{userId}/profile`           | :material-close: No     |
| `abyss`       | [`genshin_abyss`](../commands/commands-list/genshin/abyss.md)             | `https://mahiru.one/g/{userId}/abyss`             | :material-close: No     |
| `exploration` | [`genshin_exploration`](../commands/commands-list/genshin/exploration.md) | `https://mahiru.one/g/{userId}/exploration`       | :material-close: No     |
| `notes`       | [`genshin_notes`](../commands/commands-list/genshin/notes.md)             | `https://mahiru.one/g/{userId}/notes`             | :material-check: Yes    |
| `tcg`         | [`genshin_tcg`](../commands/commands-list/genshin/tcg.md)                 | `https://mahiru.one/g/{userId}/teapot`            | :material-close: No     |
| `teapot`      | [`genshin_teapot`](../commands/commands-list/genshin/teapot.md)           | `https://mahiru.one/g/{userId}/teapot`            | :material-close: No     |
| `characters`  | [`genshin_characters`](../commands/commands-list/genshin/characters.md)   | `https://mahiru.one/g/{userId}/characters`        | :material-close: No     |
| `character`   | [`genshin_characters`](../commands/commands-list/genshin/characters.md)   | `https://mahiru.one/g/{userId}/character/{characterId}`  | :material-close: No     |

## Query Parameters

Query parameters can help you configure the image you want to receive.

### Default Parameters

Default parameters are present in every method:

- **theme** `Literal['light', 'dark'] (optional)` – Theme for the image. Can be either `light` or `dark`.
- **language** `Literal['ru', 'en'] (optional)` – Language of the image. Can be set to `ru` (Russian) or `en` (English).
- **authkey** `string (optional)` – Your `authkey` for request authentication. Required for routes that either have authentication enabled by default or ones for which you have disabled [«Display to others»](../dashboard/pages/game-integrations/genshin.md#display-to-others) setting in Dashboard.

### Unique Parameters

Some methods have unique parameters:

| Method          | Parameters | Type                                        | Parameters description                                       |
| --------------- | ---------- | ------------------------------------------- | ------------------------------------------------------------ |
| `abyss`         | `schedule` | `Literal['current', 'previous'] (optional)` | Schedule of the image. Can be set to `current` or `previous` |

### Adding Parameters

To append query params to the end of a URL, a `?` is added followed immediately by a query parameter:
```yaml
https://mahiru.one/g/{userId}/{method}?language=en&theme=dark
```

## Privacy and Security

???+ Danger "Warning"

    You must not neither share URLs containing your `authkey` with anyone nor upload images using these URLs. Everyone who has your `authkey` may have unexpected access to your data stored by Mahiru. If you accidentally leaked your `authkey`, please contact us in our [Support Group](https://mahiru.one/community) in order to reset it as soon as possible.

If you want to prevent other users from accessing your images, you can do this by disabling [«Display to others»](../dashboard/pages/game-integrations/genshin.md#display-to-others) for methods you do not want to share. (1)
{ .annotate }

1. Some methods always require authentication. These are the ones you most likely won't want to share, for example, notes. See methods which always require authentication in [Methods Table](#methods).

In order to authenticate your request you need to add `authkey` as a query parameter of the URL:
```yaml
https://mahiru.one/g/{userId}/{method}?authkey=ABCDEFG12345
```

## Rate limits

Every endpoint (method) can be accessed 10 times/1 minute/IP. If you exceed this limit, your IP will be rate limited.

## Caching

Each image requires a significant amount of server resources to generate. Therefore, we use caching. Each method except `notes` has a cache time of one hour. For `notes` it is 3600 seconds (5 minutes).