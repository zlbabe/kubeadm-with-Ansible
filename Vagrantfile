# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.synced_folder ".", "/vagrant", disabled: true
  config.vm.provider "virtualbox" do |vb|
    vb.gui = false
    vb.memory = "512"
  end
  
  config.vm.define "master" do |master|
  	master.vm.hostname = "master"
  	master.vm.network "private_network", ip: "10.0.0.100"
        master.vm.provider "virtualbox" do |vb|
                vb.customize ["modifyvm", :id, "--memory", "1024"]
        end
  end

  config.vm.define "worker1" do |worker1|
  	worker1.vm.hostname = "worker1"
  	worker1.vm.network "private_network", ip: "10.0.0.101"
  end

  config.vm.define "worker2" do |worker2|
  	worker2.vm.hostname = "worker2"
  	worker2.vm.network "private_network", ip: "10.0.0.102"
  end
  
  config.vm.provision "file", source: "~/.ssh/id_rsa.pub", destination: "/home/vagrant/.ssh/authorized_keys"

end
