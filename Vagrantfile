# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.provider "virtualbox" do |vb|
    vb.memory = 1024
    vb.cpus = 1
  end
  config.vm.define "servidor1" do |servidor1|
    servidor1.vm.box = "centos/7"
    servidor1.vm.network "forwarded_port", guest: 80, host: 8095
    servidor1.vm.network "public_network", ip: "192.168.56.5", bridge: "wlp5s0"
    servidor1.vm.synced_folder "~/vm_shared_folder", "/vagrant", type: "virtualbox"
  end
  config.vm.define "servidor2" do |servidor2|
    servidor2.vm.box = "ubuntu/focal64"
    servidor2.vm.network "forwarded_port", guest: 80, host: 8080
    servidor2.vm.network "public_network", ip: "192.168.15.5", bridge: "wlp5s0"
    servidor2.vm.synced_folder "~/vm_shared_folder", "/vagrant", type: "virtualbox"
  end
  config.vm.define "servidor3" do |servidor3|
    servidor3.vm.box = "ubuntu/bionic64"
    servidor3.vm.network "forwarded_port", guest: 80, host: 8090
    servidor3.vm.network "public_network", ip: "192.168.15.6", bridge: "wlp5s0"
  end
  config.vm.define "servidor4" do |servidor4|
    servidor4.vm.box = "gusztavvargadr/windows-server"
    servidor4.vm.network "forwarded_port", guest: 80, host: 8070
    servidor4.vm.network "public_network", ip: "192.168.56.6", bridge: "wlp5s0"
  end
end
