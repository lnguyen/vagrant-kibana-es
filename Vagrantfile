# -*- mode: ruby -*-
# vi: set ft=ruby :

# Vagrantfile API/syntax version. Don't touch unless you know what you're doing!
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "centos65"

  config.vm.define "es", primary: true do |v|
    v.vm.network "private_network", ip: "192.168.69.100"
    v.vm.hostname = "es"
    v.vm.provision "shell" do |sh|
      sh.path = "bin/es"
    end
  end

  config.vm.define "kibana", primary: true do |v|
    v.vm.network "private_network", ip: "192.168.69.101"
    v.vm.hostname = "kibana"
    v.vm.provision "shell" do |sh|
      sh.path = "bin/kibana"
    end
  end
end
