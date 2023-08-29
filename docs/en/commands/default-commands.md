# Default commands

Default commands are the one starting with `/`. They can be used both in groups and your private chat with Mahiru.

???+ note "Note"

    All commands in groups must include bot mention like the following: `/help@MahiruShiinaBot`. 
    Mahiru will not respond to your command in a group if it does not include her mention. 
    This was made to prevent conflicts between bots in the same group that have similar commands.

## Arguments

Most commands have at least one argument, some commands can not be executed without passing required arguments. In order to pass an argument, you need to use certain syntax which is `--argument: value`. All arguments have short aliases like `--arg: value`. Use `/help command` to view information about command and a list of arguments it has.

???+ tip "Tip"

    As you type a command, a list of suggestions will appear. On mobile, hold down a suggestion 
    to autofill your message. On a PC, use ++up++ or ++down++ to select from the list, then press ++tab++ to 
    autofill the chosen command.

### Arguments types

Every argument has it's own type. This means you can't, for example, use string if type of the argument is number.

| Type        | Description                                             | Example values          |
| ----------- | ------------------------------------------------------- | ----------------------- |
| `string`    | String containing letters, characters, numbers etc.     | `Hello world!`          |
| `number`    | Any integer or float number.                            | `234`, `-0.5`           |
| `boolean`   | `True` or `False`. Short forms `t` and `f` can be used. | `true`, `f`             |
| `mention`   | Mention of the user. They must have used Mahiru before. | `@jokelbaf`             |
| `url`       | Any HTTPS url matching the purpose of the command.      | `https://example.com`   |
| `Literal`   | Fixed list of allowed values for the argument.          | `gpt-3.5-turbo`, `neko` |

At times, specific ranges of numbers are permissible. In such instances, you'll encounter entries like `[-1, 2]` instead of the actual type. This indicates that any number within the range of `-1` to `2`, inclusive of both `-1` and `2`, is acceptable.

If you see `(optional)` near the argument type, the argument is not a required one. This allows the command to be executed successfully even if you choose not to pass this particular argument.
