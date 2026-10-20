<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/kkeeland/perseids/main/assets/logo-dark.svg">
    <img alt="perseids" src="https://raw.githubusercontent.com/kkeeland/perseids/main/assets/logo-light.svg" width="260">
  </picture>
</p>

<p align="center"><b>gh perseids</b>: run every job in your GitHub Actions workflow at once, on fresh cloud machines.<br>
A <code>gh</code> extension for <a href="https://github.com/kkeeland/perseids">Perseids</a>.</p>

## Install

```bash
gh extension install kkeeland/gh-perseids
gh perseids key      # your Boat API key, asked once
```

## Use

```bash
gh perseids run              # every job in .github/workflows/ci.yml
gh perseids run unit e2e     # only these jobs
gh perseids exec 'npm test'  # one command on one machine
```

Every Perseids command works after `gh perseids`. The first run installs Perseids into `~/.perseids` (set
`PERSEIDS_HOME` to move it), and it updates itself at most once a day. It needs `git`, `curl`, `ssh`, `jq` and Ruby 2.6+,
and tells you how to install anything missing.

Docs, exit codes and settings: [kkeeland/perseids](https://github.com/kkeeland/perseids).

## License

[MIT](LICENSE) © 2026 Kevin Keeland
