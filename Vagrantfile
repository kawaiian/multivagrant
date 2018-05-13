Vagrant.configure("2") do |config|
    config.vm.define "host1" do |host1|
        host1.vm.box = "ubuntu/xenial64"
        host1.vm.hostname = "host1.akira"
        host1.vm.network :private_network, ip: "192.168.56.101"
        host1.vm.provision "file", source: "hosts", destination: "/tmp/hosts"

        host1.vm.provision "shell", inline: "mv /tmp/hosts /etc/hosts"
    end
    config.vm.define "host2" do |host2|
        host2.vm.box = "ubuntu/xenial64"
        host2.vm.hostname = "host2.akira"
        host2.vm.network :private_network, ip: "192.168.56.102"
        host2.vm.provision "file", source: "hosts", destination: "/tmp/hosts"

        host2.vm.provision "shell", inline: "mv /tmp/hosts /etc/hosts"
    end
    config.vm.define "host3" do |host3|
        host3.vm.box = "ubuntu/xenial64"
        host3.vm.hostname = "host3.akira"
        host3.vm.network :private_network, ip: "192.168.56.103"
        host3.vm.provision "file", source: "hosts", destination: "/tmp/hosts"

        host3.vm.provision "shell", inline: "mv /tmp/hosts /etc/hosts"
    end

end