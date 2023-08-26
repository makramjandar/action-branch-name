# action-github-branch-name
[![Test](https://github.com/microsoft/action-python/workflows/Test/badge.svg)](https://github.com/microsoft/action-python/actions?query=workflow%3ATest)
[![reviewdog](https://github.com/microsoft/action-python/workflows/reviewdog/badge.svg)](https://github.com/microsoft/action-python/actions?query=workflow%3Areviewdog)
[![depup](https://github.com/microsoft/action-python/workflows/depup/badge.svg)](https://github.com/microsoft/action-python/actions?query=workflow%3Adepup)
[![release](https://github.com/microsoft/action-python/workflows/release/badge.svg)](https://github.com/microsoft/action-python/actions?query=workflow%3Arelease)
[![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/microsoft/action-python?logo=github&sort=semver)](https://github.com/microsoft/action-python/releases)
[![action-bumpr supported](https://img.shields.io/badge/bumpr-supported-ff69b4?logo=github&link=https://github.com/haya14busa/action-bumpr)](https://github.com/haya14busa/action-bumpr)

This repo contains a action to run ...:
- [...](...)
- [...](...)

## Input

```yaml
inputs:
  black:
    description: |
```

## Usage

```yaml
name: Pull Request
on:
  push:
    branches: [ main ]
  pull_request:
    branches: [ main ]
  workflow_dispatch:

jobs:
```

## Development

### Release

#### [haya14busa/action-bumpr](https://github.com/haya14busa/action-bumpr)
You can bump version on merging Pull Requests with specific labels (bump:major,bump:minor,bump:patch).
Pushing tag manually by yourself also work.

#### [haya14busa/action-update-semver](https://github.com/haya14busa/action-update-semver)

This action updates major/minor release tags on a tag push. e.g. Update v1 and v1.2 tag when released v1.2.3.
ref: https://help.github.com/en/articles/about-actions#versioning-your-action
