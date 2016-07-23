# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure("2") do |config|
  config.vm.box      = "ubuntu/trusty64"
  config.vm.hostname = "vPostgreSQL"
  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.provider :virtualbox do |vb|
    vb.name   = "vPostgreSQL"
    vb.cpus   = 2
    vb.memory = 1024
    vb.customize ["modifyvm", :id, "--ioapic", "on"]
  end  

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
    #ansible.verbose  = "v"
  end
end
