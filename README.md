<p align="center">
  <img src="assets/logo.svg" width="128" height="128" alt="Vayaan Labs logo">
</p>

<h1 align="center">Vayaan Labs plugins</h1>

<p align="center"><b>A Claude Code plugin marketplace: add it once, then install any Vayaan Labs plugin by name and keep it updated.</b></p>

<p align="center">
  <a href="#get-started">Add the catalogue</a> · <a href="#plugins">Plugins</a> · <a href="https://github.com/vayaan-labs/claude-plugins/issues">Report a bug</a>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Claude_Code-2.1.289+-d97757?style=flat-square" alt="Claude Code 2.1.289 or later">
  <a href="LICENSE"><img src="https://img.shields.io/github/license/vayaan-labs/claude-plugins?style=flat-square" alt="MIT licence"></a>
  <a href="https://github.com/vayaan-labs/claude-plugins/stargazers"><img src="https://img.shields.io/github/stars/vayaan-labs/claude-plugins?style=flat-square" alt="GitHub stars"></a>
</p>

A marketplace is a list Claude Code reads so you can install plugins by name instead of hunting down each repository. This one carries the Claude Code plugins Vayaan Labs makes.

## Plugins

| Plugin | What it does | Install |
| --- | --- | --- |
| [Cache Maxxer](https://github.com/vayaan-labs/cache-maxxer) | Shows your prompt cache's countdown and hit rate above the input box, explains every cache break, and can keep the cache warm so you stop paying to rebuild it. | `cache-maxxer@vayaan-labs` |

<p align="center">
  <img src="assets/band.png" alt="The Cache Maxxer band in a terminal: a green countdown at 59:47 beside a bar that drains, 1 hour cache, hit 95.33% last request and 68.19% this session, and the buttons Keep warm: off, Warm now and More.">
</p>
<p align="center"><i>Cache Maxxer in a terminal.</i></p>

## Get started

1. **Add the catalogue.** In the Claude desktop app, open the Directory, choose Plugins, press + and choose Add marketplace, then Add from a repository, and enter `vayaan-labs/claude-plugins`.

   ![The Add marketplace dialog in the Claude desktop app, with two choices: Browse Anthropic sources, and Add from a repository, which syncs a plugin marketplace from a GitHub repository or Git URL.](assets/add-marketplace.png)

   In a terminal:

   ```
   claude plugin marketplace add vayaan-labs/claude-plugins
   ```

2. **Install a plugin.** Find it in the Vayaan Labs catalogue and install it, or in a terminal use its name from the table:

   ```
   claude plugin install cache-maxxer@vayaan-labs
   ```

3. **Use it.** If Claude Code was already open, run `/reload-plugins` first. Each plugin's own page says what to expect.

Update with `claude plugin marketplace update vayaan-labs`, then `claude plugin update <plugin>@vayaan-labs`, and restart Claude Code. Remove a plugin with `claude plugin uninstall <plugin>@vayaan-labs`, or the whole catalogue with `claude plugin marketplace remove vayaan-labs`.

## Privacy

The catalogue is one file, `.claude-plugin/marketplace.json`, naming each plugin and the GitHub repository its code lives in. It has no server and runs nothing. Claude Code fetches it from GitHub when you add or update the catalogue, and fetches a plugin's repository when you install it. What a plugin does once installed is on its own page.

## Contributing

Found a problem with the catalogue? Open an issue. A problem with a plugin belongs in that plugin's own repository. Check a change to the catalogue with:

```
claude plugin validate --strict .claude-plugin/marketplace.json
```

To report a security problem privately, see [SECURITY.md](SECURITY.md).

## Licence

MIT. Built by [@YaanFPV](https://github.com/yaanfpv).
