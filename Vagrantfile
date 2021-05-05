# -*- mode: ruby -*-
# vi: set ft=ruby :

VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "bento/ubuntu-20.10"
  
  # Provision
  config.vm.provision :shell, :path => "install.sh"

  # Pour accéder à la VM depuis l'hote
  config.vm.network :forwarded_port, guest: 5000, host: 5000

  # Shared folder
  config.vm.synced_folder "vagrant/", "/home/vagrant", create: true

  #config.vm.provider :libvirt do |p|
  #  p.management_network_name = 'vagrant-libvirt-new'
  #  p.management_network_address = '192.168.124.0/24'
  #end
  
end