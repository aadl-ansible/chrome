# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.define "chrome-test"
  config.vm.hostname = "chrome-test"
  config.vm.provider "virtualbox" do |vb|
     # Display the VirtualBox GUI when booting the machine
     vb.gui = true
     vb.name = "chrome-test-box"
  end
  config.vm.network "private_network", ip: "192.168.10.10"
  config.vm.provision "shell", inline: <<-SHELL
    echo -e "testingpass\ntestingpass" | passwd ubuntu
  SHELL
end
