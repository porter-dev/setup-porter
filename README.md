# setup-porter

This Github action installs the Porter CLI on the Github Actions Runner.

## Usage

```yaml
steps:
  - name: Run a Porter CLI command
    uses: porter-dev/setup-porter@v0.1.0
```

By default the latest release is installed.

### Installing a specific version

```yaml
steps:
  - name: Run a Porter CLI command
    uses: porter-dev/setup-porter@v0.1.0
    with:
      tagged_release: v0.68.13
```
