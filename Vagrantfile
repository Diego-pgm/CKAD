# -*- mode: ruby -*-
# vi: set ft=ruby :


Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 2
  end
  config.vm.box_download_insecure = true
  config.vm.define "control" do |control|
    control.vm.box = "bento/ubuntu-20.04"
    control.vm.hostname = "control"
    control.vm.network "private_network", ip: "192.168.56.2"
    control.vm.network "public_network"
  end

  config.vm.define "worker1" do |worker1|
    worker1.vm.box = "bento/ubuntu-20.04"
    worker1.vm.hostname = "worker1"
    worker1.vm.network "private_network", ip: "192.168.56.3"
    worker1.vm.network "public_network"
  end

  config.vm.define "worker2" do |worker2|
    worker2.vm.box = "bento/ubuntu-20.04"
    worker2.vm.hostname = "worker2"
    worker2.vm.network "private_network", ip: "192.168.56.4"
    worker2.vm.network "public_network"
  end

end
