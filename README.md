# kiwi-trolley

A [Claude Code](https://docs.claude.com/en/docs/claude-code) [plugin](https://code.claude.com/docs/en/plugins)
of New Zealand grocery tooling.

The plugin bundles [skills](https://docs.claude.com/en/docs/claude-code/skills) under `skills/`.
Right now there is one.

## Skills

- **[comparison](skills/comparison/)**: comparison-shop a grocery basket across New
  Zealand's main supermarket sites (Woolworths, New World, PAK'nSAVE and Four Square),
  reconcile the real cart prices, and build an interactive HTML price-comparison report
  plus an over-time trend report. Invoked as `kiwi-trolley:comparison`.

## Installing

Add this repo as a plugin marketplace, then install the plugin:

```
/plugin marketplace add etoews/kiwi-trolley
/plugin install kiwi-trolley@kiwi-trolley
```

## Developing

To work on the plugin against a live checkout, point a marketplace at this directory
and install from it:

```
/plugin marketplace add /path/to/kiwi-trolley
/plugin install kiwi-trolley@kiwi-trolley
```

The plugin manifest is `.claude-plugin/plugin.json`. Each skill is a self-contained
`skills/<name>/` directory: a `SKILL.md` plus any `references/`, `scripts/`, `assets/`
and `evals/` it needs.

## License

[MIT](LICENSE)
