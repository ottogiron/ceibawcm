# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # All Vagrant configuration is done here. The most common configuration
  # options are documented and commented below. For a complete reference,
  # please see the online documentation at vagrantup.com.
  config.vm.network "forwarded_port", guest: 8090, host: 8090
  config.vm.network "forwarded_port", guest: 9100, host: 9100

  # Every Vagrant virtual environment requires a box to build off of.
  config.vm.box = "ubuntu-modeshape-wildfly"

  config.vm.provider "virtualbox" do |v|
    v.memory = 1024
    v.cpus = 2
  end

  config.vm.synced_folder ".", "/home/vagrant/modeshape-rest-client"
  config.vm.hostname = "modeshape.dev"

  #Provisioning
  #config.vm.provision :shell, :inline => "sudo apt-get update"

  # config.vm.provision "puppet" do |puppet|
  #   puppet.manifests_path = "puppet/manifests"
  #   puppet.manifest_file = "site.pp"
  #   puppet.module_path = "puppet/modules"
  # end



end
