# Vayaan Labs plugins

**Add one catalogue to Claude Code and get every Vayaan Labs plugin, kept in sync.**

This is a plugin marketplace: a list that Claude Code reads so you can install plugins by name instead of hunting for each repository. Add it once, then install what you want from it. Today it carries Cache Maxxer, a plugin that shows your Claude Code prompt cache above the input box, explains every cache break and cache expiry, and can keep the cache warm to cut Claude Code cost.

![The Cache Maxxer band above the input box in a terminal: a green countdown at 58:53 with a track, a 100% hit rate on the last request and 89% over the session, 38K tokens of context, 67K read and 8.4K written, about $0.10 saved, and the buttons Keep warm: on, Warm now and Details.](assets/band.png)

## Plugins

| Plugin | What it does |
|---|---|
| [Cache Maxxer](https://github.com/vayaan-labs/cache-maxxer) | Shows the prompt cache's countdown and hit rate above the input box, explains every cache break and cache expiry, and can keep the cache warm to cut Claude Code cost. Install it as `cache-maxxer@vayaan-labs`. |

## Get started

1. **Add the catalogue.** In the Claude desktop app, open the Directory, choose Plugins, press the + button at the top right and choose Add marketplace, then Add from a repository ("Sync a plugin marketplace from a GitHub repository or Git URL"). Enter `vayaan-labs/claude-plugins`, or the full link `https://github.com/vayaan-labs/claude-plugins`.

   ![The Add marketplace dialog in the Claude desktop app, with two choices: Browse Anthropic sources, and Add from a repository, which syncs a plugin marketplace from a GitHub repository or Git URL.](assets/add-marketplace.png)

   In a terminal, run `claude plugin marketplace add vayaan-labs/claude-plugins` instead.

2. **Install a plugin.** In the Desktop app, find the plugin in the Vayaan Labs catalogue and install it. In a terminal, run `claude plugin install cache-maxxer@vayaan-labs`, using the plugin's name from the table above.

3. **Use it.** If Claude Code was already open when you installed, run `/reload-plugins` in that session, or start a new one. Each plugin's own page says what to expect.

Tested with Claude Code 2.1.289 on macOS, in the terminal. The Desktop app route follows the app's own labels but has not been run by us yet.

## Updates

Run `claude plugin marketplace update vayaan-labs` to pull the latest catalogue, then `claude plugin update cache-maxxer@vayaan-labs` for a plugin, and restart Claude Code to apply it.

## Removing things

To remove a plugin, run `claude plugin uninstall cache-maxxer@vayaan-labs`. To remove the whole catalogue, run `claude plugin marketplace remove vayaan-labs`.

## Privacy

The catalogue is a single file, `.claude-plugin/marketplace.json`, that names each plugin and where its code lives on GitHub. It has no server and runs nothing. Claude Code fetches it from GitHub when you add or update the catalogue, and fetches a plugin's repository from GitHub when you install it. What a plugin does once installed is described on that plugin's own page; for Cache Maxxer, see its Privacy section.

## Get help

Open an issue at https://github.com/vayaan-labs/claude-plugins/issues. To report a security problem privately, see [SECURITY.md](SECURITY.md).

## Checking the catalogue

```
claude plugin validate --strict .claude-plugin/marketplace.json
```

MIT licensed. Built by @YaanFPV.
