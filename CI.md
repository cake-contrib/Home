# Setting up Cake Contrib Addins on CI providers

<!-- markdownlint-disable -->
<!-- TOC depthfrom:2 depthto:6 -->

- [What is this](#what-is-this)
- [Using AppVeyor](#using-appveyor)
  - [Available Environment Variables](#available-environment-variables)
  - [Using Cake.Recipe 2.x with AppVeyor](#using-cakerecipe-2x-with-appveyor)
  - [Using Cake.Recipe 1.x with AppVeyor](#using-cakerecipe-1x-with-appveyor)
    - [Additional notes](#additional-notes)
- [Using Azure Pipelines](#using-azure-pipelines)
- [Using GitHub Actions](#using-github-actions)
  - [Available Organization Secrets](#available-organization-secrets)
  - [Using Cake.Recipe 2.x with GitHub Actions](#using-cakerecipe-2x-with-github-actions)
  - [Additional workflows](#additional-workflows)
    - [Forcing documentation publishing](#forcing-documentation-publishing)
    - [Drafting new releases](#drafting-new-releases)
      - [Drafting new stable release](#drafting-new-stable-release)
      - [Drafting new pre-release](#drafting-new-pre-release)

<!-- /TOC -->
<!-- markdownlint-enable -->

## What is this

The goal of this document is to help setting up new builds for different build
providers under the cake-contrib organization.
Some CI providers may already have Environment Variables or secrets set on the
organization level that are available during the build.

## Using AppVeyor

### Available Environment Variables

The following environment variables are accessible when running builds on the
AppVeyor CI provider and will be available without further configuration.
Private variables are noted, which means they will not be available in pull requests.
However, these private variables can be made available in pull requests
originating from the same repository.

- `APPVEYOR_API_TOKEN` (_secret variable_)
- `AZURE_PASSWORD` (_secret variable_)
- `AZURE_SOURCE`
- `AZURE_USER`
- `GITHUB_PASSWORD` (_secret variable, can be used as a GitHub Token_)
- `GITHUB_USERNAME`
- `GITTER_ROOM_ID` (_secret variable_)
- `GITTER_TOKEN` (_secret variable_)
- `GPR_PASSWORD` (_secret variable_)
- `GPR_SOURCE`
- `GPR_USER`
- `MYGET_API_KEY` (_secret variable_)
- `MYGET_SOURCE`
- `NUGET_API_KEY` (_secret variable_)
- `NUGET_SOURCE`
- `TWITTER_ACCESS_TOKEN_SECRET` (_secret variable_)
- `TWITTER_ACCESS_TOKEN` (_secret variable_)
- `TWITTER_CONSUMER_KEY` (_secret variable_)
- `TWITTER_CONSUMER_SECRET` (_secret variable_)
- `WYAM_ACCESS_TOKEN` (_secret variable_)
- `WYAM_DEPLOY_BRANCH`

### Using Cake.Recipe 2.x with AppVeyor

While the latest version of Cake.Recipe is currently in pre-release stage,
it is entirely usable on AppVeyor.
We already assume you have configured the repository to use Cake.Recipe,
otherwise please see its [Getting Started][cake-recipe-started] on how to proceed.

_Please see the [Cake.Recipe documentatian][cake-recipe-migrate] on how to upgrade
from Cake.Recipe 1.x te 2.x._

If you do not need to specify any additional configuration, and wish to just
have it work with default options.
Then the most basic build script can be specified as follows:

```yml
# This image may be changed when needed,
# but the recommendation is to keep it on
# Visual Studio 2019.
image: Visual Studio 2019

#---------------------------------#
#  Build Script                   #
#---------------------------------#
build_script:
  - ps: .\build.ps1 -Target CI

# Tests
test: off

#---------------------------------#
#        Branches to build        #
#---------------------------------#
branches:
  # Whitelist
  only:
    - develop
    - master
    - /release/.*/
    - /hotfix/.*/

#---------------------------------#
#  Build Cache                    #
#---------------------------------#
cache:
  # Update this cache variable to match
  # your current setup.
  - "tools -> recipe.cake,tools/packages.config"

#---------------------------------#
#  Environment Variables          #
#---------------------------------#

environment:
  # We set MYGET_SOURCE to an empty variable due to known issues when pushing
  # packages to MyGet
  MYGET_SOURCE:
```

**WARNING: At this time it is not recommended to add a matrix to build on
multiple platforms on AppVeyor due to the increased build time necessary.**

### Using Cake.Recipe 1.x with AppVeyor

Configuring AppVeyor to build projects targeting Cake.Recipe 1.x is very similar
to how to use Cake.Recipe 2.x documentation.
The main change between the build script on AppVeyor is mainly to change the
build target from `CI` to `AppVeyor`.
See the below build script as an example of this.

```yml
image: Visual Studio 2017
#---------------------------------#
#  Build Script                   #
#---------------------------------#
build_script:
  - ps: .\build.ps1 -Target AppVeyor

# Tests
test: off

#---------------------------------#
#        Branches to build        #
#---------------------------------#
branches:
  # Whitelist
  only:
    - develop
    - master
    - /release/.*/
    - /hotfix/.*/

#---------------------------------#
#  Build Cache                    #
#---------------------------------#
cache:
  # Update this cache variable to match
  # your current setup.
  - "tools -> recipe.cake,tools/packages.config"

#---------------------------------#
#  Environment Variables          #
#---------------------------------#

environment:
  # We set MYGET_SOURCE to an empty variable due to known issues when pushing
  # packages to MyGet
  MYGET_SOURCE:
```

**WARNING: At this time it is not recommended to add a matrix to build on
multiple platforms on AppVeyor due to the increased build time necessary.**

#### Additional notes

If you do not plan to use AppVeyor as the preferred build platform,
it may not be possible to use Cake.Recipe 1.x. Please migrate to the latest 2.x
pre-release instead.

## Using Azure Pipelines

There is currently no documentation on how to set up Cake Contrib addins for
building on Azure Pipelines.

## Using GitHub Actions

### Available Organization Secrets

The following secrets are provided on the organization level and can be made
available in GitHub workflows.
See the examples of how these can be made available for usage.
Unless configured per repository, these secrets are not available when running
workflows toward pull requests (_we do not recommend changing settings to allow this_).
Maintainers may also go to `Settings --> Secrets` to see the available secrets
set (you will not be able to see the values).

- `APPVEYOR_API_TOKEN` (_Should not be needed on GitHub Actions in general_)
- `AZURE_PASSWORD`
- `AZURE_SOURCE`
- `AZURE_USER`
- `GH_TOKEN` (In most cases, this token should be used instead of `GITHUB_TOKEN`
  as using the latter will prevent any workflows from triggering.)
- `GITTER_ROOM_ID`
- `GITTER_TOKEN`
- `GPR_PASSWORD`
- `GPR_SOURCE`
- `GPR_USER`
- `MYGET_API_KEY`
- `MYGET_SOURCE`
- `NUGET_API_KEY`
- `NUGET_SOURCE`
- `TWITTER_ACCESS_TOKEN`
- `TWITTER_ACCESS_TOKEN_SECRET`
- `TWITTER_CONSUMER_KEY`
- `TWITTER_CONSUMER_SECRET`
- `WYAM_ACCESS_TOKEN`
  (_`GITHUB_TOKEN` can also be used, but we recommend to use this token instead_)
- `WYAM_DEPLOY_BRANCH` (_provided for convenience_)

### Using Cake.Recipe 2.x with GitHub Actions

For using GitHub Actions as the preferred build provider, it is necessary to use
Cake.Recipe 2.x.
Using Cake 1.x will require overriding criteria on publishing tasks,
and it completely unsupported.

You can use the following minimal workflow file if you want to use Cake.Recipe
together with GitHub Actions.

```yml
name: Build

on:
  push:
    branch:
      - master
      - develop
      - "release/**"
      - "hotfix/**"
      # Add any additional branches you wish to run the workflow on
    pull_request:

jobs:
  build:
    runs-on: ${{ matrix.os }}
    strategy:
      os: [windows-latest, ubuntu-latest, macos-latest]
    env:
      AZURE_PASSWORD: ${{ secrets.AZURE_PASSWORD }}
      AZURE_SOURCE: ${{ secrets.AZURE_SOURCE }}
      AZURE_USER: ${{ secrets.AZURE_USER }}
      GITHUB_TOKEN: ${{ secrets.GH_TOKEN }}
      GITTER_ROOM_ID: ${{ secrets.GITTER_ROOM_ID }}
      GITTER_TOKEN: ${{ secrets.GITTER_TOKEN }}
      GPR_PASSWORD: ${{ secrets.GPR_PASSWORD }}
      GPR_SOURCE: ${{ secrets.GPR_SOURCE }}
      GPR_USER: ${{ secrets.GPR_USER }}
      # The MyGet related environment variables are currently not recommended
      # to be used. But kept here for completeness.
      MYGET_API_KEY: ${{ secrets.MYGET_API_KEY }}
      MYGET_SOURCE: ${{ secrets.MYGET_SOURCE }}
      NUGET_API_KEY: ${{ secrets.NUGET_API_KEY }}
      NUGET_SOURCE: ${{ secrets.NUGET_SOURCE }}
      TWITTER_ACCESS_TOKEN: ${{ secrets.TWITTER_ACCESS_TOKEN }}
      TWITTER_ACCESS_TOKEN_SECRET: ${{ secrets.TWITTER_ACCESS_TOKEN_SECRET }}
      TWITTER_CONSUMER_KEY: ${{ secrets.TWITTER_CONSUMER_KEY }}
      TWITTER_CONSUMER_SECRET: ${{ secrets.TWITTER_CONSUMER_SECRET }}
      WYAM_ACCESS_TOKEN: ${{ secrets.WYAM_ACCESS_TOKEN }}
      WYAM_DEPLOY_BRANCH: "gh-pages"
      WYAM_DEPLOY_REMOTE: ${{ github.event.repository.html_url }}

    steps:
      - uses: actions/checkout@v2
      - name: Fetch all tags and branches
        run: git fetch --prune --unshallow
      - name: Cache Tools
        uses: actions/cache@v2
        with:
          path: tools
          # Make any necessary changes to this key if you use a different
          # cake build script name.
          key: ${{ runner.os }}-tools-${{ hashFiles('recipe.cake') }}
      # If you are running unit tests against only .NET Core 3.1,
      # then you do not need this step
      - name: Set up .NET Core 2.1
        uses: actions/setup-dotnet@v1.5.0
        with:
          dotnet-version: 2.1.809
      - name: Build Addin
        uses: cake-build/cake-action@v1
        with:
          # Change the script path to your actual cake script file
          script-path: recipe.cake
          target: CI
          cake-version: 0.38.4
          cake-bootstrap: true
      # The following is untested, and needs verification
      - name: Upload artifacts
        uses: actions/upload-artifacts@v2
        with:
          name: ${{ runner.os }}-artifacts
          path: |
            BuildArtifacts/issues-report.html
            Buildartifacts/packages/**/*.nupkg
            BuildArtifacts/**/coverlet/*.xml
```

### Additional workflows

The following workflow files are made available to make particular release
related tasks more comfortable to achieve.
Use of these files should be in addition to the standard build workflow file.

#### Forcing documentation publishing

When there is a need to force publishing a new set of documentation, then the
following workflow may be used to allow this.
The workflow will run from the branch that is configured as the base branch when
triggering the run.

```yml
name: Publish Documentation

on:
  workflow_dispatch:

jobs:
  publish-docs:
    env:
      WYAM_ACCESS_TOKEN: ${{ secrets.WYAM_ACCESS_TOKEN }}
      WYAM_DEPLOY_REMOTE: "${{ github.event.repository.html_url }}"
      WYAM_DEPLOY_BRANCH: "gh-pages"
    # ubuntu-latest is used here due to it being
    # the one taking the shortest time to execute
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
        with:
          ref: ${{ github.event.ref }}
      - name: Cache Tools
        uses: actions/cache@v2
        with:
          path: tools
          key: ${{ runner.os }}-doc-tools-${{ hashFiles('recipe.cake') }}
      - name: Publishing documentaiton
        uses: cake-build/cake-action@v1
        with:
          script-path: recipe.cake
          target: Force-Publish-Documentation
          cake-version: 0.38.4
          cake-bootstrap: true
```

#### Drafting new releases

When it comes the time to release a new stable release of the addin, then you
may use the following workflow file instead of needing to run the necessary
steps locally.
These workflows will create a new branch (when one do not exist) called `release/asserted-version`.
(where asserted-version is the version as detected by GitVersion)

##### Drafting new stable release

```yml
name: Draft Release Notes

on:
  workflow_dispatch:

jobs:
  draft:
    env:
      # Do not use the normal GITHUB_TOKEN here.
      # It will prevent builds running on tags to be initiated.
      GITHUB_TOKEN: ${{ secrets.GH_TOKEN }}
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
        with:
          ref: ${{ github.event.ref }}
      - name: Fetch all tags and branches
        run: git fetch --prune --unshallow
      - name: Cache Tools
        uses: actions/cache@v2
        with:
          path: tools
          key: ${{ runner.os }}-draft-tools-${{ hashFiles('build.cake') }}
      - name: Set up git version
        if: ${{ !contains(github.ref, '/hotfix/') && !contains(github.ref, '/release/') }}
        uses: gittools/actions/gitversion/setup@v0.9.4
        with:
          versionSpec: "5.x"
      - name: Run git version
        if: ${{ !contains(github.ref, '/hotfix/') && !contains(github.ref, '/release/') }}
        id: gitversion
        uses: gittools/actions/gitversion/execute@v0.9.4
      - name: Create release branch ${{ github.event.inputs.version }}
        if: ${{ steps.gitversion.outputs.majorMinorPatch }}
        run: git switch -c release/${{ steps.gitversion.outputs.majorMinorPatch }}
      - name: Push new branch
        if: ${{ steps.gitversion.outputs.majorMinorPatch }}
        uses: ad-m/github-push-action@v0.6.0
        with:
          branch: "release/${{ steps.gitversion.outputs.majorMinorPatch }}"
          github_token: ${{ secrets.GH_TOKEN }}
      - name: Drafting Release Notes
        uses: cake-build/cake-action@v1
        with:
          script-path: recipe.cake
          target: releasenotes
          cake-version: 0.38.4
          cake-bootstrap: true
```

##### Drafting new pre-release

```yml
name: Draft Pre Release Notes

on:
  workflow_dispatch:

jobs:
  draft-pre-release:
    env:
      # Do not use the normal GITHUB_TOKEN here.
      # It will prevent builds running on tags to be initiated.
      GITHUB_TOKEN: ${{ secrets.GH_TOKEN }}
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v2
        with:
          ref: ${{ github.event.ref }}
      - name: Fetch all tags and branches
        run: git fetch --prune --unshallow
      - name: Cache Tools
        uses: actions/cache@v2
        with:
          path: tools
          key: ${{ runner.os }}-draft-tools-${{ hashFiles('build.cake') }}
      - name: Set up git version
        if: ${{ !contains(github.ref, '/hotfix/') && !contains(github.ref, '/release/') }}
        uses: gittools/actions/gitversion/setup@v0.9.4
        with:
          versionSpec: "5.x"
      - name: Run git version
        if: ${{ !contains(github.ref, '/hotfix/') && !contains(github.ref, '/release/') }}
        id: gitversion
        uses: gittools/actions/gitversion/execute@v0.9.4
      - name: Create release branch ${{ github.event.inputs.version }}
        if: ${{ steps.gitversion.outputs.majorMinorPatch }}
        run: git switch -c release/${{ steps.gitversion.outputs.majorMinorPatch }}
      - name: Push new branch
        if: ${{ steps.gitversion.outputs.majorMinorPatch }}
        uses: ad-m/github-push-action@v0.6.0
        with:
          branch: "release/${{ steps.gitversion.outputs.majorMinorPatch }}"
          github_token: ${{ secrets.GITHUB_TOKEN }}
      - name: Create release notes
        # Cake action do not support passing additional arguments.
        # As such we need to run the bootstrapper manually
        run: ./build.sh --target=releasenotes --create-pre-release
```

<!-- The following migrate docs need to be
  updated when migration documentation are
  complete -->

[cake-recipe-migrate]: https://github.com/cake-contrib/Cake.Recipe/issues/612
[cake-recipe-started]: https://cake-contrib.github.io/Cake.Recipe/docs/usage/getting-started-with-cake-recipe
