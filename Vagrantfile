# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.define :test_vm do |test_vm|
  test_vm.vm.box = "alvistack/ubuntu-20.04"
    test_vm.vm.provider :libvirt do |domain|
      domain.memory = 2048
      domain.cpus = 2
    end

    test_vm.vm.network :private_network, :ip => '192.168.122.132'
  end


  config.vm.provider :libvirt do |libvirt|

    libvirt.driver = "kvm"
    libvirt.connect_via_ssh = false

    libvirt.username = "root"
    #libvirt.password = "secret"

    libvirt.storage_pool_name = "default"

  end
end
