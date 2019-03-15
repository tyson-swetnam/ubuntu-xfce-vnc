# ubuntu-xfce-vnc
Ubuntu Bionic XFCE desktop with TurboVNC

This build is taken almost whole cloth from https://hub.docker.com/r/consol/ubuntu-xfce-vnc/dockerfile, https://github.com/ConSol/docker-headless-vnc-container

I have updated the OS to Ubuntu 18.04 Bionic over 16.04 Xenial to correct a dependency problem  I was having with my GIS software.

```
docker run -it -p 5901:5901 -p 6901:6901 tswetnam/ubuntu-xfce-vnc:18.04
```

Run with OpenGL 

```
docker run -it --runtime=nvidia -v /tmp/.X11-unix:/tmp/.X11-unix -v /tmp/.docker.xauth:/tmp/.docker.xauth -p 5901:5901 -p 6901:6901 tswetnam/ubuntu-xfce-vnc:opengl
```
