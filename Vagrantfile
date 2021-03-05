Vagrant.configure("2") do |box|
  box.vm.box = "generic/ubuntu2004"
  box.vm.network "private_network", ip: "192.168.111.111"
  box.vm.provision "shell", inline: <<-SHELL
	      apt-get install python3
  	  SHELL
  end

