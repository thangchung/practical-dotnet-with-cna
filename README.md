# practical-dotnet-with-cna

```bash
$ choco install pack --version=0.18.0
```

PaketoBuildpacks: https://github.com/paketo-buildpacks/samples/tree/main/dotnet-core

```bash
$ cd service1
$ dotnet publish -c Release -r ubuntu.14.04-x64 --self-contained true
$ pack build webapi --buildpack gcr.io/paketo-buildpacks/dotnet-core
```