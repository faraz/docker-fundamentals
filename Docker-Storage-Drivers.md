# Docker Storage Driver
- Every docker container gets its own area of local storage where image layers are stacked and the container filesystem is mounted
- This is where all container read/write operations occur ( thus it is important for the performance and stability of containers)
- This local storage area is managed by the _storage driver_ or _graphdriver_
  - Copy-On-Write technologies
  - Some of the storage drivers available for Docker on Linux are:
    - `aufs` (original and oldest)
    - `overlay2` (probably the best choice for the future)
    - `devicemapper`
    - `btrfs`
    - `zfs`
  - Docker on Windows only supports a *single storage driver* : `windowsfilter`
  - Selecting a storage driver is a per node decision - i.e. 1 docker host can host only 1 storage driver. You cannot select a storage driver per container
  - You can set the storage driver in `/etc/docker/daemon.json`

  
    
