# -*- mode: ruby -*-
# vi: set ft=ruby :

# It is recommended to upgrade instead of disabling the requirement below.
Vagrant.require_version ">= 1.7.0"

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "bento/ubuntu-14.04"
    config.vm.network :private_network, ip: "192.168.74.32"
    config.ssh.insert_key = false

    config.vm.provider "virtualbox" do |vb|
        vb.name = "vim"
        vb.memory = 1024
        vb.cpus = 2
    end

    # Sync global gitconfig file from host machine.
    config.vm.synced_folder "~/.gitconfig", desitination: ".gitconfig"

    # Provision tools.
    config.vm.provision "ansible" do |ansible|
        ansible.verbose = "v"
        ansible.playbook = "provisioning/main.yml"
    end
end
