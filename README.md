# docker-pablodraw

A container for [PabloDraw](http://picoe.ca/products/pablodraw/).

# how to

```bash
$ git clone https://github.com/lvm/docker-pablodraw
$ cd docker-pablodraw
$ docker build -t pablodraw .
$ docker run -it -v /tmp/.X11-unix:/tmp/.X11-unix -e DISPLAY=unix$DISPLAY --name pablodraw pablodraw
```

Note: probably you might need to execute `xhost local:root` or `xhost +my-computer-hostname.local`
