# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  # For a complete reference of options, please see the online documentation 
  # at: https://docs.vagrantup.com

  # Base box for virtual machine will be CentOS 7
  config.vm.box = "centos/7"

  # GoCD's default http port is 8153, let's use the same port in the host.
  # Thus all http requests on localhost:8153 will be redirect to the VM on 
  # the same port.
  config.vm.network "forwarded_port", guest: 8153, host: 8153

  # We'll do provisioning with Ansible (needs to be installed on host)
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/ci-playbook.yml"
  end
end
