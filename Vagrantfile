# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = 2

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty32"
  config.vm.box_check_update = true

  config.vm.network :private_network, ip: "10.0.3.101"
  config.vm.synced_folder ".", "/vagrant", nfs: true

  config.ssh.forward_agent = true

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/vde.yml"
  end
end
