# Build Packs using ACR Tasks

[Buildpacks](https://buildpacks.io/) provide a higher-level abstraction for building apps. You can build images using buildpack and ACR tasks. 

## Get the Buildpack CLI image

Ensure you have an image that has Buildpack CLI. You need the `pack` binary to run the build commands.
You can use the [Dockerfile](pack/Dockerfile) in the repo to obtain the image you your registry using [`acr build`](https://aka.ms/acr/build)

```bash
az configure --defaults acr=myregistry
az acr build -t pack:latest -f ./pack/Dockerfile .  
```

## Pack a node app

Build the sample node app using the [acr.yaml](node-app/acr.yaml)

```bash
cd ./node-app/
az acr run -f acr.yaml .
```