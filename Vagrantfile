ENV["LC_ALL"] = "en_US.UTF-8"
Vagrant.configure(2) do |config|

  config.vm.box = "centos/7"

  config.vm.define "master" do |master|
    master.vm.hostname = "master"
    master.vm.network "private_network", ip: "192.168.1.10", :netmask => "255.255.255.0"
	config.disksize.size = '80GB'
	config.vm.provider :virtualbox do |vb|
       vb.memory = 2048
       vb.cpus = 1
    end  
    master.vm.provision "shell", inline: <<-SHELL
		useradd -mr bmg
		useradd -g users -G wheel,root bmg
		yum update -y
		yum install epel-release -y
		yum install ansible -y
	SHELL
  end
 
  config.vm.define "das" do |m|
    m.vm.hostname = "das-server"
    m.vm.network "private_network", ip: "192.168.1.11", :netmask => "255.255.255.0"
	config.disksize.size = '80GB'
    config.vm.provider :virtualbox do |vb|
       vb.memory = 2048
       vb.cpus = 1
    end  
    m.vm.provision "shell", inline: $script
  end

  config.vm.define "xms" do |m|
    m.vm.hostname = "xms-server"
    m.vm.network "private_network", ip: "192.168.1.12", :netmask => "255.255.255.0"
	config.disksize.size = '80GB'
    config.vm.provider :virtualbox do |vb|
       vb.memory = 2048
       vb.cpus = 1
    end  
    m.vm.provision "shell", inline: $script
  end  

  config.vm.define "me" do |m|
    m.vm.hostname = "me-server"
    m.vm.network "private_network", ip: "192.168.1.13", :netmask => "255.255.255.0"
	config.disksize.size = '80G'   
    config.vm.provider :virtualbox do |vb|
       vb.memory = 2048
       vb.cpus = 1
    end  
    m.vm.provision "shell", inline: $script
  end
  
  config.vm.define "se" do |m|
    m.vm.hostname = "se-server"
    m.vm.network "private_network", ip: "192.168.1.14", :netmask => "255.255.255.0"
	config.disksize.size = '80GB'
    config.vm.provider :virtualbox do |vb|
       vb.memory = 2048
       vb.cpus = 1
    end  
    m.vm.network "forwarded_port", guest: 7001, host: 7001
    m.vm.provision "shell", inline: $script
  end
  
  config.vm.define "pcs" do |m|
    m.vm.hostname = "pcs-server"
    m.vm.network "private_network", ip: "192.168.1.15", :netmask => "255.255.255.0"
	config.disksize.size = '80GB'
    config.vm.provider :virtualbox do |vb|
       vb.memory = 2048
       vb.cpus = 1
    end  
    m.vm.provision "shell", inline: $script
  end
  
$script = <<SCRIPT

echo $HOSTNAME "Created Succesfully ..."

useradd -mr bmg
useradd -g users -G wheel,root bmg
yum update -y
sudo cp /vagrant/hosts /etc/hosts

SCRIPT

end
