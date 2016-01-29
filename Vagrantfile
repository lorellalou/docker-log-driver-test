# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.vm.define "dev" do |dev|
    dev.vm.box = "ubuntu/trusty64"
  	dev.vm.synced_folder ".", "/data/docker/compose/test"
  	dev.vm.provider "virtualbox" do |v|
      v.memory = 4096
  	end
  	dev.vm.network "private_network", ip: "192.168.50.33"
	# Provision the machine with Docker
    dev.vm.provision :docker
    dev.vm.provision :docker_compose
  end

 
end
