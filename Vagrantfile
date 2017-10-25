Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/xenial64"
  config.vm.network "forwarded_port", guest: 8888, host: 8888, host_ip: "127.0.0.1", id: 'ipyton-notebook-port'

  if Vagrant.has_plugin?("vagrant-vbguest") then
    config.vbguest.auto_update = false
  end
  config.vm.provider "virtualbox" do |vb|
   vb.memory = "2048"
   vb.cpus = 2
  end

  config.vm.hostname = "lstm-vm"
  config.vm.provision "shell", path: "setup.sh"   
end