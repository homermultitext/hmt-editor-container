Try configuring HMT editing functionality under alpine Linux.



## Build

From within the `docker` directory,

1. `source envvars.sh` (or otherwise set environment variable `MYNAME`)
2. `docker build -t $IMAGE_NAME:latest .`



## Use


    docker run --rm -it -v $(pwd):/work $IMAGE_NAME:latest /bin/bash


## Notes

https://www.cis.uni-muenchen.de/~schmid/tools/SFST/data/SFST-${SFST_VERSION}.tar.gz
