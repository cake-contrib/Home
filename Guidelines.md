# Cake-Contrib Guidelines & Best Practices

This document provides some guidelines and best practices for writing Cake addins hosted within the cake-contrib GitHub Organization.

All known addins are audited twice daily to ensure compliance, and a summary report, as well as a detailed report, are generated at the conclusion of each audit.
Results of this auditing are integrated into the Cake website (e.g. version of Cake with which an addin is compatible).
As an addin author you should use the [detailed audit report](Audit.xlsx) to verify that you are complying with all recommendations.

## General Best Practices

Addins should follow general [Best Practices for writing Cake addins] as documented on the Cake website.

## Build Infrastructure

Addins which are part of the cake-contrib Organization should use the [Cake.Recipe] scripts for their build process.

## Addin documentation

The preferred tool for creating documentation for the addin is [Wyam].
The [Cake.Recipe] scripts support building [Wyam] projects and the created website can be published to
`https://cake-contrib.github.io/Cake.AddinName/` using a `gh-pages` branch.

For details see [How to create gh-pages branch].

## Deprecating an addin

From time to time, a previously published addin  needs to be deprecated. This could be for a number of reasons:

- It was created in error.
- It has been superseded by another package.
- It is an older package that no longer follows the guidelines.
- Its package id has been changed to something that better fits with the package naming guidelines.

All versions of this package could simply be unlisted from nuget.org, meaning that they could no longer be found, however, this solution is not ideal. Any build script referencing this package without a specific version would no longer works which is far from ideal. When a package needs to be deprecated, it needs to be handled in such a way that existing users will continue to be able to use the old package id, but take advantage of the replacement package, if there is one.

In order to deprecate an addin, the following steps should be followed:

- Create a new version of the deprecated addin package.
- Prepend `[DEPRECATED]` to the title of the package (e.g. "[DEPRECATED] My Cake addin")
- Update the package description: Why is the package being deprecated?
- Publish this new version of the package to nuget.org

## Further reading

- [Best Practices for writing Cake addins]
- [Cake Documentation Guidelines]
- [Cake.Recipe]
- [Wyam]
- [How to create gh-pages branch]

[Best Practices for writing Cake addins]: https://cakebuild.net/docs/extending/addins/best-practices
[Cake Documentation Guidelines]: https://cakebuild.net/community/contributing/documentation
[Cake.Recipe]: https://cake-contrib.github.io/Cake.Recipe/
[Wyam]: https://wyam.io/
[How to create gh-pages branch]: https://www.gep13.co.uk/blog/how-to-create-gh-pages-branch
