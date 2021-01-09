# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
  config.vm.define "cybersec" do |cybersec|
    cybersec.vm.box = "kalilinux/rolling"
    cybersec.vm.box_check_update = false

    cybersec.vm.hostname = "cybersec"
    cybersec.vm.network "private_network",ip: "192.168.200.10", dns:"8.8.8.8"

    cybersec.vm.provider "virtualbox" do |vb|
      vb.memory = 4096
      vb.cpus = 2
    end

    config.vm.provision "file", source: "tmux.conf", destination: "/home/vagrant/.tmux.conf"
    config.vm.provision "file", source: "bash_aliases", destination: "/home/vagrant/.bash_aliases"
    config.vm.provision "shell", inline: <<-SHELL
      sudo cp /home/vagrant/.tmux.conf /root/
      sudo cp /home/vagrant/.bash_aliases /root/
      sudo timedatectl set-timezone America/Sao_Paulo
    SHELL
  end
end
