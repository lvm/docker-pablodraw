# docker-pablodraw

A container for [PabloDraw](http://picoe.ca/products/pablodraw/).

# how to 

## install

```bash
$ docker pull lvm23/pablodraw
```

or 

```bash
$ git clone https://github.com/lvm/docker-pablodraw && \
  cd docker-pablodraw && \
  docker build -t pablodraw .
```

## run

```bash
$ docker run -it -v /tmp/.X11-unix:/tmp/.X11-unix -v /tmp/asc:/asc -e DISPLAY=unix$DISPLAY --name pablodraw pablodraw
```

`-v /tmp/asc:/asc` is used to mount the container's `/asc` directory to the host `/tmp/asc` directory, you can choose other directory.  
Note: probably you might need to execute `xhost local:root` or `xhost +my-computer-hostname.local`
