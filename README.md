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

The `edge` channel installs the most recently published release, even if it
has not yet been promoted to latest. Useful for verifying a release before
promotion.

```yaml
steps:
  - name: Run a Porter CLI command
    uses: porter-dev/setup-porter@v0.1.0
    with:
      channel: edge
```

`tagged_release` takes precedence over `channel` when both are set.
