#!/bin/bash

sudo apt-get update
sudo apt-get -y install unzip

#Install latest docker
curl -sSL https://get.docker.com/ | sh
sudo usermod -aG docker ubuntu

#Install consul
cd /usr/local/bin
sudo wget https://dl.bintray.com/mitchellh/consul/0.5.2_linux_amd64.zip
sudo unzip *.zip
sudo rm *.zip
sudo adduser consul
sudo mkdir -p /etc/consul.d/{bootstrap,server,client}
sudo mkdir /var/consul
sudo chown consul:consul /var/consul
