# Solar2D Plugin Updater

This is simple GitHub Composite Action to perform updating of the plugin.

It publishes a new release and requests and update from the [Plugin Directory](https://plugins.solar2d.com).

```yaml
on:
  push:
    paths:
      - 'plugins/**'
      - 'docs/**'
  repository_dispatch:

jobs:
  publish-release:
    runs-on: ubuntu-latest
    steps:
      - uses: solar2d/directory-plugin-action@main
        with:
          pat: ${{ secrets.ISSUE_PAT }}
      
```
