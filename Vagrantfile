# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  # Ubuntu Box
  config.vm.box = "ubuntu/bionic64"

  # Hostname
  config.vm.hostname = "web01"

  # Private network disabled temporarily
  # because VirtualBox Host-Only adapter is broken
  # config.vm.network "private_network", ip: "192.168.56.10"

  # VirtualBox Settings
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "2048"
    vb.cpus = 2
  end

  # Install basic packages
  config.vm.provision "shell", inline: <<-SHELL
    sudo apt-get update -y
    sudo apt-get install -y vim wget unzip curl net-tools
  SHELL

end