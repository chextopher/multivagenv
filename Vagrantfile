Vagrant.configure("2") do |config|

     config.vm.define "webS" do |webS|
       webS.vm.box = "choose source of server from vagrant cloud"
       webS.vm.hostname = "input hostName"
       webS.vm.network "private_network", ip: "input your ip address"
       webS.vm.network "public_network"
     config.vm.synced_folder ".", "/var/www/html"
     webS.vm.provider "virtualbox" do |vb|
         vb.memory = "mem size"
         vb.name = "name of vb"
         vb.cpus = "# of cpus"
     end
     webS.vm.provision "shell", inline: <<-SHELL
         run your commands
        SHELL
     end


    config.vm.define "dbS" do |dbS|
        dbS.vm.box = "choose source of server from vagarnt cloud"
        dbS.vm.hostname = "input hostName"
        dbS.vm.network "private_network", ip: "input your ip address"
        dbS.vm.network "public_network"
    config.vm.synced_folder ".", "/var/www/html"
    dbS.vm.provider "virtualbox" do |vb|
          vb.memory = "mem size"
          vb.name = "name of vb"
          vb.cpus = "# of cpus"
      end
    dbS.vm.provision "shell", inline: <<-SHELL
          run your commands
         SHELL
      end
 

    config.vm.define "phpS" do |phpS|
        phpS.vm.box = "choose source of server from vagarnt cloud"
        phpS.vm.hostname = "input hostName"
        phpS.vm.network "private_network", ip: "input your ip address"
        phpS.vm.network "public_network"
    config.vm.synced_folder ".", "/var/www/html"
    phpS.vm.provider "virtualbox" do |vb|
          vb.memory = "mem size"
          vb.name = "name of vb"
          vb.cpus = "# of cpus"
      end
    phpS.vm.provision "shell", inline: <<-SHELL
          run your commands
         SHELL
      end
 

    config.vm.define "lbS" do |lbS|
        lbS.vm.box = "source of the server from vagrant cloud"
        lbS.vm.hostname = "input hostName"
        lbS.vm.network "private_network", ip: "input your ip"
        lbS.vm.network "public_network"
    config.vm.synced_folder ".", "/var/www/html"
    lbS.vm.provider "virtualbox" do |vb|
          vb.memory = "input your mem size"
          vb.name = "input name of vb(lbS)"
          vb.cpus = "input size of cpu"
      end
    config.vm.provision "shell" , path: "script.sh"
    end
end
 
