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
Private variables are noted, which means they will no be available in pull requests.
However, these private variables can be made available in pull requests
originating from the same repository.

- `APPVEYOR_API_TOKEN` (_secret variable_)
- `AZURE_PASSWORD`
- `AZURE_SOURCE`
- `AZURE_USER`
- `GITHUB_PASSWORD` (_secret variable, can be used as a GitHub Token_)
- `GITHUB_USERNAME`
- `GITTER_ROOM_ID` (_secret variable_)
- `GITTER_TOKEN` (_secret variable_)
- `GPR_PASSWORD`
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

If you do not need to specify any additional configuration, and wishes to just
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

<!-- The following migrate docs need to be
  updated when migration documentation are
  complete -->

[cake-recipe-migrate]: https://github.com/cake-contrib/Cake.Recipe/issues/612
[cake-recipe-started]: https://cake-contrib.github.io/Cake.Recipe/docs/usage/getting-started-with-cake-recipe
