Vagrant.configure("2") do |config|

  
  config.vm.define "yolo" do |yolo|
    config.vm.box = "geerlingguy/ubuntu2004"
    config.vm.network "private_network", type: "dhcp"
    yolo.vm.hostname = "vagrant"
    yolo.ssh.forward_agent = true
    yolo.ssh.port = 2222    

    yolo.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
    yolo.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end
end
