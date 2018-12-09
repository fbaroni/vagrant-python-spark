# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.define "ubuntu-python-spark" do |srv|

    srv.vm.box = "bento/ubuntu-18.04"

    srv.vm.hostname = "python-spark"
    srv.vm.network "private_network", ip: "192.168.37.14"
    
    srv.vm.provider "virtualbox" do |vb|
      vb.memory = "2048"
    end

    srv.vm.provision "ansible" do |ansible|
      ansible.playbook = "provision/playbook.yml"
    end
  end
end
