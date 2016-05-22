# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.ssh.forward_agent = true
  if Vagrant.has_plugin?("vagrant-cachier")
    config.cache.scope = :box
  end
  config.vm.provider :virtualbox do |vb|
    vb.customize ["modifyvm", :id, "--memory", "6144"]
    vb.customize ["modifyvm", :id, "--cpus", "2"]   
  end  
  config.vm.provision "shell", inline: <<-SHELL
    /vagrant/provision
  SHELL
end
