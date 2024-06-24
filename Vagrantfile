Vagrant.configure("2") do |config|
  # Configuration de la machine de test
  config.vm.define "test" do |test|
    test.vm.box = "ubuntu/bionic64"
    test.vm.hostname = "test-env"
    test.vm.network "private_network", ip: "192.168.56.102"
    test.vm.provision "shell", inline: <<-SHELL
      # Installer Docker
      sudo apt-get update
      sudo apt-get install -y docker.io
      sudo usermod -aG docker vagrant
      # Installer Docker Compose
      sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
      sudo chmod +x /usr/local/bin/docker-compose
    SHELL
  end

  # Configuration de la machine de production
  config.vm.define "prod" do |prod|
    prod.vm.box = "ubuntu/bionic64"
    prod.vm.hostname = "prod-env"
    prod.vm.network "private_network", ip: "192.168.56.103"
    prod.vm.provision "shell", inline: <<-SHELL
      # Installer Docker
      sudo apt-get update
      sudo apt-get install -y docker.io
      sudo usermod -aG docker vagrant
      # Installer Docker Compose
      sudo curl -L "https://github.com/docker/compose/releases/download/1.29.2/docker-compose-$(uname -s)-$(uname -m)" -o /usr/local/bin/docker-compose
      sudo chmod +x /usr/local/bin/docker-compose
    SHELL
  end
end



