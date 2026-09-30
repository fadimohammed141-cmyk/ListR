# ListR

ListR is a Discord bot for managing personal anime lists directly through Discord and tracking your total number of watched episodes.

## Commands

### `/addanime`

Adds an anime to your ListR collection.

This command has 3 required options:

| Option | Description |
|---|---|
| `title` | The name of the anime to add. |
| `category` | The list to add the anime to: `completed`, `watching`, or `interested`. |
| `episodes` | The number of episodes to add to your overall watched-episode total. |

**Important:** The `episodes` value is **not tied to the anime title whatsoever**. It is only used to track your **total number of episodes watched overall**.

For `completed` and `watching`, enter the number of episodes you want to add to your overall watched-episode total. For `interested`, use `0`.

### `/animestats`

Displays your ListR anime lists, including:

- Completed
- Watching
- Interested
- Total number of episodes recorded as watched

The episode total is a separate global counter. It is **not associated with any anime name**.

### `/animereset`

Resets or modifies existing ListR data.

The first required option is `reset-wat`. It determines what the command will affect:

| `reset-wat` option | What it does | Required additional option |
|---|---|---|
| `all` | Resets all of your ListR data, including anime lists and the global episode total. | None |
| `category` | Resets a specific anime category/list. | `category` |
| `anime` | Removes a specific anime from your lists. | `anime` |
| `episodes` | Removes a specified number from the global watched-episode total. | `episode` |

The command has 3 additional options: `anime`, `category`, and `episode`.

These options are technically optional command parameters, but they are conditionally required depending on the selected `reset-wat` value:

- **`anime`** — Required only when `reset-wat` is `anime`. It specifies which anime to remove.
- **`category`** — Required only when `reset-wat` is `category`. It specifies which category/list to reset.
- **`episode`** — Required only when `reset-wat` is `episodes`. It specifies how much to change the global episode total.
- **`all`** — Requires none of the additional options.

**Important:** With `reset-wat=episodes`, the `episode` value affects the **global watched-episode total**, not any particular anime. A negative value adds episodes instead of removing them. For example, entering `-5` adds 5 to the overall watched-episode total.

## Data & Privacy

ListR is designed to store only the data required for its anime-list functionality.

Its persistent ListR variables store only:

- **User IDs**, and only where a User ID is required to associate data with the correct user.
- **Anime names**.
- **Episode numbers**, used as the overall watched-episode total and not tied to anime names.
- **Chosen options** used by ListR's functionality, such as selected categories or reset options.

These are the only categories intentionally stored in ListR's persistent variables.

ListR does **not** intentionally store Discord server IDs, usernames or display names, avatars, message content, passwords, authentication tokens, payment information, IP addresses, precise location information, voice/video data, or unrelated personal information in its persistent ListR variables.

For the complete rules governing data collection and use, see the [Privacy Policy](Privacy%20Policy/PRIVACY_POLICY.txt).

For the terms governing use of ListR, see the [Terms of Service](Terms%20of%20Service/TERMS_OF_SERVICE.txt).

## Important

ListR is an independent third-party Discord application. It is not affiliated with, endorsed by, or sponsored by Discord Inc.
