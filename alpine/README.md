Try configuring HMT editing functionality under alpine Linux.



## Build and publish



From within the `docker` directory,

    source envvars.sh

### Build

    docker build -t ${IMAGE_NAME}:latest .

### Publish a tested version

    docker login // if haven't already
    docker push ${IMAGE_NAME}:latest

    docker tag ${IMAGE_NAME}:latest registry:${MAJOR_VERSION}
    docker push ${IMAGE_NAME}:${MAJOR_VERSION}

    docker tag ${IMAGE_NAME}:latest ${IMAGE_NAME}:$MAJOR_VERSION.$MINOR_VERSION
    docker push ${IMAGE_NAME}:$MAJOR_VERSION.$MINOR_VERSION

    docker tag ${IMAGE_NAME}:latest ${IMAGE_NAME}:$MAJOR_VERSION.$MINOR_VERSION.$PATCH_VERSION
    docker push ${IMAGE_NAME}:$MAJOR_VERSION.$MINOR_VERSION.$PATCH_VERSION


## Use or test locally built image

`run.sh` will start a `bash` shell in the container.
