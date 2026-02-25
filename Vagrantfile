Vagrant.configure("2") do |config|
  config.vm.provider "qemu" do |qemu|
    qemu.memory = "4096"
    qemu.gui = true
    qemu.qemu_img_cmd = "create"
    qemu.qemu_img_opts = "-f qcow2"
    qemu.disk_size = "20G"
  end
  
  config.vm.provision "shell", inline: <<-SHELL
    apt-get update
    apt-get install -y openssh-server
    systemctl enable ssh
  SHELL
end
