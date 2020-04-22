


## Build and publish



From within the `docker` directory,

    source envvars.sh

### Build

    docker build -t ${IMAGE_NAME}:latest .

### Use or test a locally built image

    run.sh

### Publish a tested version


```sh
    docker login #  if you haven't already
    ./publish.sh
```
