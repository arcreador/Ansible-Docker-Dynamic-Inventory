# Ansible-Docker-Dynamic-Inventory
Dynamically updating the IP of docker container which is running on manage node 
I have used  my custimize os image which is available on my docker-hub account https://hub.docker.com/r/arcreador/myweb
In that image i have configured the openssh-sever ,openssh-clients
You can also set the your os image 

#follow these step to setup docker image for ssh

step 1: yum install openssh-sever
step 2: yum install openssh-clients
step 3: ssh-keygen -A
step 4: /usr/sbin/sshd  -D -e "$@"
step 5: press Ctr+p+q for exit
step 6: docker exec -it <containerNmae> bash
step 7: yum install passwd
step 8: passwd root (set new password for root inside container)
step 9: exit
step 10: docker commit <ConatinerName> <NameImageYouWantToSet>
step 11: docker tag <imageName> <dockerHubAccountName>/<NameOfImageany>:<version>
step 12: docker login
step 13: docker push <ImageNAme>
