# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

    config.vm.box = "ubuntu/bionic64"

    config.vm.hostname = "mdm-lamp"

    config.vm.network "forwarded_port", guest: 80, host: 8085
    config.vm.network "private_network", ip: "192.168.33.110"

    config.vm.synced_folder ".", "/var/www", :mount_options => ["dmode=777", "fmode=666"]

    config.ssh.insert_key = false

    config.vm.provision "shell", path: "install.sh", privileged: false

end
