# Docker <div align=right><image width=100 height=80 src=https://github.com/wushoucheng30510/Docker/blob/main/pictures/homepage-docker-logo.png ></div>

This page would introduce how to install docker on windows/ubuntu

Install guidence: 
## Basic requirements:
- [Windows](https://www.youtube.com/watch?v=bP0uGUpw_Mo&ab_channel=%E6%AD%90%E9%8E%A7%E8%B1%AA)
       
    - Windows 10 64-bit: Pro, Enterprise or Education (home is not feasible)
    - Activate hyper-V
        
        <div><image width=300 height=250 src=https://github.com/wushoucheng30510/Docker/blob/main/pictures/hyper-v.png ></div>
            
- [Linux](https://www.youtube.com/watch?v=X6sk3OxZkRY&list=PLliocbKHJNwubNT2oK-xlB1GXTXuLFb0I&index=2&ab_channel=%E5%B0%8F%E9%A9%AC%E6%8A%80%E6%9C%AF)
    
## steps
- Windows
    - Go to [*Docker*](https://docs.docker.com/desktop/install/windows-install/) to install docker Desktop

- Linux
    ```shell
    $ sudo apt update
    $ sudo apt upgrade
    $ sudo apt autoremove
    $ sudo apt-get install apt-transport-https ca-certificates curl gnupg-agent software-properties-common
    $ curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
    $ apt-key list
    $ sudo apt-key fingerprint 0EBFCD88
    $ sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu $(lsb_release-cs) stable"
    $ sudo apt update
    $ sudo apt upgrade
    $ sudo apt autoremove
    $ apt show docker-ce
    $ sudo apt install docker-ce docker-ce-cli containerd.io
    ```
                
## Verified
            
```shell
docker version
```
            
<image width=300 height=250 src=https://github.com/wushoucheng30510/Docker/blob/main/pictures/docker%20version.png>
    
```shell
docker run -it ubuntu
```
<image width=300 height=150 src=https://github.com/wushoucheng30510/Docker/blob/main/pictures/docker%20run%20ubuntu.png>


***            
## Useful command
- Check docker version
```shell
docker version
```

- Go to Ubuntu
```shell
docker run -it ubuntu
```

- Check docker image
```shell
docker image ls
```

- Pull a docker image
```shell
docker image pull $docker      ex: docker image pull python:3.7
```

- create a docker container
```shell
nano Dockerfile

#From $env
#Run mkdir /test
#copy $file /test
#CMD["node","/test/$file"]  (run,file)
```

- build a docker image ("." is required)
```shell
docker image build -t $imageName:v01 .
```

- run a docker container
```shell
docker container run $dockerName
```

- stop a docker container
```shell
docker container stop $dockerName
```

- start a docker container
```shell
docker container start $dockerName
```

- list all the docker container
```shell
docker container ls -a
```

- list the running docker 
```shell
docker container ls
```

- delete a docker container
```shell
docker container rm -f $dockerName
```

- delete all docker containers
```shell
docker container prune
```







