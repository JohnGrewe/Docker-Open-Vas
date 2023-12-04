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
![[Pasted image 20231202223807.png]]
Entered in default admin password and username

went to scans and started a vulnerability scan for my IP

![[Pasted image 20231202224040.png]]

Had a connection issue ![[Pasted image 20231202225132.png]]

restarted the terminal

```
sudo docker run -d -p 443:443 --name openvas2 mikesplain/openvas
```
```
sudo docker run -d -p 443:443 --name openvas3 mikesplain/openvas
```
Tried running the vuln scan again
![[Pasted image 20231202231325.png]]
![[Pasted image 20231202231549.png]]

![[Pasted image 20231202232429.png]]
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
![[Pasted image 20231202234424.png]]
Changed to:![[Pasted image 20231203000617.png]]

![[Pasted image 20231202235001.png]]
![[Pasted image 20231203000514.png]]
Doing the Vuln Scan again through the created openvas4 via the yml file
![[Pasted image 20231202235355.png]]
![[Pasted image 20231203001025.png]]
