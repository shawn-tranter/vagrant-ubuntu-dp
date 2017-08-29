# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"

  # add docker, python, pip
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update

    apt-get -y install docker.io
    usermod -aG docker ubuntu

    apt-get -y install python
    apt-get -y install python-pip

    pip install --upgrade pip
    pip install docker-py

    service docker start
  SHELL
end
