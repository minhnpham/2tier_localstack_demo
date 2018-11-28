Vagrant.configure("2") do |config|
  config.vm.box = "centos/7"

  # Customise VM configuration
  config.vm.provider "virtualbox" do |v|
    v.customize ["modifyvm", :id, "--memory", "2048"]
  end

  # Executes the Ansible playbook to provision the entire tech stack
  config.vm.provision "ansible_local", run: "always" do |ansible|
    ansible.playbook = "ansible_plays/site.yml"    
  end

  # Port forward guest VM ports to local host ports
  config.vm.network "forwarded_port", guest: 3000, host: 3000
  config.vm.network "forwarded_port", guest: 3000, host: 8080

end