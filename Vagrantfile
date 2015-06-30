# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = 2

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "ubuntu/trusty32"
  config.vm.box_check_update = true

  config.ssh.forward_agent = true

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/vde.yml"
  end
end
