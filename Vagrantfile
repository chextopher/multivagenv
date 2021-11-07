Vagrant.configure("2") do |config|

     config.vm.define "webS" do |webS|
       webS.vm.box = "ubuntu/bionic64"
       webS.vm.hostname = "webS"
       webS.vm.network "private_network", ip: "192.168.10.88"
       webS.vm.network "public_network"
     config.vm.synced_folder ".", "/var/www/html"
     webS.vm.provider "virtualbox" do |vb|
         vb.memory = "1500"
         vb.name = "webS"
         vb.cpus = "2"
     end
     webS.vm.provision "shell", inline: <<-SHELL
         uptime
        SHELL
     end


    config.vm.define "dbS" do |dbS|
        dbS.vm.box = "ubuntu/bionic64"
        dbS.vm.hostname = "dbS"
        dbS.vm.network "private_network", ip: "192.168.10.89"
        dbS.vm.network "public_network"
    config.vm.synced_folder ".", "/var/www/html"
    dbS.vm.provider "virtualbox" do |vb|
          vb.memory = "1500"
          vb.name = "dbS"
          vb.cpus = "1"
      end
    dbS.vm.provision "shell", inline: <<-SHELL
          lscpu
         SHELL
      end
 

    config.vm.define "phpS" do |phpS|
        phpS.vm.box = "centos/7"
        phpS.vm.hostname = "phpS"
        phpS.vm.network "private_network", ip: "192.168.10.90"
        phpS.vm.network "public_network"
    config.vm.synced_folder ".", "/var/www/html"
    phpS.vm.provider "virtualbox" do |vb|
          vb.memory = "1024"
          vb.name = "phpS"
          vb.cpus = "1"
      end
    phpS.vm.provision "shell", inline: <<-SHELL
          cat /etc/*release
         SHELL
      end
 

    config.vm.define "lbS" do |lbS|
        lbS.vm.box = "source of the server "
        lbS.vm.hostname = "lbS"
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
 
