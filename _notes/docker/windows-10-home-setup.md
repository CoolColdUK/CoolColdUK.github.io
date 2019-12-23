---
tags: docker, instruction
source: https://forums.docker.com/t/how-to-share-volumes-and-or-drives-using-docker-machine-on-windows-not-beta/20170/6
---
# Windows 10 home setup docker
windows 10 home do not have hyper-v and therefore cannot use docker desktop. In order to get docker working, one must use docker toolbox and virtual box.
The main problem with virtual box is that everything goes through virtual box itself. Therefore, sharing volume and port forwarding has to be setup separately making it more difficult to use.

> Access is via the virtual box ip instead of localhost

## Installation
1. install chocolatey
2. install virtual box using ``choco install virtualbox``
3. install docker toolbox using ``choco install docker-toolbox``
4. install docker cli using ``choco install docker-cli``
5. install make using ``choco install make``
6. install make using ``choco install bash``

## Setup docker (using virtual box)
1. create virtual machine using ``docker-machine create --driver virtualbox default``
2. start vm using ``docker-machine start default``
3. check settings and ip using ``docker-machine env default``
4. check if vm running using ``docker-machine ls``
5. (optional) configure environment to use docker vm ``eval $(docker-machine env default --shell linux)``
6. confirm docker is connected ``docker info``
7. if not connected, run ``@FOR /f "tokens=*" %i IN ('docker-machine env --shell cmd <vm name>') DO @%i`` in cmd with admin privilege
8. If still not connected, try
```
cd "C:\Program Files\Docker\Docker"
./DockerCli.exe -SwitchDaemon
```

## Other setup
### Share folder for virtualbox using command

```
docker-machine stop

vboxmanage sharedfolder add <vm name> --name "<path name on vm>" --hostpath "<path name on local machine>" --automount

docker-machine start
```
This can also be done using virtual box GUI in settings. This is required if volumes are used in docker-compose

### Port forwarding for virtualbox
As the docker is run behind the virtual box, port forwarding is required in order to access the docker. This can be set in virtual box GUI in settings.
Guest ip is the ip of docker found using ``curl ifconfig.me``
After setting port forwarding, the site can be accessed via ip of virtualbox

### Connect to virtual box
1. run bash
2. connect via ssh using ``docker-machine ssh <vm name>``

# Source
1. https://github.com/docker/for-win/issues/1825
2. https://www.sitepoint.com/docker-windows-10-home/
3. https://osric.com/chris/accidental-developer/2018/04/python-flask-and-virtualbox-networking/