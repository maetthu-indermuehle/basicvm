# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|

  config.vm.hostname = 'basicvm.vagrant.maetthu.com'
  config.vm.box = 'puppetlabs/ubuntu-14.04-64-puppet'
  vm_memory = 2048
  vm_cores = 2

  # export gpg key from host
  # system('gpg --export-secret-keys -a > gpgkey.asc') unless File.exist?('gpgkey.asc')
  # import gpg key in vm
  # config.vm.provision :shell, inline: 'if [ -f /vagrant/gpgkey.asc ]; then gpg --import /vagrant/gpgkey.asc; fi'

  # install basic build packages
  #  config.vm.provision "puppet"

  config.vm.provider :virtualbox do |vb|
    vb.gui  = false
    vb.name = 'Ansible Controler - maetthu'
    vb.customize ['modifyvm', :id, '--memory', vm_memory]
    vb.customize ['modifyvm', :id, '--ioapic', 'on']
    vb.customize ['modifyvm', :id, '--cpus', vm_cores]
  end

end
