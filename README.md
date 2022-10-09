# git-restore-mtime-action
GitHub Action for running [git-restore-mtime](https://github.com/MestreLion/git-tools)

## Example

```yaml
on: [push]

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v3
        with:
          fetch-depth: 0 # fetch commit log

      - uses: ciffelia/git-restore-mtime-action@v1

      - run: ./build.sh
```
