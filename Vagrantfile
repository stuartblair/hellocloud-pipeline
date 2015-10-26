# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "concourse/lite"
  config.vm.provision "shell", inline: "echo "" > /etc/resolvconf/resolv.conf.d/head; resolvconf -u"
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--natdnshostresolver1", "on"]
  end
end
