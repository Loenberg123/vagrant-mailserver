# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
 config.vm.define "mail" do |mail|
  mail.vm.box = "ubuntu/trusty64"
  mail.vm.hostname = 'mail.example.com'
  mail.vm.network "public_network", ip: "192.168.1.26"
 #mail.vm.synced_folder "/shared", "/var/www/html"
  mail.vm.provision "shell", :inline => "apt-get update -y"
  mail.vm.provision :ansible do |ansible|
        ansible.playbook = "main.yml"
  end
 end
end
