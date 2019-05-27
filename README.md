# `hmt-editor-container`

A docker container for HMT editing.


## What it does

When you run this docker container, you are put in a bash shell in a Linux environment that includes:

- `git` for version control
- `sbt`, the simple build tool (used to run HMT validation scripts)
- `sfst`, the Stuttgart Finite State Transducer (used to build and run morphological parsers)


From this bash shell, you can start an `sbt console` to run HMT validation scripts, including scripts to build updated morphological parsers as the HMT lexicon and morphological data sets are updated.

## Prerequisites

- docker

That's it!  The rest of the software you need is available from within the docker container.

## Managing the container

Start the container:

    docker run -ti --name hmt -v $(pwd):/workspace hmteditor

When you're done working, from the bash shell, just `exit`.

To resume work in a stopped container, first restart the container:

    docker restart hmt

then run a bash sh (`/bin/bash`)  in the restarted container:

    docker exec -ti hmt /bin/bash


## Editing in a HMT editor's environment

See the separate documentation (LINK TBA).
