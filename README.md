# PullWeights APT Repository

APT package repository for the [PullWeights CLI](https://github.com/pullweights/cli) — served via GitHub Pages at `apt.pullweights.com`.

## Install

```bash
curl -fsSL https://apt.pullweights.com/gpg | sudo gpg --dearmor -o /usr/share/keyrings/pullweights.gpg
echo "deb [signed-by=/usr/share/keyrings/pullweights.gpg] https://apt.pullweights.com stable main" | sudo tee /etc/apt/sources.list.d/pullweights.list
sudo apt update
sudo apt install pullweights
```

## Update

```bash
sudo apt update && sudo apt upgrade pullweights
```

## Architectures

- `amd64` (x86_64)
- `arm64` (aarch64)

## How it works

The [`pullweights/cli`](https://github.com/pullweights/cli) release workflow builds `.deb` packages with `cargo-deb`, assembles the APT repository with `reprepro`, and deploys to the `gh-pages` branch of this repo. Packages are signed with the PullWeights GPG key.

Only the latest version is published here. Previous versions are available on the [GitHub Releases](https://github.com/pullweights/cli/releases) page.

## Links

- [CLI source](https://github.com/pullweights/cli)
- [Documentation](https://pullweights.com/docs/cli)
- [Quickstart](https://pullweights.com/docs/quickstart)
