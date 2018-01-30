

# Summary

A handy Docker build containing JConsole and CJMX -- for profiling Java apps. 

Profbox is a container based set of utilities aimed at performing JMX profiling of Java apps, in particular, DC/OS MoM (Marathon on Marathon), which is itself a Docker container based Java app. Profbox should be useful for connecting to any container based Java app.  Its primary tool is [JConsole](http://openjdk.java.net/tools/svc/jconsole/). JConsole is available by via a noVnc graphical interface to a linux desktop.


## Quick Start
#### Run the docker image listening on port 6080;

```
docker run -it --rm -p 8080:8080 mkurtis/profbox:v5
```

*Now point your browser to: http://localhost:8080/*

