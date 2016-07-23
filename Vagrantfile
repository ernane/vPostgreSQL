# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box      = "ubuntu/trusty64"
  config.vm.hostname = "vPostgreSQL"
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provider "virtualbox" do |vb|
    vb.customize [ "modifyvm", :id, "--name", "vPostgreSQL", "--memory", 1024]
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  #  ansible.verbose = "vvv"
  end
end
