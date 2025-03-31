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

Behind the scenes, `gh prq` uses `gh pr create --editor -H BRANCH
--fill-first`. This opens your `$EDITOR` using the contents of the current
branch's first commit message as the Pull Request title. If there's a
`.github/pull_request_template.md` file at the root of the repository, its
contents will be added as the `--body` argument, ready to edit in your
`$EDITOR`.

Pass `--copy` to copy the Pull Request URL to your clipboard.

Pass `--open` to open the Pull Request in your web browser.

Pass `--push` to push your branch upstream first.

Configure a `git prq` alias:

```sh
git config --global --add alias.prq '!gh prq --copy --open --push'
```

## Editor Examples

By default, `gh prq` will use the same editor that `gh pr create --editor`
would use. `gh`  determines that by checking for one of:

- `gh config editor`
- `$GIT_EDITOR`
- `git config core.editor`
- `$EDITOR`

If you want to configure one, `gh config set editor <editor>` is your best
bet. Run one of the following:

Vim:

```sh
gh config set editor vim
```

MacVim:

```sh
gh config set editor mvim
```

Emacs:

```sh
gh config set editor emacs
```

VSCode:

```sh
gh config set editor "code --wait"
```

Sublime Text:

```sh
gh config set editor "subl --wait"
```

## Bug Reports

Issues can be reported on GitHub:

<https://github.com/itspriddle/gh-prq/issues>

## License

MIT License - see [`LICENSE`](./LICENSE) in this repository.
