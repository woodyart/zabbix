VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|

  config.ssh.insert_key = false

  config.vm.box      = "ubuntu/bionic64"
  config.vm.hostname = "monitoring"
  config.vm.network "forwarded_port", guest: 80, host: 8999

  config.vm.provider :virtualbox do |v|
    v.memory = 1024
    v.cpus   = 2
  end

  config.vm.provision "ansible" do |ansible|
    ansible.compatibility_mode = "2.0"
#    ansible.verbose = "vv+" # Enable debug
    ansible.playbook = "ansible/playbook.yml"
    ansible.inventory_path = "ansible/inventory"
    ansible.become = true
  end

end
