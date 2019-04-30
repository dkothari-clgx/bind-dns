Vagrant.configure("2") do |config|
    config.vm.define "dns" do |dns|
        dns.vm.network "private_network", ip: "192.168.1.2"
        dns.vm.box = "ubuntu/trusty64"
        dns.vm.provision :ansible do |ansible|
          ansible.playbook = "ansible/site.yml"
        end
    end

    config.vm.define "test" do |test|
        test.vm.network "private_network", ip: "192.168.1.6"
        test.vm.box = "ubuntu/trusty64"
        test.vm.provision :ansible do |ansible|
          ansible.playbook = "ansible/site.yml"
        end
    end
end
