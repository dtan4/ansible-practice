# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.box = "opscode-ubuntu-14.04"
  config.vm.network "private_network", ip: "192.168.111.222"

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "vagrant.yml"
    ansible.inventory_path = "hosts"
    ansible.limit = "all"
  end
end
