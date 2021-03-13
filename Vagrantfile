Vagrant.configure("2") do |config|

config.vm.define "das" do |subconfig|
ENV['LANG']=en_US.utf-8
ENV['LC_ALL']=en_US.utf-8
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "das"
subconfig.vm.network :private_network, ip: "192.168.1.10", :netmask => "255.255.255.0"
end

config.vm.define "me" do |subconfig|
ENV['LANG']=en_US.utf-8
ENV['LC_ALL']=en_US.utf-8
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "me"
subconfig.vm.network :private_network, ip: "192.168.1.11", :netmask => "255.255.255.0"
end

config.vm.define "pcs" do |subconfig|
ENV['LANG']=en_US.utf-8
ENV['LC_ALL']=en_US.utf-8
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "pcs"
subconfig.vm.network :private_network, ip: "192.168.1.12", :netmask => "255.255.255.0"
end

config.vm.define "se" do |subconfig|
ENV['LANG']=en_US.utf-8
ENV['LC_ALL']=en_US.utf-8
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "se"
subconfig.vm.network :private_network, ip: "192.168.1.13", :netmask => "255.255.255.0"
end

config.vm.define "sources" do |subconfig|
ENV['LANG']=en_US.utf-8
ENV['LC_ALL']=en_US.utf-8
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "sources"
subconfig.vm.network :private_network, ip: "192.168.1.14", :netmask => "255.255.255.0"
end

config.vm.define "xms" do |subconfig|
ENV['LANG']=en_US.utf-8
ENV['LC_ALL']=en_US.utf-8
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "xms"
subconfig.vm.network :private_network, ip: "192.168.1.15", :netmask => "255.255.255.0"
end

end
