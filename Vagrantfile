# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
    config.vm.box = "ubuntu/bionic64"
    config.vm.hostname = 'flaskex'
    config.vm.provider "virtualbox" do |v|
        v.customize [ "modifyvm", :id, "--uartmode1", "disconnected" ]
    end

    config.vm.provision "ansible" do |ansible|
        ansible.verbose = "v"
        ansible.playbook = "playbook.yml"
    end
    
  end