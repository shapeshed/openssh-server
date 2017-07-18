Vagrant.configure("2") do |config|
  #config.vm.box = "ubuntu/trusty64"
  #config.vm.box = "debian/jessie64"
  #config.vm.box = "centos/7"
  config.vm.box = "terrywang/archlinux"

  #config.ssh.insert_key = false

  config.vm.provision :ansible do |ansible|
    ansible.playbook = "tests/test.yml"
    #ansible.inventory_path = "tests/inventory"
    ansible.sudo = true
  end
end
