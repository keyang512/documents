#!/bin/bash

sudo apt-get update
sudo apt-get -y install unzip

#Install latest docker
curl -sSL https://get.docker.com/ | sh
sudo usermod -aG docker ubuntu
