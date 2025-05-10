Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  
  # Configuración de red
  config.vm.network "private_network", ip: "192.168.56.10"
  
  # Configuración de puertos
  config.vm.network "forwarded_port", guest: 80, host: 1234
  config.vm.network "forwarded_port", guest: 22, host: 2222

  # Configuración de la memoria y CPU
  config.vm.provider "virtualbox" do |vb|
    vb.memory = "1024"
    vb.cpus = 2
  end
  
  # Aumentar el tiempo de espera al arrancar
  config.vm.boot_timeout = 600  # 10 minutos
end
