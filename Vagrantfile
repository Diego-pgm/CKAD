# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 4086
    v.cpus = 4
  end
  config.vm.box_download_insecure = true
  config.vm.define "control" do |control|
    control.vm.box = "bento/ubuntu-20.04"
    control.vm.hostname = "control"
    control.vm.network "private_network", ip: "10.0.0.2"
    control.vm.network "public_network"
  end

  config.vm.define "worker1" do |worker1|
    worker1.vm.box = "bento/ubuntu-20.04"
    worker1.vm.hostname = "worker1"
    worker1.vm.network "private_network", ip: "10.0.0.3"
    worker1.vm.network "public_network"
  end

  config.vm.define "worker2" do |worker2|
    worker2.vm.box = "bento/ubuntu-20.04"
    worker2.vm.hostname = "worker2"
    worker2.vm.network "private_network", ip: "10.0.0.4"
    worker2.vm.network "public_network"
  end

  config.vm.define "docker" do |docker|
    docker.vm.box = "bento/ubuntu-20.04"
    docker.vm.hostname = "docker-server"
    docker.vm.network "private_network", ip: "10.0.0.5"
    docker.vm.network "public_network"
  end

end
