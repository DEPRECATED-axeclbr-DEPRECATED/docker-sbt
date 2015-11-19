# docker-sbt
sbt - Scala Simple Build Tool in Docker

## Usage

Example of usage with explicit cpu- and memory-settings. Please adjust to your needs.

    $ docker run -it \
      --rm \
      --cpuset-cpus=0-7 \
      --memory="4g" \
      -v $HOME/.m2:/root/.m2 \
      -v $HOME/.ivy2:/root/.ivy2 \
      -v $HOME/.sbt:/root/.sbt \
      -v $(pwd):/root/workdir \
      axeclbr/sbt


## Hint for OS X users

Because the build process heavily writes to the hosts filesystem and Vboxfs is very slow, it is strongly recommended to enable NFS. An easy way to do this is provided by (docker-machine-nfs)[https://github.com/adlogix/docker-machine-nfs].

