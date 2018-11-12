Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  # Customise VM configuration
  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", "2048"]
  end

  # Port forward guest VM ports to local host ports
  config.vm.network "forwarded_port", guest: 80, host: 80
  config.vm.network "forwarded_port", guest: 8080, host: 8080

end