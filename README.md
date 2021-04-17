# practical-dotnet-with-cna

## Build with CNCF `buildpacks`

### Preparation

```bash
$ choco install pack --version=0.18.0
```

PaketoBuildpacks: https://github.com/paketo-buildpacks/samples/tree/main/dotnet-core

### Build services

#### Service 1

```bash
$ pack build vietnamdevsgroup/webapi --env BP_DOTNET_PROJECT_PATH=./service1/src/WebApi 
--buildpack gcr.io/paketo-buildpacks/dotnet-core
```

#### Service 2

```bash
$ pack build vietnamdevsgroup/webapi2 --env BP_DOTNET_PROJECT_PATH=./service2/src/WebApi2 
--buildpack gcr.io/paketo-buildpacks/dotnet-core
```

#### Run all services

```bash
$ docker-compose up
```