## Docker

### Docker basic command 

#### Management images 
* search docker image 
~~~
docker search <image-name>
~~~

* pull image
~~~
# docker image pull <image-name>
# docker pull <image-name>
~~~

* list docker image
~~~
# docker image ls
# docker images 
~~~

* docker image remove 
~~~
# docker image rm <image-id>
# docker rmi <image-id>
# docker rmi <repository:tag>
# docker rmi <image-id1> <image-id2>
~~~

* remove all docker images 
~~~
# docker rmi $(docker images -q)
~~~
`docker images -q` -> list images' iamge ids

#### Management container
* create
~~~
# docker container create --name webserver nginx 
# docker create --name webserver nginx
~~~

* start
~~~
# docker container start webserver
# docker start webserver
~~~

* stop 
~~~
# docker container stop webserver
# docker stop webserver
~~~

* status
~~~
# docker stats webserver
~~~

* rm
~~~
# docker container rm webserver
# docker rm webserver
~~~

* list
~~~
# docker container ls 
# docker ls 
# docker ls -a
~~~

#### running docker
* docker run 
   * `-d` : background 
   * `-it` : `--interactive` `--tty`
   * `-rm` :  
   * `-v` : `--volume`
   * `-p` : 
   * `--name` : 
   * `--restart` :
   * `--network` : 


