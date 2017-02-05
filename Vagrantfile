# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = "2"

VM_NAME = "guild_demo"
MEMORY_SIZE_MB = 1024
NUMBER_OF_CPUS = 2

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/xenial64"

  config.vm.define "guild_box" do |guild_box|
    guild_box.vm.provider "virtualbox" do |v|
      v.name = VM_NAME
      v.customize ["modifyvm", :id, "--memory", MEMORY_SIZE_MB]
      v.customize ["modifyvm", :id, "--cpus", NUMBER_OF_CPUS]
    end
    guild_box.vm.network :private_network, ip: "192.168.55.55"
    guild_box.vm.network :forwarded_port, guest: 5432, host: 45432
    guild_box.vm.network :forwarded_port, guest: 6333, host: 6333
    guild_box.vm.network :forwarded_port, guest: 6444, host: 6444
    guild_box.vm.provision :shell, :path => "vagrant_provision.sh"
  end
end
