# gh-prq

Open GitHub Pull Requests with your `$EDITOR` (like `hub pull-request`).

## Installation

First, install `gh` from <https://github.com/cli/cli/releases/latest> (`brew
install gh` on a Mac using Homebrew).

Install gh-prq via `gh extension install`:

```sh
gh extension install itspriddle/gh-prq
```

## Usage

When you're ready to submit a new Pull Request:

```
cd project
gh prq
```

Pass `--copy` to copy the Pull Request URL to your clipboard.

Pass `--open` to open the Pull Request in your web browser.

Pass `--push` to push your branch upstream first.

Configure a `git prq` alias:

```
git config --global --add alias.prq '!gh prq --copy --open --push'
```

## Bug Reports

Issues can be reported on GitHub:

<https://github.com/itspriddle/gh-prq/issues>

## License

MIT License - see [`LICENSE`](./LICENSE) in this repository.
