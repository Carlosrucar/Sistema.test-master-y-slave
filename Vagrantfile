Vagrant.configure("2") do |config|
  
  # Configuración de máquina Venus (Debian texto)
  config.vm.define "venus" do |venus|
    venus.vm.box = "debian/bullseye64"
    venus.vm.hostname = "venus.sistema.test"
    venus.vm.network "private_network", ip: "192.168.57.102"
    venus.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y bind9
      echo "Configurando Venus"
    SHELL
  end


