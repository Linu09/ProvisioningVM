ENV["LC_ALL"] = "en_US.UTF-8"

Vagrant.configure("2") do |config|

config.vm.define "vm01" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "vm01"
subconfig.vm.network :private_network, ip: "192.168.1.10", :netmask => "255.255.255.0"
end

config.vm.define "vm02" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "vm02"
subconfig.vm.network :private_network, ip: "192.168.1.11", :netmask => "255.255.255.0"
end

config.vm.define "vm03" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "vm03"
subconfig.vm.network :private_network, ip: "192.168.1.12", :netmask => "255.255.255.0"
end

config.vm.define "vm04" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "vm04"
subconfig.vm.network :private_network, ip: "192.168.1.13", :netmask => "255.255.255.0"
end

config.vm.define "vm05" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "vm05"
subconfig.vm.network :private_network, ip: "192.168.1.14", :netmask => "255.255.255.0"
end

config.vm.define "vm06" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "vm06"
subconfig.vm.network :private_network, ip: "192.168.1.15", :netmask => "255.255.255.0"
end

end
