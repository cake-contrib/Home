# Cake-Contrib Guidelines & Best Practices

This document provides some guidelines and best practices for writing Cake addins hosted within the cake-contrib GitHub organisation.

## Build Infrastructure

Addins which are part of the cake-contrib organisation should use the [Cake.Recipe] scripts for their build process.

## Supported Cake Version

To have the best support for different versions of Cake, the addin should currently be build against Cake version 16.2,
or, if a specific newer functionality is required, the lowest version providing the specific functionality.

If the addin is built against newer versions it might not be compatible with previous versions of Cake.

## Assembly References

Assemblies required by the addin should be merged with or embedded in the Cake addin.
Otherwise there might be conflicts which cannot be resolved between different versions required by different addins.

There are different solutions explained below.

### Fody Costura

[Costura] is an addin for [Fody] which embeds dependencies as resources during build.
It's very easy to setup, in most cases just adding the [Costura.Fody NuGet package].
Loading assemblies from embedded resources comes with a small performance loss, but which shouldn't be an issue in most cases for Cake addins.

This is therefore the prefered method.

### ILMerge

[ILMerge] is a utility for merging multiple .NET assemblies into a single .NET assembly.
It is more difficult to setup than Costura, would require additional build steps currently not supported by [Cake.Recipe],
but would provide better performance than Costura.

[Cake.Recipe]: https://github.com/cake-contrib/Cake.Recipe
[Costura]: https://github.com/Fody/Costura
[Fody]: https://github.com/Fody/Fody/
[Costura.Fody NuGet package]: https://nuget.org/packages/Costura.Fody/
[ILMerge]: https://www.microsoft.com/en-us/download/details.aspx?id=17630 