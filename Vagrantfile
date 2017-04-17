# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
    config.vm.box = "bento/ubuntu-14.04"
    config.vm.network :private_network, ip: "192.168.74.32"

    config.vm.provider "virtualbox" do |vb|
        vb.name = "vim_test_env"
        vb.memory = 1024
        vb.cpus = 2
    end

    # Sync global gitconfig file from host machine.
    config.vm.synced_folder "~/.gitconfig", desitination: ".gitconfig"

    # Provision tools.
    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "provisioning/main.yml"
    end
end
