

# Summary

A handy Docker build containing JConsole and CJMX -- for profiling Java apps. 

Profbox is a container based set of utilities aimed at performing JMX profiling of Java apps, in particular, DC/OS MoM (Marathon on Marathon), which is itself a Docker container based Java app. Profbox should be useful for connecting to any container based Java app.  It primary tool is [JConsole](http://openjdk.java.net/tools/svc/jconsole/) or [CJMX](https://github.com/cjmx/cjmx) to provide command line based JMX Client.  JConsole is available by virtue of the noVnc graphical interface, while cjmx is command line based.   The noVnc setup is based on the excellent [dorowu](https://hub.docker.com/r/dorowu/) build, [ubuntu-desktop-lxde-vnc](https://hub.docker.com/r/dorowu/ubuntu-desktop-lxde-vnc/), which is a Docker image to provide HTML5 VNC interface to access Ubuntu 16.04 LXDE desktop environment.


## Quick Start
#### Run the docker image listening on port 6080;

```
docker run -it --rm -p 6080:80 dorowu/ubuntu-desktop-lxde-vnc
```

*Now point your browser to: http://localhost:6080/*

## Additional Options

#### Connect with VNC Viewer and Protect with a Custom VNC Password;

```
docker run -it --rm -p 6080:80 -p 5900:5900 dorowu/ubuntu-desktop-lxde-vnc
```

*Now connect by pointing your VNC viewer to localhost port 5900.*

```
docker run -it --rm -p 6080:80 -p 5900:5900 -e VNC_PASSWORD=mypassword dorowu/ubuntu-desktop-lxde-vnc
```

*A prompt will ask password either in the browser or vnc viewer.*


