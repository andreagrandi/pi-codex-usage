# @andreagrandi/pi-codex-usage

Pi extension that shows ChatGPT Codex subscription usage from inside Pi.

This fork keeps the `/codex-status` command and adds statusline-chip emission for `@andreagrandi/pi-statusline`, so Codex usage appears as:

```text
📊 57% (5h) / 50% (7d)
```

## Install

From GitHub:

```bash
pi install git:github.com/andreagrandi/pi-codex-usage
```

Reload Pi:

```text
/reload
/codex-status --refresh
```

## Commands

```text
/codex-status
/codex-status --refresh
/codex-status --no-statusline
/codex-status --clear-statusline
/codex-status --timeout 30
```

## Auth behavior

The extension tries usage sources in this order:

1. Pi's `openai-codex` provider auth.
2. Codex CLI app-server fallback when Pi auth cannot provide usable subscription auth.

OpenAI API keys are not ChatGPT Codex subscription auth and do not expose these quotas.

## Credits

This package is a fork/refactor of [`@narumitw/pi-codex-usage`](https://www.npmjs.com/package/@narumitw/pi-codex-usage).

Thank you to the original author and maintainers. This fork keeps the MIT license.
