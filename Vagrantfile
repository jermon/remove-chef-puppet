# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure('2') do |config|

  config.vm.define 'test' do |machine|
    machine.vm.box = "ubuntu/trusty64"

    machine.vm.network :private_network, ip: '192.168.33.10'
    machine.vm.hostname = 'test.local'
    machine.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'tests/test.yml'
      ansible.sudo = true
      #ansible.inventory_path = 'vagrant-inventory'
      #ansible.host_key_checking = false
    end
  end
end
