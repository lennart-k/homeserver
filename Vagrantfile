# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure(2) do |config|
  config.vm.box = "debian/bookworm64"

  # config.vm.network "private_network", ip: "172.30.1.5"
  # config.vm.network "forwarded_port", guest: 80, host: 8080, host_ip: "127.0.0.1"
  # config.vm.provision "ansible_local" do |ansible|
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "tests.yml"
    ansible.compatibility_mode = "2.0"
    ansible.galaxy_role_file = "requirements.yml"
    ansible.become = true
  end
end
