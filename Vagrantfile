# -*- mode: ruby -*-
# vi: set ft=ruby :
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "dreamscapes/archlinux"
  config.vm.provision "shell", inline: "pacman -S --noconfirm python2", privileged: true
end
