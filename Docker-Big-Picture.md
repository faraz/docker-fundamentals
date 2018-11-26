# Docker: DevOps Perspective

- When you install docker, you get:
  - the docker client
  - the docker daemon (aka "engine" or "server")
  
- The daemon implements the Docker Engine API
- The client talks to the daemin via a local IPC/Unix socket at `var/run/docker.sock`. On windows this happens via a named pipe at `npipe:////./pipe/docker_engine`

### Images

- Useful to think of a docker image as an object that contains an OS filesystem and an application.
  - Its like a virtual machine template. A virtual machine template is essentially a stopped virtual machine.
  - In the docker world, an image is effectively a stopped container.
  - think of an image as a `class` in the development sense.
  
  
