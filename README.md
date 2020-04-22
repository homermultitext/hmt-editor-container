# `hmt-editor-container`

A docker container for HMT editing.


## Current version: 1.0.0


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

    run-hmt.sh

If you prefer, you can specify the full docker command:

    docker run -ti --rm -v $(pwd):/work neelsmith/hmteditor:latest
