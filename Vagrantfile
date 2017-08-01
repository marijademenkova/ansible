Vagrant.configure("2") do |config|
  config.vm.box = "sbeliakou-centos-7.3-x86_64-minimal.box"
  config.vm.network "private_network", ip: "192.168.56.60"
  config.vm.network "forwarded_port", guest: 8080, host: 8080
  config.vm.hostname = "vagrantvm"
  config.vm.provider "virtualbox" do |vb|
    vb = config.vm.hostname
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = 'tomcat_provision.yml'
    ansible.verbose = 'vv'
  end
end
end
