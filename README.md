Getting started with dockerizing Wordpress:
1. First step would be installing Docker and Docker-Compose on your System. You can install Docker in various ways, but I will share my installation in the command below:
- sudo apt update
- sudo apt install apt-transport-https ca-certificates curl software-properties-common
- curl -fsSL https://download.docker.com/linux/ubuntu/gpg | sudo apt-key add -
- sudo add-apt-repository "deb [arch=amd64] https://download.docker.com/linux/ubuntu focal stable"
- apt-cache policy docker-ce
- sudo apt install docker-ce
- sudo systemctl status docker

If it shows the status is active then Docker is running on your system, so you can start installing docker-compose with commands below:
- sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
- sudo chmod +x /usr/local/bin/docker-compose
- docker-compose --version

If you can see a version as an Output, then You're all set.

2. Second step is "Setiing up your docker-compose.yml" file
- mkdir wordpress-docker
- cd wordpress-docker
Create the docker-compose.yml file with any text editor you work always with, and copy paste the docker-compose file in this repository (Case-sensitive).

Then run the code below:
- docker-compose up -d

Hooray! You have done the job!
Test the result with openning a browser and searching for this address:
http://localhost:8080
