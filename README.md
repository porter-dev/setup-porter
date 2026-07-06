# setup-porter

This Github action installs the Porter CLI on the Github Actions Runner.

## Usage

```yaml
steps:
  - name: Run a Porter CLI command
    uses: porter-dev/setup-porter@v0.1.0
```

By default the latest promoted (stable) release is installed.

### Installing a specific version

```yaml
steps:
  - name: Run a Porter CLI command
    uses: porter-dev/setup-porter@v0.1.0
    with:
      tagged_release: v0.68.13
```

### Installing the newest release, promoted or not

Setting `allow_unstable: true` installs the most recently published release,
even if it has not yet been promoted to latest. Useful for verifying a
release before promotion. If the newest release cannot be resolved, the
action falls back to the latest promoted release.

```yaml
steps:
  - name: Run a Porter CLI command
    uses: porter-dev/setup-porter@v0.1.0
    with:
      allow_unstable: true
```

`tagged_release` takes precedence over `allow_unstable` when both are set.
