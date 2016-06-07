# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"
  # config.vm.box = "debian/jessie64"
  # config.vm.box = "ubuntu/trusty32"
  # config.vm.box = "ubuntu/trusty64"

  # config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.synced_folder ".", "/home/vagrant/sync", disabled: true
  config.vm.synced_folder ".", "/vagrant", disabled: true

  config.vm.provider "virtualbox" do |vb|
    # Display the VirtualBox GUI when booting the machine
    # vb.gui = true

    # Customize the amount of memory on the VM:
    vb.memory = "1024"
  end

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "deploy.yml"
  end
end
