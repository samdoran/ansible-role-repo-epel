Vagrant.configure(2) do |config|

  config.vm.define :centos6 do |v|
    v.vm.box = "geerlingguy/centos6"

    v.vm.network "private_network", type: "dhcp"

    v.vm.hostname = "centos6.vagrant.com"

    v.vm.provider :virtualbox do |p|
      p.memory = 1024
      p.customize ["modifyvm", :id, "--paravirtprovider", "kvm"]
    end
  end

  config.vm.define :centos7 do |v|
    v.vm.box = "jkyle/centos-7.0-x86_64"

    v.vm.network "private_network", type: "dhcp"

    v.vm.hostname = "centos7.vagrant.com"

    v.vm.provider :virtualbox do |p|
      p.memory = 1024
      p.customize ["modifyvm", :id, "--paravirtprovider", "kvm"]
    end
  end

  config.vm.provision "ansible" do |a|
    a.playbook = "tests/vagrant.yml"
  end

end
