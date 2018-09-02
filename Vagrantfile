Vagrant.configure("2") do |config|
  config.vm.box = "bento/ubuntu-16.04"

  config.vm.network "private_network", ip: "192.168.33.10"

  config.vm.synced_folder "sssignal2-2", "/home/vagrant/sssignal2-2"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "provisioning/site.yml"
    ansible.inventory_path = "provisioning/hosts"
    ansible.limit = 'all'
  end

  config.vm.provision "shell", inline: <<-SHELL
    git clone https://github.com/mizzsig/Dotfiles.git
    mv /home/vagrant/Dotfiles/.bashrc /home/vagrant/
    mv /home/vagrant/Dotfiles/.bash_profile /home/vagrant/
    mv /home/vagrant/Dotfiles/.vimrc /home/vagrant/
    rm -rf /home/vagrant/Dotfiles
  SHELL
end
