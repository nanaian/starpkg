# Contributing

:tada: Thank you for contributing to starpkg!! :tada:

## Commits

Use [Conventional Commit messages](https://www.conventionalcommits.org/en/v1.0.0-beta.4/).

If your commit makes a breaking change, consider whether it would be feasible to make it minor
instead (i.e. make it backwards-compatible)! Otherwise, merging it will have to be delayed until the
next major release of starpkg.

For commit scopes, prefer using the name of a starpkg subcommand, eg. `new`, if relevant.

Changelogs are generated with [git-chglog](https://github.com/git-chglog/git-chglog) upon release.
Only some commit types (`feat`, `fix`, `pref`, `improvement`) will be shown in release changelogs.

## Linting

Source files are linted with [clippy](https://crates.io/crates/clippy). Linting errors will fail a
build, so it is suggested that you run clippy locally:

```sh
$ rustup component add clippy
$ cargo clippy
```

## Documentation

To view the user guide locally, use [mdBook](https://github.com/rust-lang/mdBook):

```sh
$ cargo install mdbook
$ cargo mdbook serve
```

## Releases

- Bump [Cargo.toml](Cargo.toml) version according to [semver](https://semver.org/spec/v2.0.0.html)
- `git add -A && git commit -m "chore(release): [VERSION]"`
- `git tag v[VERSION]`
- `git push && git push --tags`

The install script gist can be found [here][install-gist].

[install-gist]: https://gist.github.com/nanaian/cf9ca4e645d8b7b1951c42d2b9c6f2f6