# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/bionic64"

  # provision
  config.vm.provision 'chef_solo' do |chef|
    chef.cookbooks_path = "berks-cookbooks"
    chef.add_recipe 'test_env_ami'
    # chef.nodes_path = 'nodes'
    chef.arguments = '--chef-license=accept'

    config.vm.synced_folder "./code", "/home/ubuntu/code"

  end
end
