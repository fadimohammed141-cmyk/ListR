# ListR

ListR is a Discord bot for managing personal anime lists directly through Discord.

## Commands

### `/addanime`

Adds an anime to your ListR collection.

This command has 3 required options:

| Option | Description |
|---|---|
| `title` | The name of the anime to add. |
| `category` | The list to add the anime to: `completed`, `watching`, or `interested`. |
| `episodes` | The number of episodes watched. Use `0` when the category is `interested`. |

For `completed` and `watching`, enter the number of episodes you have watched. For `interested`, enter `0`.

### `/animestats`

Displays your ListR anime lists, including:

- Completed
- Watching
- Interested

The displayed information is based on the anime names, episode numbers, and category information associated with your lists.

### `/animereset`

Resets or modifies existing anime-list data.

The first required option is `reset-wat`. It determines what the command will affect:

| `reset-wat` option | What it does | Required additional option |
|---|---|---|
| `all` | Resets all of your ListR anime data. | None |
| `category` | Resets a specific anime category/list. | `category` |
| `anime` | Removes a specific anime from your lists. | `anime` |
| `episodes` | Removes a specified number of episodes from a specific anime. | `anime` and `episode` |

The command has 3 additional options: `anime`, `category`, and `episode`.

These options are technically optional command parameters, but they are required when the corresponding `reset-wat` value is selected:

- **`anime`** — Required when `reset-wat` is `anime` or `episodes`. Specifies which anime the command should affect.
- **`category`** — Required when `reset-wat` is `category`. Specifies which category/list should be reset.
- **`episode`** — Required when `reset-wat` is `episodes`. Specifies the number of episodes to remove.

If `reset-wat` is `all`, none of the three additional options are required.

**Important:** When using `episodes`, use a **negative number to add episodes** instead of removing them. For example, `-5` adds 5 episodes.

## Data & Privacy

ListR is designed to store only the data required for its anime-list functionality.

Its persistent ListR variables store only:

- **User IDs**, and only where a User ID is required to associate data with the correct user.
- **Anime names**.
- **Episode numbers**.
- **Chosen options** used by ListR's functionality, such as selected categories or reset options.

ListR does **not** intentionally store Discord server IDs, usernames, message content, passwords, authentication tokens, payment information, or other personal information in its persistent ListR variables.

For the complete rules governing data collection and use, see the [Privacy Policy](Privacy%20Policy/PRIVACY_POLICY.txt).

For the terms governing use of ListR, see the [Terms of Service](Terms%20of%20Service/TERMS_OF_SERVICE.txt).

## Important

ListR is an independent third-party Discord application. It is not affiliated with, endorsed by, or sponsored by Discord Inc.
