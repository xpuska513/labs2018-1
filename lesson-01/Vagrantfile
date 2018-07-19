Vagrant.configure("2") do |config|
  config.vm.provision "shell", inline: "echo Hello"

  config.vm.define "ubuntu" do |ubuntu|
      ubuntu.vm.box = "ubuntu/xenial64"
      ubuntu.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"

  config.vm.provider "virtualbox" do |vb| 
 		  vb.gui = false
  	  vb.memory = "1049"
  	 end

  end

  config.vm.define "centos" do |centos|
    centos.vm.box = "CentOS/7"
     centos.vm.network "forwarded_port", guest: 80, host: 3094, host_ip: "127.0.0.1"

    	 config.vm.provider "virtualbox" do |vb|
 	 			vb.gui = false
  	 			vb.memory = "1050"
  		 end
  end
end

