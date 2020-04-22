


## Build and publish



From within the `docker` directory,

    source envvars.sh

### Build

    docker build -t ${IMAGE_NAME}:latest .

### Publish a tested version

    docker login // you if haven't already
    ./publish.sh


## Use or test locally built image

`run.sh` will start a `bash` shell in the container.
