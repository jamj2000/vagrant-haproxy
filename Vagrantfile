Vagrant.configure("2") do |config|
    config.vm.define :frontend do |frontend|
        frontend.vm.box = "debian/bullseye64"
        frontend.vm.hostname = "ha"
        frontend.vm.synced_folder ".", "/vagrant", disabled: true
        frontend.vm.network :private_network,
          :libvirt__network_name => "red1",
          :libvirt__dhcp_enabled => false,
          :ip => "10.0.0.100",
          :libvirt__forward_mode => "veryisolated"
    end
    config.vm.define :backend1 do |backend1|
      backend1.vm.box = "debian/bullseye64"
      backend1.vm.hostname = "backend1"
      backend1.vm.synced_folder ".", "/vagrant", disabled: true
      backend1.vm.network :private_network,
        :libvirt__network_name => "red1",
        :libvirt__dhcp_enabled => false,
        :ip => "10.0.0.10",
        :libvirt__forward_mode => "veryisolated"
      #backend1.vm.provision "shell",
      #  run: "always",
      #  inline: "sudo ip route add default via 10.0.0.100"
    end
    config.vm.define :backend2 do |backend2|
      backend2.vm.box = "debian/bullseye64"
      backend2.vm.hostname = "backend2"
      backend2.vm.synced_folder ".", "/vagrant", disabled: true
      backend2.vm.network :private_network,
        :libvirt__network_name => "red1",
        :libvirt__dhcp_enabled => false,
        :ip => "10.0.0.11",
        :libvirt__forward_mode => "veryisolated"
      #backend2.vm.provision "shell",
      #  run: "always",
      #  inline: "sudo ip route add default via 10.0.0.100"
      
    end
  end
  