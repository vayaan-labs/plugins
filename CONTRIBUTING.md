# Contributing to the Vayaan Labs plugins catalogue

This catalogue lists the plugins Vayaan Labs makes. Each plugin lives in its own repository, linked from the table in the [README](README.md), and that is where its bugs, ideas and code changes go.

## Reporting a problem with the catalogue

Open an [issue](https://github.com/vayaan-labs/plugins/issues/new/choose) if adding the catalogue fails, a plugin listed here won't install, or the README is wrong. Include your Claude Code version (`claude --version`) and the exact command or steps you used, with the error you saw.

A security problem goes through [SECURITY.md](SECURITY.md) instead, never a public issue.

## Changing the catalogue

Fork the repository, branch from `main` and edit `.claude-plugin/marketplace.json`. Before you open a pull request, check it with:

```
claude plugin validate --strict .claude-plugin/marketplace.json
```

Open the pull request against `main` and say what changed and why. Pull requests are squash-merged, so the title becomes the commit message.

## Code of conduct

Everyone taking part follows the [code of conduct](CODE_OF_CONDUCT.md).
