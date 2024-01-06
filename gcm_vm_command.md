**please give me gcloud command to create ubuntu vm wiht tags allow-mysql-fw and startup script to create mysql using dokcer with root password as root123 and port 3306**

gcloud compute instances create mysql-instance \
    --image-family=ubuntu-2004-lts \
    --image-project=ubuntu-os-cloud \
    --zone=us-central1-a \
    --tags=allow-mysql-fw \
    --metadata=startup-script='#! /bin/bash
sudo apt-get update
sudo apt-get -y install docker.io
sudo docker run -d --name=mysql-server -e MYSQL_ROOT_PASSWORD=root123 -p 3306:3306 mysql:latest'
