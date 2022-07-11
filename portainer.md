## Portainer   


 
### Install   
>`docker standalone` && `centos`
  
1. create volume 
~~~
#docker volume create portainer_data
~~~

2. portainer pull && run 
~~~
#docker run -d -p 9000:9000 -p 9443:9443 --restart=always \
  --name portainer -v /var/run/docker.sock:/var/run/docker.sock \
  -v portainer_data portainer/portainer-ce:2.9.3
~~~

3. check docker
~~~
#docker ps
~~~


* * * 
* [deploy portainer ce](https://docs.portainer.io/v/ce-2.9/start/install/server/docker/linux)
