# docker-sbt
sbt - Scala Simple Build Tool in Docker

## Usage

    $ docker run -it \
      -v $HOME/.m2:/root/.m2 \
      -v $HOME/.ivy2:/root/.ivy2 \
      -v $HOME/.sbt:/root/.sbt \
      -v $(pwd):/root/workdir \
      axeclbr/sbt
