BOX_IMAGE = "bento/ubuntu-18.04"

Vagrant.configure("2") do |config|
  config.vm.define "webserver" do |subconfig|
    subconfig.vm.box = BOX_IMAGE
    subconfig.vbguest.auto_update = false
    subconfig.vm.hostname = "webserver"
    subconfig.vm.network :"public_network", bridge: 'en0: Wi-Fi (AirPort)'
    config.vm.provision :shell, path: "bootstrap.sh"
  end

  config.vm.define "db1" do |subconfig|
    subconfig.vm.box = BOX_IMAGE
    subconfig.vbguest.auto_update = false
    subconfig.vm.hostname = "db1"
    subconfig.vm.network :"public_network", bridge: 'en0: Wi-Fi (AirPort)'
    config.vm.provision :shell, path: "bootstrap.sh"
  end

  config.vm.define "db2" do |subconfig|
    subconfig.vm.box = BOX_IMAGE
    subconfig.vbguest.auto_update = false
    subconfig.vm.hostname = "db2"
    subconfig.vm.network :"public_network", bridge: 'en0: Wi-Fi (AirPort)'
    config.vm.provision :shell, path: "bootstrap.sh"
  end
  VAGRANT_DISABLE_VBOXSYMLINKCREATE=1

end
