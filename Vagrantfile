# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  # For a complete reference of options, please see the online documentation 
  # at: https://docs.vagrantup.com

  config.vm.box = "centos/7"
  config.vm.network "forwarded_port", guest: 8153, host: 8153
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/ci-playbook.yml"
  end
end
