Vagrant.configure("2") do |config|

#DOCKER_SERVER
  config.vm.define "dockerserver" do |dockerserver|
    dockerserver.vm.hostname = "dockerserver"
    dockerserver.vm.box = "ubuntu/bionic64"
    dockerserver.vm.network "private_network", ip: "192.168.99.2", dns: "8.8.8.8"

    config.vm.provider "virtualbox" do |dockerserver|
        dockerserver.memory = "3072"
    end

  end

end

