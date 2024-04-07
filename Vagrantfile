Vagrant.configure("2") do |config|
   config.vm.box = "jborean93/WindowsServer2019"
   config.winrm.ssl_peer_verification = false # Disable SSL verification

   config.vm.provider "virtualbox" do |hv|
      hv.cpus = "2"
      hv.memory = "2048"
      hv.linked_clone = true
   end

   config.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook-ansible.yml"
      ansible.verbose = "v"
   end
end

