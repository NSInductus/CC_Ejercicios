Vagrant.configure("2") do |config|
    config.vm.box = "debian/jessie64"
    #config.vm.box = "freebsd/FreeBSD-12.0-CURRENT"
    config.vm.provider "virtualbox" do |virtualbox|
        virtualbox.memory = 2048
        virtualbox.cpus = 2
    end

end

#Vagrant.configure("2") do |config|
    #config.vm.box = "ubuntu/bionic64"
    #config.vm.network "forwarded_port", guest: 8080, host: 8080
    #config.vm.network "forwarded_port", guest: 8000, host: 8000
    #config.vm.provider "virtualbox" do |virtualbox|
        #virtualbox.memory = 2048
        #virtualbox.cpus = 2
    #end
    #config.vm.provision "shell" do |s|
        #s.inline = "echo hello"
    #end
    #config.vm.provision "ansible" do |ansible|
        #ansible.playbook = "./workstate.yml"
    #end

#end
