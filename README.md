# vagrant-ci-jenkins
Vagrant and Ansible setup to spin up a VM with Jenkins up and running

## Pre-requisites

- virtualbox or another provider
- vagrant
- ansible (v2.2 or higher, check with "ansible --version")
- vagrant box Ubuntu 14.04 - vagrant box add ubuntu/trusty64

## Usage

### Start new VM

copy Vagrantfile
vagrant up

check Jenkins is running: sudo service jenkins status
localhost:8080

unlock jenkins
<image>
vagrant ssh
sudo cat /var/lib/jenkins/secrets/initialAdminPassword


roughly half a minute for GoCD to be up and running


### Update running VM

vagrant provision

### Tests

## Virtual Machine Environment

### OS

VM ubuntu 14.04 LTS

#### Change OS


### Jenkins

#### Example pipeline

## Troubleshooting

### Port conflicts

## ToDo

- security setup
- scale agents / tune resources
- granular tests