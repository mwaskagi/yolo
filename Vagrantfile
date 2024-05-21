Vagrant.configure("2") do |config|

  
  config.vm.define "yolo" do |yolo|
    config.vm.box = "ubuntu/jammy64"
    yolo.vm.network "private_network", ip: "192.168.56.11"
    yolo.vm.hostname = "yolo"
    yolo.ssh.forward_agent = true
    yolo.ssh.port = 2222    
    yolo.vm.synced_folder ".", "/vagrant"
    yolo.vm.provider "virtualbox" do |vb|
      vb.memory = "1024"
    end
    yolo.vm.provision "ansible" do |ansible|
      ansible.playbook = "playbook.yml"
    end
  end
end
