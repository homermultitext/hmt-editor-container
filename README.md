# A docker container for HMT editing



## TL;DR

If you have docker installed, run this shell script:

```sh
./run-hmt.sh
```

or else run

```sh
docker run -ti --rm -v $(pwd):/work neelsmith/hmteditor:latest
```


to start a container with all the tools you need for editing HMT project material.        

## Latest version: 1.0.0

Images are tagged with versions according to semantic versioning. (See [this blog post](https://medium.com/@mccode/using-semantic-versioning-for-docker-image-tags-dfde8be06699) for a full explanation.)

## What it does

When you run this docker container, you are put in a bash shell in a Linux environment that includes:

- `git` for version control
- `sbt`, the simple build tool (used to run HMT validation scripts)
- `sfst`, the Stuttgart Finite State Transducer (used to build and run morphological parsers)
- `amm`, the Ammonite shell


From this bash shell (once you `cd` to your HMT editing repository), you can start an `sbt console` to run HMT validation scripts, including scripts to build updated morphological parsers as the HMT lexicon and morphological data sets are updated.

## Prerequisites

- docker

That's it!  The rest of the software you need is available from within the docker container.

## Running the container

You can save yourself some typing by using the one-line shell script included in this repository

```sh
./run-hmt.sh
```

If you prefer, you can specify the full docker command:

```sh
docker run -ti --rm -v $(pwd):/work neelsmith/hmteditor:1.0.0
```


## Source

The `ubuntu` directory has the docker build file for a container that was used in the summer of 2019.  The current image is built from the sources in the `alpine` directory.
