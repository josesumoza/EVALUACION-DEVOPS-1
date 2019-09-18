Vagrant.configure("2") do |config|
    config.vm.box = "bento/ubuntu-16.04"
    #config.vm.box = "geerlingguy/ubuntu1804"
    config.vm.network "forwarded_port", guest: 80, host: 8080
    config.vm.network :private_network, ip: "10.10.10.10"
     # Configuración de VirtualBox
     config.vm.provider :virtualbox do |vb|
        # Nombre de la máquina virtual
        vb.name = 'EVALUACION-TEST1'
        # Memoria
        vb.memory = 2048
        # Número de procesadores
        vb.cpus = 2
    end
    ####### Provision #######
    config.vm.provision "ansible_local" do |ansible|
      ansible.playbook = "ansible/playbook.yml"
      ansible.verbose = true
    end
  end