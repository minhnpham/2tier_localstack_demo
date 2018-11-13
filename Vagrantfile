Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  # Customise VM configuration
  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", "2048"]
  end

  # Executes the Ansible playbook to provision the entire tech stack
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook = "ansible_plays/site.yml"
  end

  # Port forward guest VM ports to local host ports
  config.vm.network "forwarded_port", guest: 80, host: 80
  config.vm.network "forwarded_port", guest: 8080, host: 8080

end