# Information

- This report was generated on Wednesday, March 28, 2018 at 12:03:58 PM GMT
- The desired Cake version is `0.26.0`
- The `Cake Core Version` and `Cake Common Version` columns  show the version referenced by a given addin
- The `Cake Core IsPrivate` and `Cake Common IsPrivate` columns indicate whether the references are marked as private. In other words, we are looking for references with the `PrivateAssets=All` attribute like in this example: `<PackageReference Include="Cake.Common" Version="0.26.0" PrivateAssets="All" />`
- The `Framework` column shows the .NET framework(s) targeted by a given addin. As of Cake 0.26.0, addins should target netstandard2.0 only (there is no need to multi-target)
- The `Icon` column indicates if the nuget package for your addin uses the cake-contrib icon.
- The `YAML` column indicates if there is a `.yml` file describing the addin in this [repo](https://github.com/cake-build/website/tree/develop/addins).

- The analysis discovered 216 addins
  - 192 were successfully audited (see the 'Addins' section)
  - 24 could not be audited (see the 'Exceptions' section)

# Addins

| Name | Cake Core Version | Cake Core IsPrivate | Cake Common Version | Cake Common IsPrivate | Framework | Icon | YAML |
| --- | :---: | :---: | :---: | :---: | :---: | :---: | :---: |
| [Cake.ActiveDirectory](https://github.com/RadioSystems/Cake.ActiveDirectory) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.AliaSql](https://github.com/cake-contrib/Cake.AliaSql) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Android.Adb](https://github.com/Redth/Cake.Android.Adb) | Unknown :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Android.AvdManager](https://github.com/redth/Cake.Android.AvdManager) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0 :white_check_mark: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Android.SdkManager](https://github.com/Redth/Cake.Android.SdkManager) | Unknown :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.AndroidAppManifest](https://github.com/ghuntley/Cake.AndroidAppManifest) | 0.22.0 :small_red_triangle: | false :small_red_triangle: | 0.22.0 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Apigee](https://github.com/LittleColin/Cake.Apigee) | 0.22.2 :small_red_triangle: | true :white_check_mark: |  |  | v4.6.2 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.AppleSimulator](https://github.com/ghuntley/Cake.AppleSimulator) | Unknown :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.AppPackager](https://github.com/phillipsj/Cake.AppPackager) | 0.16.2 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net45 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Apprenda](https://github.com/apprenda/Cake.Apprenda) | 0.24.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.AppVeyor](https://github.com/Redth/Cake.AppVeyor) | 0.22.0 :small_red_triangle: | false :small_red_triangle: | 0.22.0 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.APT.Module](https://github.com/agc93/Cake.APT.Module) | 0.20.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net45 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.ArgumentHelpers](https://github.com/patridge/Cake.ArgumentHelpers) | Unknown :small_red_triangle: | false :small_red_triangle: | Unknown :small_red_triangle: | false :small_red_triangle: | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.ArtifactDrop](https://github.com/stefandevo/Cake.ArtifactDrop) | 0.20.0 :small_red_triangle: | false :small_red_triangle: | 0.20.0 :small_red_triangle: | false :small_red_triangle: | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.AssemblyInfoReflector](https://github.com/wexman/Cake.AssemblyInfoReflector) | 0.26.1 :white_check_mark: | false :small_red_triangle: | 0.26.1 :white_check_mark: | false :small_red_triangle: | netstandard2.0, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.AutoRest](https://github.com/agc93/Cake.AutoRest) | 0.19.5 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net45 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.AWS.CloudFront](https://github.com/SharpeRAD/Cake.AWS.CloudFront) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.AWS.CodeDeploy](https://github.com/SharpeRAD/Cake.AWS.CodeDeploy) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.AWS.EC2](https://github.com/SharpeRAD/Cake.AWS.EC2) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.AWS.ElasticBeanstalk](https://github.com/mathieukempe/Cake.AWS.ElasticBeanstalk) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.AWS.ElasticLoadBalancing](https://github.com/SharpeRAD/Cake.AWS.ElasticLoadBalancing) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.AWS.Lambda](https://github.com/SharpeRAD/Cake.AWS.Lambda) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.AWS.Route53](https://github.com/SharpeRAD/Cake.AWS.Route53) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.AWS.S3](https://github.com/SharpeRAD/Cake.AWS.S3) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.AzCopy](https://github.com/agc93/Cake.AzCopy) | 0.25.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net46 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.Azure](https://github.com/DixonDs/Cake.Azure) | 0.22.2 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.AzureStorage](https://github.com/RadioSystems/Cake.AzureStorage) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Bower](https://github.com/cake-contrib/Cake.Bower) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.BuildSystems.Module](https://github.com/agc93/Cake.BuildSystems.Module) | 0.24.0 :small_red_triangle: | false :small_red_triangle: | 0.24.0 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Bumpy](https://github.com/cake-contrib/Cake.Bumpy) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.CakeBoss](https://github.com/SharpeRAD/CakeBoss) | 0.6.4 :small_red_triangle: | true :white_check_mark: | 0.8.0 :small_red_triangle: | true :white_check_mark: | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.CakeMail](https://github.com/cake-contrib/Cake.CakeMail/) | 0.26.1 :white_check_mark: | true :white_check_mark: | 0.26.1 :white_check_mark: | true :white_check_mark: | netstandard2.0 :white_check_mark: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Chocolatey.Module](https://github.com/cake-contrib/Cake.Chocolatey.Module/) | 0.22.2 :small_red_triangle: | true :white_check_mark: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.Chutzpah](https://github.com/cake-contrib/Cake.Chutzpah) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.CK.Pack](https://github.com/Invenietis/ck-globbing) | 0.13.0 :small_red_triangle: | true :white_check_mark: | 0.13.0 :small_red_triangle: | true :white_check_mark: | v4.5.1 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.CMake](https://github.com/cake-contrib/Cake.CMake) | 0.18.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.CodeAnalysisReporting](https://github.com/cake-contrib/Cake.CodeAnalysisReporting) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Codecov](https://github.com/cake-contrib/Cake.Codecov) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Compression](https://github.com/akordowski/Cake.Compression/) | 0.26.1 :white_check_mark: | false :small_red_triangle: | 0.26.1 :white_check_mark: | false :small_red_triangle: | v4.6.1 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Coveralls](https://github.com/cake-contrib/Cake.Coveralls) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | net46, netstandard2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.CsvHelper](https://github.com/RadioSystems/Cake.CsvHelper) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Curl](https://github.com/ecampidoglio/Cake.Curl) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.DependencyCheck](https://github.com/burakince/Cake.DependencyCheck) | 0.21.1 :small_red_triangle: | false :small_red_triangle: | 0.21.1 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net45, net46, netcoreapp2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.DeployParams](https://github.com/wooboo/Cake.DeployParams) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.DevicesXunitTestReceiver](https://github.com/pellet/Cake.DevicesXunitTestReceiver) | 0.22.0 :small_red_triangle: | false :small_red_triangle: | 0.22.0 :small_red_triangle: | false :small_red_triangle: | netstandard2 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Dialog](https://github.com/wk-j/cake-dialog) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.DNF.Module](https://github.com/cake-contrib/Cake.DNF.Module) | 0.22.2 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net46 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.DocCreator](https://bitbucket.org/agc93/DocCreator/) | 0.19.4 :small_red_triangle: | false :small_red_triangle: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.DocFx](https://github.com/cake-contrib/Cake.DocFx) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Docker](https://github.com/MihaMarkic/Cake.Docker) | 0.26.0 :white_check_mark: | true :white_check_mark: |  |  | netstandard2.0 :white_check_mark: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.DocumentDb](https://github.com/BudSystemLimited/Cake.DocumentDb) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.DoInDirectory](https://github.com/pitermarx/Cake.DoInDirectory) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.DotNetCoreEf](https://github.com/cake-contrib/Cake.DotNetCoreEf) | 0.17.0 :small_red_triangle: | true :white_check_mark: | 0.17.0 :small_red_triangle: | true :white_check_mark: | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Email](https://github.com/cake-contrib/Cake.Email/) | 0.26.1 :white_check_mark: | true :white_check_mark: | 0.26.1 :white_check_mark: | true :white_check_mark: | netstandard2.0 :white_check_mark: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Ember](https://github.com/cake-contrib/Cake.Ember/) | 0.17.0 :small_red_triangle: | true :white_check_mark: | 0.17.0 :small_red_triangle: | true :white_check_mark: | v4.5.2 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Endpoint](https://github.com/cake-contrib/Cake.Endpoint/) | 0.26.0 :white_check_mark: | true :white_check_mark: | 0.26.0 :white_check_mark: | true :white_check_mark: | netstandard2.0 :white_check_mark: | true :white_check_mark: | true :white_check_mark: |
| [Cake.EntityFramework](https://github.com/cake-contrib/Cake.EntityFramework/) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6, v4.6.1 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.EnvXmlTransform](https://github.com/nengberg/cake-envxmltransform) | 0.17.0 :small_red_triangle: | true :white_check_mark: | 0.17.0 :small_red_triangle: | true :white_check_mark: | v4.6.1 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.ExtendedNuGet](https://github.com/Redth/Cake.ExtendedNuGet) | 0.26.1 :white_check_mark: | false :small_red_triangle: | 0.26.1 :white_check_mark: | false :small_red_triangle: | net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Fastlane](https://github.com/RLittlesII/Cake.Fastlane) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | net46, netstandard2.0 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Figlet](https://github.com/enkafan/Cake.Figlet) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0 :white_check_mark: | true :white_check_mark: | true :white_check_mark: |
| [Cake.FileHelpers](https://github.com/Redth/Cake.FileHelpers) | 0.22.0 :small_red_triangle: | false :small_red_triangle: | 0.22.0 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.FileSet](https://github.com/CleanKludge/Cake.FileSet) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net46, netcoreapp1.1 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.FluentMigrator](https://github.com/cake-contrib/Cake.FluentMigrator) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Flyaway](https://github.com/buthomas/Cake.Flyway) | 0.21.1 :small_red_triangle: | false :small_red_triangle: | 0.21.1 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net45, net46 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Ftp](https://github.com/phillipsj/Cake.Ftp) | 0.22.2 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Gem](https://github.com/cake-contrib/Cake.Gem) | 0.17.0 :small_red_triangle: | true :white_check_mark: | 0.17.0 :small_red_triangle: | true :white_check_mark: | v4.5.2 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Genymotion](https://github.com/ghuntley/Cake.Genymotion) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5.2 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Git](https://github.com/cake-contrib/Cake_Git) | 0.26.0 :white_check_mark: | true :white_check_mark: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.GitPackager](https://github.com/ilich/Cake.GitPackager) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Gitter](https://github.com/cake-contrib/Cake.Gitter) | 0.26.0 :white_check_mark: | false :small_red_triangle: | 0.26.0 :white_check_mark: | false :small_red_triangle: | net46, netstandard2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Gradle](https://github.com/abeggchr/cake-gradle/blob/master/README.md) | Unknown :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.2 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.Graph](https://github.com/wozzo/Cake.Graph) | 0.25.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.Grunt](https://github.com/cake-contrib/Cake.Grunt/) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0 :white_check_mark: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.Gulp](https://github.com/cake-contrib/cake-gulp) | 0.22.0 :small_red_triangle: | true :white_check_mark: |  |  | net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Handlebars](https://github.com/agc93/Cake.Handlebars) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | net46, netstandard2.0 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.Helm](https://github.com/santey/Cake.Helm) | 0.25.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard2.0 :white_check_mark: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Hg](https://github.com/cake-contrib/Cake.Hg) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | net461 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.HgVersion](https://github.com/vCipher/Cake.HgVersion) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | net461 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.HipChat](https://github.com/cake-contrib/Cake.HipChat) | 0.17.0 :small_red_triangle: | true :white_check_mark: | 0.17.0 :small_red_triangle: | true :white_check_mark: | v4.5.2 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.HockeyApp](https://github.com/cake-contrib/Cake.HockeyApp) | 0.26.0 :white_check_mark: | true :white_check_mark: |  |  | net46, netstandard2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Homebrew](https://github.com/RLittlesII/Cake.Homebrew) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Hosts](https://github.com/AMVSoftware/Cake.Hosts) | 0.23.0 :small_red_triangle: | true :white_check_mark: |  |  | net46, netcoreapp1.1 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Http](https://github.com/cake-contrib/Cake.Http) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.IIS](https://github.com/SharpeRAD/Cake.IIS) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net461, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.ImageOptimizer](https://github.com/SharpeRAD/Cake.ImageOptimizer) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Incubator](https://github.com/cake-contrib/Cake.Incubator) | 0.22.0 :small_red_triangle: | false :small_red_triangle: | 0.22.0 :small_red_triangle: | false :small_red_triangle: | netstandard2.0, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Intellisense.Core](https://github.com/Meir017/Cake.Intellisense) | 0.20.0 :small_red_triangle: | false :small_red_triangle: |  |  | netcoreapp2.0 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.IntellisenseGenerator](https://github.com/Meir017/Cake.Intellisense) | 0.20.0 :small_red_triangle: | false :small_red_triangle: |  |  | netcoreapp2.0 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.ISO](https://github.com/austinlparker/Cake.ISO) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.2 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Issues](https://github.com/cake-contrib/Cake.Issues) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Issues.DocFx](https://github.com/cake-contrib/Cake.Issues.DocFx) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Issues.EsLint](https://github.com/cake-contrib/Cake.Issues.EsLint) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Issues.InspectCode](https://github.com/cake-contrib/Cake.Issues.InspectCode) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Issues.Markdownlint](https://github.com/cake-contrib/Cake.Issues.Markdownlint) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Issues.MsBuild](https://github.com/cake-contrib/Cake.Issues.MsBuild) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Issues.PullRequests](https://github.com/cake-contrib/Cake.Issues.PullRequests) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.JMeter](https://github.com/pitermarx/Cake.JMeter) | 0.22.2 :small_red_triangle: | true :white_check_mark: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Json](https://github.com/Redth/Cake.Json) | 0.22.0 :small_red_triangle: | false :small_red_triangle: | 0.22.0 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Karma](https://github.com/cake-contrib/Cake.Karma/) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.KeePass](https://github.com/Ashthos/Cake.KeePass) | 0.19.5 :small_red_triangle: | false :small_red_triangle: |  |  | v4.5.2 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Kudu](https://github.com/cake-contrib/Cake.Kudu) | 0.26.0 :white_check_mark: | false :small_red_triangle: | 0.26.0 :white_check_mark: | false :small_red_triangle: | netstandard2.0, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Kudu.Client](https://github.com/cake-contrib/Cake.Kudu.Client) | 0.26.0 :white_check_mark: | true :white_check_mark: |  |  | netstandard2.0, net461 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Liquibase](https://github.com/papauorg/Cake.Liquibase) |  |  | 0.22.2 :small_red_triangle: | false :small_red_triangle: | net461 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.Mage](https://github.com/cake-contrib/Cake.Mage) | 0.18.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Markdown-Pdf](https://github.com/wozzo/Cake.Markdown-Pdf) | 0.21.1 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.MarkdownToPdf](https://github.com/twenzel/Cake.MarkdownToPdf) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.MicrosoftTeams](https://github.com/cake-contrib/Cake.MicrosoftTeams) | 0.26.0 :white_check_mark: | true :white_check_mark: |  |  | netstandard2.0, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.MiniCover](https://github.com/nlowe/Cake.MiniCover) | 0.26.0 :white_check_mark: | false :small_red_triangle: | 0.26.0 :white_check_mark: | false :small_red_triangle: | netstandard2.0 :white_check_mark: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.MobileCenter](https://github.com/cake-contrib/Cake.MobileCenter) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0 :white_check_mark: | true :white_check_mark: | true :white_check_mark: |
| [Cake.MonoApiTools](https://github.com/Redth/Cake.MonoApiTools) | Unknown :small_red_triangle: | false :small_red_triangle: | Unknown :small_red_triangle: | false :small_red_triangle: | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.MSBuildTask](https://github.com/marcosnz/Cake.MSBuildTask) | Unknown :small_red_triangle: | false :small_red_triangle: | Unknown :small_red_triangle: | false :small_red_triangle: | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.MsDeploy](https://github.com/cake-contrib/Cake.MsDeploy) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.NDepend](https://github.com/joaoasrosa/cake-ndepend) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | net461, netstandard2.0, netcoreapp2.0 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Netlify](https://github.com/cake-contrib/Cake.Netlify) | 0.22.2 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.NewRelic](https://github.com/BMWilding/Cake.NewRelic) | 0.17.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Npm](https://github.com/cake-contrib/cake-npm) | 0.26.0 :white_check_mark: | true :white_check_mark: |  |  | net46, netstandard2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Npx](https://github.com/michael-wolfenden/Cake.Npx) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0 :white_check_mark: | true :white_check_mark: | false :small_red_triangle: |
| [Cake.NSpec](https://github.com/app-iron/Cake.NSpec/tree/master) | Unknown :small_red_triangle: | false :small_red_triangle: | Unknown :small_red_triangle: | false :small_red_triangle: | v4.5, v4.6.1 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.NSwag](https://github.com/agc93/Cake.NSwag) | 0.19.5 :small_red_triangle: | false :small_red_triangle: |  |  | net45 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.NSwag.Console](https://github.com/agc93/Cake.NSwag.Console) | 0.19.5 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net45 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Nuget.Versioning](https://github.com/Kemyke/Cake.Nuget.Versioning) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, netcoreapp2.0 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.OctoDeploy](https://github.com/NinetailLabs/Cake.OctoDeploy) | 0.17.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net45, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.OctoVariapus](https://github.com/osoykan/Cake.OctoVariapus) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Openshift](https://github.com/cake-contrib/Cake.Openshift) | 0.22.2 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Orchard](https://github.com/RadioSystems/Cake.Orchard) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Paket](https://github.com/larzw/Cake.Paket) | Unknown :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Paket.Module](https://github.com/cake-contrib/Cake.Paket) | Unknown :small_red_triangle: | true :white_check_mark: |  |  | v4.6 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Path](https://github.com/CleanKludge/Cake.Path) | 0.19.5 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net45, netcoreapp1.1 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Plist](https://github.com/cake-contrib/Cake.Plist) | 0.22.2 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.2 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Powershell](https://github.com/SharpeRAD/Cake.Powershell) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.ProGet](https://github.com/apprenda/Cake.ProGet) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.ProtobufTools](https://github.com/cake-contrib/Cake.ProtobufTools) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0 :white_check_mark: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Putty](https://github.com/MihaMarkic/Cake.Putty) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, netcoreapp2.0 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Raygun](https://github.com/ghuntley/Cake.Raygun) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5.2 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.ReSharperReports](https://github.com/cake-contrib/Cake.ReSharperReports) | 0.26.0 :white_check_mark: | false :small_red_triangle: | 0.26.0 :white_check_mark: | false :small_red_triangle: | net46, netstandard2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.ResxConverter](https://github.com/cake-contrib/Cake.ResxConverter) | Unknown :small_red_triangle: | false :small_red_triangle: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.ScheduledTasks](https://github.com/hawker-am/Cake.ScheduledTasks) | 0.10.1 :small_red_triangle: | true :white_check_mark: |  |  | v4.5.2 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Scripty](https://github.com/daveaglick/Scripty) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6, v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.SemVer](https://github.com/Redth/Cake.SemVer) | 0.22.0 :small_red_triangle: | false :small_red_triangle: | 0.22.0 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.SendGrid](https://github.com/cake-contrib/Cake.SendGrid/) | 0.26.1 :white_check_mark: | true :white_check_mark: | 0.26.1 :white_check_mark: | true :white_check_mark: | netstandard2.0 :white_check_mark: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Services](https://github.com/SharpeRAD/Cake.Services) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.SimpleHTTPServer](https://github.com/cake-addin/cake-server) | Unknown :small_red_triangle: | false :small_red_triangle: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Slack](https://github.com/cake-contrib/Cake.Slack) | 0.26.0 :white_check_mark: | false :small_red_triangle: | 0.26.0 :white_check_mark: | false :small_red_triangle: | net46, netstandard2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.SmartAssembly](https://github.com/cake-contrib/Cake.SmartAssembly) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Sonar](https://github.com/AgileArchitect/Cake.Sonar) | 0.26.1 :white_check_mark: | false :small_red_triangle: | 0.26.1 :white_check_mark: | false :small_red_triangle: | net46, netstandard2.0, netcoreapp2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.SonarScanner](https://github.com/pitermarx/Cake.SonarScanner) | 0.22.1 :small_red_triangle: | true :white_check_mark: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.SqlPackage](https://github.com/RLittlesII/Cake.SqlPackage) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | net46, netstandard2.0, netcoreapp2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.SqlServer](https://github.com/AMVSoftware/Cake.SqlServer) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.7 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.SqlServerPackager](https://github.com/ilich/Cake.SqlServerPackager) | 0.17.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.SqlTools](https://github.com/SharpeRAD/Cake.SqlTools) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Squirrel](https://github.com/phillipsj/Cake.Squirrel) | 0.22.2 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.SSRS](https://github.com/cake-contrib/Cake.SSRS) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard2.0, net461 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Storyteller](https://github.com/bibodha/Cake.Storyteller) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5.2 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.StrongNameTool](https://github.com/SaferSocietyGroup/cake.strongnametool) | 0.25.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6.1 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Svn](https://github.com/cake-contrib/Cake.Svn) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.SynVer](https://github.com/fsprojects/Cake.SynVer) | 0.18.0 :small_red_triangle: | false :small_red_triangle: | 0.18.0 :small_red_triangle: | false :small_red_triangle: | v4.5.2 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Talend](https://github.com/RadioSystems/Cake.Talend) | 0.23.0 :small_red_triangle: | false :small_red_triangle: | 0.23.0 :small_red_triangle: | false :small_red_triangle: | v4.6.1 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Terraform](https://github.com/erikvanbrakel/Cake.Terraform) | Unknown :small_red_triangle: | false :small_red_triangle: |  |  | net461, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Tfs.AutoMerge](https://github.com/mabreuortega/Cake.Tfs) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Tfs.Build.Variables](https://github.com/Kemyke/Cake.Tfs.Build.Variables) | 0.26.0 :white_check_mark: | false :small_red_triangle: | 0.26.0 :white_check_mark: | false :small_red_triangle: | netstandard2.0 :white_check_mark: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Tfx](https://github.com/cake-contrib/Cake.Tfx) | 0.17.0 :small_red_triangle: | true :white_check_mark: | 0.17.0 :small_red_triangle: | true :white_check_mark: | v4.5.2 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Topshelf](https://github.com/SharpeRAD/Cake.Topshelf) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46, netstandard1.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Transifex](https://github.com/cake-contrib/Cake.Transifex) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Twitter](https://github.com/cake-contrib/Cake.Twitter) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | net46, netstandard2.0 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.UncUtils](https://github.com/kolletzki/Cake.UncUtils) | 0.17.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Unity](https://github.com/cake-contrib/Cake.Unity) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.UrlLoadDirective.Module](https://github.com/Redth/Cake.UrlLoadDirective.Module) | 0.22.2 :small_red_triangle: | false :small_red_triangle: | 0.22.2 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.UServer](https://github.com/cake-addin/cake-u-server) | Unknown :small_red_triangle: | false :small_red_triangle: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Utility](https://github.com/waynebrantley/Cake.Utility) | 0.26.0 :white_check_mark: | false :small_red_triangle: | 0.26.0 :white_check_mark: | false :small_red_triangle: | v4.6.1 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.Vagrant](https://github.com/cake-contrib/Cake.Vagrant) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5.2 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.ViewCompiler](https://github.com/agc93/Cake.ViewCompiler/) | 0.11.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5.2 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.VsCode](https://github.com/cake-contrib/Cake.VsCode) | 0.17.0 :small_red_triangle: | true :white_check_mark: | 0.17.0 :small_red_triangle: | true :white_check_mark: | v4.5.2 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.VSforMac](https://github.com/osamarabea/Cake.Xamarin) | Unknown :small_red_triangle: | false :small_red_triangle: | Unknown :small_red_triangle: | false :small_red_triangle: | v4.5 :small_red_triangle: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.VsixSignTool](https://github.com/MihaMarkic/Cake.VsixSignTool) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.VsMetrics](https://github.com/cake-contrib/Cake.VsMetrics) | 0.26.1 :white_check_mark: | true :white_check_mark: |  |  | v4.6 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Watch](https://github.com/cake-addin/cake-watch) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.WebDeploy](https://github.com/SharpeRAD/Cake.WebDeploy) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | net46 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.Webpack](https://github.com/philo/cake-webpack) | 0.17.0 :small_red_triangle: | true :white_check_mark: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.WindowsAppStore](https://github.com/cake-contrib/Cake.WindowsAppStore) | 0.26.1 :white_check_mark: | true :white_check_mark: |  |  | netstandard2.0 :white_check_mark: | false :small_red_triangle: | false :small_red_triangle: |
| [Cake.WinSCP](https://github.com/ilich/Cake.WinSCP) | 0.17.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.5 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Wyam](https://github.com/Wyamio/Wyam) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, net462 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Xamarin](https://github.com/Redth/Cake.Xamarin) | 0.22.0 :small_red_triangle: | false :small_red_triangle: | 0.22.0 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.XCode](https://github.com/Redth/Cake.XCode) | 0.22.0 :small_red_triangle: | false :small_red_triangle: | 0.22.0 :small_red_triangle: | false :small_red_triangle: | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.XComponent](https://github.com/xcomponent/Cake.XComponent) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | v4.6, v4.5.1 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.XdtTransform](https://github.com/phillipsj/Cake.XdtTransform) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [Cake.XmlConfigStructureBuilder](https://github.com/graph-uk/Cake.XmlConfigStructureBuilder) | 0.25.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard2.0, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.XmlDocMarkdown](https://github.com/ejball/XmlDocMarkdown) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | netstandard2.0, net461, netstandard1.1 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Yaml](https://github.com/Redth/Cake.Yaml) | 0.22.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, net46 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Yarn](https://github.com/MilovanovM/cake-yarn) | 0.26.1 :white_check_mark: | false :small_red_triangle: |  |  | v4.6.2 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |
| [Cake.Yeoman](https://github.com/cake-contrib/Cake.Yeoman) | 0.26.0 :white_check_mark: | false :small_red_triangle: |  |  | v4.6 :small_red_triangle: | true :white_check_mark: | true :white_check_mark: |
| [MagicChunks](https://github.com/sergeyzwezdin/magic-chunks) | 0.23.0 :small_red_triangle: | false :small_red_triangle: |  |  | netstandard1.6, netstandard1.3 :small_red_triangle: | false :small_red_triangle: | true :white_check_mark: |

# Exceptions

**Cake.AzureBlobStorage**: We were unable to determine the Github repo URL. Most likely this means that the PackageProjectUrl is missing from the csproj.

**Cake.CachedNpm**: We were unable to determine the Github repo URL. Most likely this means that the PackageProjectUrl is missing from the csproj.

**Cake.ClickTwice**: DownloadProjectFilesAsync: repos/agc93/clicktwice/contents/src/ClickTwice.Handlers.Core/ClickTwice.Handlers.Core.csproj was not found.
DownloadProjectFilesAsync: repos/agc93/clicktwice/contents/src/ClickTwice.Templates.SolidState.Package/ClickTwice.Templates.SolidState.Package.csproj was not found.
This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.FtpDeploy**: We were unable to determine the Github repo URL. Most likely this means that the PackageProjectUrl is missing from the csproj.

**Cake.GithubUtility**: This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.Intellisense**: This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.Issues.PullRequests.Tfs**: This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.Issues.Reporting**: FindSolutionPathAsync: Value cannot be null.
Parameter name: owner
This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.Issues.Reporting.Generic**: FindSolutionPathAsync: Value cannot be null.
Parameter name: owner
This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.Issues.Testing**: The project does not exist: https://github.com/cake-contrib/Cake.Issues.Testing
This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.Jira**: We were unable to determine the Github repo URL. Most likely this means that the PackageProjectUrl is missing from the csproj.

**Cake.LongPath.Module**: This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.Microsoft.Extensions.Configuration**: We were unable to determine the Github repo URL. Most likely this means that the PackageProjectUrl is missing from the csproj.

**Cake.Newman**: This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.Packages**: We were unable to determine the Github repo URL. Most likely this means that the PackageProjectUrl is missing from the csproj.

**Cake.Parallel.Module**: We were unable to determine the Github repo URL. Most likely this means that the PackageProjectUrl is missing from the csproj.

**Cake.PinNuGetDependency**: FindSolutionPathAsync: Value cannot be null.
Parameter name: owner
This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.ProjHelpers**: DownloadProjectFilesAsync: repos/orialmog/Cake.ProjHelpers/contents/src/Cake.ProjHelpers/Cake.ProjHelpers.csproj was not found.
This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.ServiceOrchestration**: This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.SimpleVersionIncrement**: We were unable to determine the Github repo URL. Most likely this means that the PackageProjectUrl is missing from the csproj.

**Cake.SquareLogo**: We were unable to determine the Github repo URL. Most likely this means that the PackageProjectUrl is missing from the csproj.

**Cake.StyleCop**: DownloadProjectFilesAsync: repos/Ashthos/Cake.StyleCop/contents/Cake.Stylecop/Cake.Stylecop.csproj was not found.
This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.VersionReader**: DownloadProjectFilesAsync: repos/NinetailLabs/Cake.VersionReader/contents/Cake.VersionReader/Cake.VersionReader.csproj was not found.
This addin seem to be referencing neither Cake.Core nor Cake.Common.

**Cake.Xamarin.Build**: This addin seem to be referencing neither Cake.Core nor Cake.Common.

