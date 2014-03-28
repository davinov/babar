# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

PROJECT_NAME    = "babar"
BOX_NAME        = "hashicorp/precise64"

VM_CPUCAP          = "100"
VM_CPUS            = 2
VM_MEMORY          = 2048
VM_PRIVATE_NETWORK = "199.199.199.87"

Vagrant.configure("2") do |config|
  config.vm.define PROJECT_NAME do |config|
    config.vm.box      = BOX_NAME

    config.vm.hostname = PROJECT_NAME
    config.vm.network :private_network, ip: VM_PRIVATE_NETWORK
    config.vm.network "public_network"

    config.vm.provider "virtualbox" do |v|
      v.customize ["modifyvm", :id, "--cpuexecutioncap", VM_CPUCAP]
      v.customize ["modifyvm", :id, "--memory",          VM_MEMORY]
      v.customize ["modifyvm", :id, "--cpus",            VM_CPUS]
      v.name = PROJECT_NAME
    end

    config.ssh.forward_agent = true

    config.vm.synced_folder "api/", "/var/www/"+PROJECT_NAME+"-api/current", id: "api", type: "nfs"
    config.vm.synced_folder "frontend/", "/var/www/"+PROJECT_NAME+"-frontend/current", id: "frontend", type: "nfs"

  end
end
