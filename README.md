## Starter for writing latex documents

This a starter for generating PDFs from latex documents.
The compiler is housed in a docker container to avoid poluting the host system as typical latex installations tend to be quite massive.
And of course the other benefits from using docker :)

## Prerequisites

modd(a program) for filesystem change watching.

### Installing

```shell
#With go dev tooling installed
env GO111MODULE=on go get github.com/cortesi/modd/cmd/modd
```

## Usage

Start the docker container in the background:

```shell
./scripts/startdaemon.sh

#To stop the daemon, run:
./scripts/stopdaemon.sh
```

Then in a shell run the following in the same directory as "modd.conf":

```shell
modd
```

The filesystem watcher is now running and you should see output from the compiler in the shell and a generated "example.pdf" file.
Try editing "example.tex" now and see if the file is generated anew.

## Credits

For the latex docker environment goes to
https://github.com/blang/latex-docker
