
Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"
  config.vm.network "private_network", ip:"192.168.50.55"
  config.vm.synced_folder ".", "/sergio-martinez-sisin"

  config.vm.provision "shell", inline: <<-SHELL

  # Actualizacion automatica al iniciar
  sudo apt update

  # Generar desde el entorno real archivo e inserts
  echo "--Insertar datos de una lista de 'menus'" > /home/vagrant/datos_menus.sql
  echo "INSERT INTO gestion_menus.menus (nombre, creador, tiempo, precio) VALUES" >> /home/vagrant/datos_menus.sql
  echo "('Fabada', 'ElXokas', 20, 10)," >> /home/vagrant/datos_menus.sql
  echo "('Secreto', 'Naide', 30, 50)," >> /home/vagrant/datos_menus.sql
  echo "('Macheroni', 'JeyKey', 10, 15)," >> /home/vagrant/datos_menus.sql
  echo "('Sardinillas', 'Nano', 20, 5)," >> /home/vagrant/datos_menus.sql
  echo "('Costillar', 'Alguiñano', 30, 30)" >> /home/vagrant/datos_menus.sql

  SHELL
 
end
