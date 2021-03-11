Vagrant.configure("2") do |config|

config.vm.define "das" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "das"
subconfig.vm.network :private_network, ip: "10.0.0.10"
end

config.vm.define "mediaengine" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "mediaengine"
subconfig.vm.network :private_network, ip: "10.0.0.11"
end

config.vm.define "pcs" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "pcs"
subconfig.vm.network :private_network, ip: "10.0.0.12"
end

config.vm.define "signalingengine" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "signalingengine"
subconfig.vm.network :private_network, ip: "10.0.0.13"
end

config.vm.define "sources" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "sources"
subconfig.vm.network :private_network, ip: "10.0.0.14"
end

config.vm.define "xms" do |subconfig|
subconfig.vm.box = "centos/7"
subconfig.vm.hostname = "xms"
subconfig.vm.network :private_network, ip: "10.0.0.15"
end


end
