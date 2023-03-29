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

```sh
cd project
gh prq
```

If you have a `.github/pull_request_template.md` file in your project, it will
be filled in your editor.

Pass `--copy` to copy the Pull Request URL to your clipboard.

Pass `--open` to open the Pull Request in your web browser.

Pass `--push` to push your branch upstream first.

Configure a `git prq` alias:

```sh
git config --global --add alias.prq '!gh prq --copy --open --push'
```

## Editor Examples

By default, `gh prq` will use the same editor that `git commit` would. Git
determines that by checking for the first of:

- `$GIT_EDITOR`
- `git config core.editor`
- `$EDITOR`

If you want to configure one, set one of the following in your `~/.bashrc` or
`~/.zshrc` file:

Vim:

```sh
export GIT_EDITOR="vim"
```

MacVim:

```sh
export GIT_EDITOR="mvim"
```

Emacs:

```sh
export GIT_EDITOR="emacs"
```

VSCode:

```sh
export GIT_EDITOR="code --wait"
```

Sublime Text:

```sh
export GIT_EDITOR="subl --wait"
```

If you prefer to use `~/.gitconfig`, you can use something like:

```sh
git config --global --add core.editor "vim"
git config --global --add core.editor "code --wait"
```

## Bug Reports

Issues can be reported on GitHub:

<https://github.com/itspriddle/gh-prq/issues>

## License

MIT License - see [`LICENSE`](./LICENSE) in this repository.
