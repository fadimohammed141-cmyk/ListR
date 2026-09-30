# ListR

ListR is a Discord bot for creating and managing personal anime lists.

## Commands

### /addanime

Adds an anime to your ListR collection.

It has 3 required options:

- **title** — The name of the anime you want to add.
- **category** — The list the anime should be added to. Choose **Completed**, **Watching**, or **Interested**.
- **episodes** — The number of episodes you have watched.
  - For **Completed**, enter the number of episodes you have watched.
  - For **Watching**, enter the number of episodes you have watched.
  - For **Interested**, enter **0**.

### /animestats

Displays all of your anime lists and their stored information, including your **Completed**, **Watching**, and **Interested** lists.

### /animereset

Resets or modifies anime data in your ListR collection.

Its first required option is **reset-wat**, which determines what you want to reset:

- **all** — Resets everything in your ListR data.
- **category** — Resets a specific anime category/list.
- **anime** — Removes a specific anime from your lists.
- **episodes** — Removes a set amount of episodes from a specific anime.

**Important note:** When using **episodes**, enter a **negative value** to add episodes instead of removing them. For example, entering `-5` adds 5 episodes.

## Privacy & Terms

- [Privacy Policy](Privacy%20Policy/PRIVACY_POLICY.txt)
- [Terms of Service](Terms%20of%20Service/TERMS_OF_SERVICE.txt)
