Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  config.vm.provision "ansible" do |ansible|
    ansible.playbook   = "ansible/playbook.yml"
    ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
    ansible.sudo       = true
  end

end
