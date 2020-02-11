# -*- mode: ruby -*-
# vi: set ft=ruby :

# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure("2") do |config|

  config.vm.define :master do |mast|
   mast.vm.provision "shell", path: "script.sh"
   mast.vm.box = "ubuntu/bionic64" 
   mast.vm.network :private_network, ip: "10.0.15.40"
   mast.vm.hostname = "master"
   mast.vm.provider "virtualbox" do |vb|
          vb.memory = "512"
        end
  end

  config.vm.define :slave1 do |slav|
   slav.vm.box = "ubuntu/bionic64" 
   slav.vm.provision "shell", path: "script.sh" 
   slav.vm.network :private_network, ip: "10.0.15.41"
   slav.vm.hostname = "slave1"
   slav.vm.provider "virtualbox" do |vb|
          vb.memory = "512"
        end
  end
  
 config.vm.define :slave2 do |slav|
   slav.vm.box = "ubuntu/bionic64" 
   slav.vm.provision "shell", path: "script.sh"
   slav.vm.network :private_network, ip: "10.0.15.42"
   slav.vm.hostname = "slave2"
   slav.vm.provider "virtualbox" do |vb|
          vb.memory = "512"
        end
  end

  config.vm.define :slave3 do |mast|

   mast.vm.box = "ubuntu/bionic64" 
   mast.vm.provision "shell", path: "script.sh"
   mast.vm.network :private_network, ip: "10.0.15.43"
   mast.vm.hostname = "slave3"
   mast.vm.provider "virtualbox" do |vb|
          vb.memory = "512"
        end
  end

end
