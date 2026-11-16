# homebrew-tap

Homebrew packages for tools by [thesouldev](https://github.com/thesouldev).

## Install

```bash
brew install thesouldev/tap/<package>
```

Homebrew adds the tap on first use. To add it on its own:

```bash
brew tap thesouldev/tap
```

## Packages

| Package | Platforms | Description |
| --- | --- | --- |
| [google-tasks-mcp](https://github.com/thesouldev/google-tasks-mcp) | macOS | MCP server for Google Tasks |

## Update

```bash
brew update
brew upgrade thesouldev/tap/<package>
```

## Uninstall

```bash
brew uninstall <package>
brew untap thesouldev/tap    # only once nothing else from this tap is installed
```

## How packages get here

Nothing in `Casks/` or `Formula/` is written by hand. Each project's release
workflow runs [GoReleaser](https://goreleaser.com) when a version tag is pushed.
GoReleaser builds the binaries, publishes them to that project's GitHub
Releases, and commits the updated package file here. Homebrew then downloads
the binaries from those releases and checks them against the SHA-256 in the
package file.

A manual edit here is overwritten by the next release. Change the project's
`.goreleaser.yaml` instead.

To add a project, give its release workflow a fine-grained token with Contents
read and write on this repository only, and point its GoReleaser config at
`thesouldev/homebrew-tap`.
