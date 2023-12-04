Ubuntu Version 20.04
## Installing Docker

```
sudo apt update
```

```
sudo apt install docker.io
```

```
sudo apt update
```


## Installing Docker Compose

```
sudo apt install docker-compose-plugin
```
	Unable to locate package docker-compose-plugin

```
sudo apt install pip
```

```
sudo apt install python3-pip
```
	latest version already

```
sudo pip3 install docker-compose
```

```
docker-compose --version
```
	docker-compose version 1.29.2



## Getting Open Vas
used https://utulsa.hosted.panopto.com/Panopto/Pages/Embed.aspx?id=75912983-0806-47a5-a3ad-acc9018aaec3 as a guide
```
sudo apt-get upgrade
```
```
sudo service docker status
```
	Running

```
sudo docker run -d -p 443:443 --name openvas mikesplain/openvas
```
	pull complete
Waited for all of the NVTs to be downloaded


https://localhost
![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/6423f394-fa0a-4754-a20a-207fa66115eb)

Entered in default admin password and username

went to scans and started a vulnerability scan for my IP

![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/5e6242bb-4431-4de1-b7ff-e118f296118a)


Had a connection issue ![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/7e107cc4-9668-4bb9-8b26-5d062c15e1f9)


restarted the terminal

```
sudo docker run -d -p 443:443 --name openvas2 mikesplain/openvas
```
```
sudo docker run -d -p 443:443 --name openvas3 mikesplain/openvas
```
Tried running the vuln scan again
![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/9a9d6e0e-5a1f-47fb-a643-145d82a59d11)

![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/afb54543-5dcb-4dd8-a3d7-26183208fa58)


![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/4986f751-9e27-4471-92b3-a3c3daa4a728)

Made  the  docker-compose file and tried it again
```
cd ~
```
```
mkdir my_docker_project
```
```
cd my_docker_project
```
```
nano docker-compose.yml
```
```
sudo docker-compose up -d
```
port already allocated
rebooted
```
sudo docker-compose up -d
```
opened up

![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/329b5f8e-9d70-41e7-b7d8-56fe736acfd7)

Changed to:![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/f9402890-4f82-475a-ba4a-9b15972d4c4e)


![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/19fe87cb-a498-482d-9b07-4e1db3d24e6c)
![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/0e6bef54-4467-48be-9068-e0b7a026dee8)


Doing the Vuln Scan again through the created openvass via the yml file
![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/f1834729-fafd-4f01-9e63-9142b81c67fd)
![image](https://github.com/JohnGrewe/Docker-Open-Vas/assets/112670893/41d05c47-1554-4fa4-89ad-4673d18509a9)

