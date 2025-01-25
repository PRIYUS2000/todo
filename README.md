# Todo application

git clone https://github.com/PRIYUS2000/to-do.git 

# Install docker

sudo apt-get update

sudo apt-get install ca-certificates curl

sudo install –m 0755 –d /etc/apt/keyrings

sudo curl -fsSL https://download.docker.com/linux/ubuntu/gpg -o /etc/apt/keyrings/docker.asc

sudo chmod a+r /etc/apt/keyrings/docker.asc

# Add the repository to Apt sources:

echo \ "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.asc] https://download.docker.com/linux/ubuntu \
  $(. /etc/os-release && echo "$VERSION_CODENAME") stable" | \ sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
sudo apt-get update

# Install the Docker package,check version & status

sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin


# Navigate the folder

cd to-do 

cd bitphile-todo-app-docker-compose

# Install dependencies in each of those directories

cd frontend 

sudo apt install npm 

cd backend 

sudo apt install npm

# Steps to Install Docker Compose

sudo apt-get update 

sudo apt-get install -y curl jq 

VERSION=$(curl -s https://api.github.com/repos/docker/compose/releases/latest | jq -r .tag_name) 

sudo curl -L "https://github.com/docker/compose/releases/download/$VERSION/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose 

sudo chmod +x /usr/local/bin/docker-compose

# Checking docker compose version

docker-compose --version

# Access your application

http://ec2-public ip:4000 ex: http://13.232.84.207:4000/

# To stop the Docker containers

sudo docker-compose down
