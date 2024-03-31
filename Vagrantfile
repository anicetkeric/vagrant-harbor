playbook_file = 'ansible-harbor/playbook-harbor.yml'

Vagrant.configure("2") do |config|
    config.vm.box = "geerlingguy/centos7"
    config.vm.hostname = "registry.harbor.local"
    config.vm.network "private_network", ip: "192.168.56.11"

    config.vm.provider "virtualbox" do |vb|
      vb.cpus = 4
      vb.memory = 4096
    end 

    config.vm.provision "ansible_local" do |ansible|
      ansible.playbook = playbook_file
      ansible.verbose = true
    end
    
end
