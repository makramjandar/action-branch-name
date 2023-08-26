# action-branch-name
[![Test](https://github.com/makramjandar/action-branch-name/workflows/Test/badge.svg)](https://github.com/makramjandar/action-branch-name/actions?query=workflow%3ATest)
[![reviewdog](https://github.com/makramjandar/action-branch-name/workflows/reviewdog/badge.svg)](https://github.com/makramjandar/action-branch-name/actions?query=workflow%3Areviewdog)
[![depup](https://github.com/makramjandar/action-branch-name/workflows/depup/badge.svg)](https://github.com/makramjandar/action-branch-name/actions?query=workflow%3Adepup)
[![release](https://github.com/makramjandar/action-branch-name/workflows/release/badge.svg)](https://github.com/makramjandar/action-branch-name/actions?query=workflow%3Arelease)
[![GitHub release (latest SemVer)](https://img.shields.io/github/v/release/makramjandar/action-branch-name?logo=github&sort=semver)](https://github.com/makramjandar/action-branch-name/releases)
[![action-bumpr supported](https://img.shields.io/badge/bumpr-supported-ff69b4?logo=github&link=https://github.com/haya14busa/action-bumpr)](https://github.com/haya14busa/action-bumpr)

This repo contains a action to get repo's branch name:  
based on [How to get the current branch within Github Actions?https://stackoverflow.com/questions/58033366/how-to-get-the-current-branch-within-github-actions]:()

## Output

```yaml
outputs:
  branch-name:
    description: "Branch name"
    value: ${{ steps.branch-name-extractor.outputs.branch-name }}
```

## Usage

```yaml
name: GitHub Composite Action to extract the Branch Name
on:
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest

    defaults:
      run:
        shell: bash
    
    steps:
      - uses: actions/checkout@v3
      - id: get-branch-name
        uses: makramjandar/action-branch-name@v1
      - run: echo ${{ steps.get-branch-name.outputs.branch-name }}
```



## Development

### Release

#### [haya14busa/action-bumpr](https://github.com/haya14busa/action-bumpr)
You can bump version on merging Pull Requests with specific labels (bump:major,bump:minor,bump:patch).
Pushing tag manually by yourself also work.

#### [haya14busa/action-update-semver](https://github.com/haya14busa/action-update-semver)

This action updates major/minor release tags on a tag push. e.g. Update v1 and v1.2 tag when released v1.2.3.
ref: https://help.github.com/en/articles/about-actions#versioning-your-action
