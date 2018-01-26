# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box_check_update = false
  config.hostmanager.enabled = true
  config.hostmanager.manage_host = true
  config.hostmanager.manage_guest = true
  config.hostmanager.ignore_private_ip = false
  config.vm.box = "archlinux/archlinux"
  config.vm.hostname = 'dev'
  config.vm.network "private_network", type: "dhcp"
  config.hostmanager.ip_resolver = proc do |vm, resolving_vm|
    `vagrant ssh -c "ip addr show eth1 | grep -oP 'inet \K\S[0-9.]+'"`
  end
  config.vm.synced_folder "~/work", "/work"
  config.vm.synced_folder "~/dotfiles", "/dotfiles"
end
