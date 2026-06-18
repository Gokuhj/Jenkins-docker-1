# Jenkins-docker-1
Connect to EC-2 
ssh -i your-key.pem ubuntu@<your-ip>

Install java

sudo apt update
sudo apt install openjdk-21-jdk -y

Install git

sudo apt install git -y

Install docker

sudo apt install docker.io -y
sudo systemctl start docker
sudo systemctl enable docker

Give Docker access 

sudo usermod -aG docker ubuntu
newgrp docker
verify - docker ps

Install jenkins .WAR file

wget https://get.jenkins.io/war-stable/latest/jenkins.war
sudo java -jar jenkins.war

Get jenkins password
sudo cat /root/.jenkins/secrets/initialAdminPassword

Open jenkins
http://<your-ip>:8080
