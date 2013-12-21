# -*- mode: ruby -*-
# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = ["http://files.vagrantup.com/precise64.box", "http://files.vagrantup.com/precise64_vmware_fusion.box"]

  config.vm.provision :shell, inline: <<-SCRIPT
    apt-get update
    apt-get -y install python-software-properties
    add-apt-repository -y ppa:staticfloat/juliareleases
    add-apt-repository -y ppa:staticfloat/julia-deps
    apt-get update
    apt-get -y install julia
  SCRIPT
end
