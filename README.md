# homebrew-gomod

A brew command to cleanly install binaries from Go modules.

https://blog.filippo.io/install-go-tools-from-modules-with-brew-gomod

## Installation

```
$ brew install cdzombak/gomod/brew-gomod
```

## Usage

```
$ brew gomod github.com/maruel/panicparse/cmd/pp
go: creating new go.mod: module gomod-pp/2020-03-15
go: downloading github.com/maruel/panicparse v1.3.0
go: found github.com/maruel/panicparse/cmd/pp in github.com/maruel/panicparse v1.3.0
go: downloading github.com/mattn/go-isatty v0.0.7
go: downloading github.com/mattn/go-colorable v0.1.1
go: downloading github.com/mgutz/ansi v0.0.0-20170206155736-9520e82c474b
go: downloading golang.org/x/sys v0.0.0-20190222072716-a9d3bda3a223
Linking /usr/local/Cellar/gomod-pp/2020-03-15...  1 symlinks created

$ brew uninstall gomod-pp
Uninstalling /usr/local/Cellar/gomod-pp/2020-03-15... (3 files, 4.8MB)
```

## Releases

When a new version is tagged (e.g., `v0.0.6`), the GitHub Actions workflow automatically:

1. Creates a GitHub release
2. Downloads the release tarball and calculates its SHA256 hash
3. Updates `brew-gomod.rb` with the new version URL and hash
4. Commits the updated formula back to the repository
5. Uploads the updated formula as a release asset

This ensures the Homebrew formula is always synchronized with the latest release.
