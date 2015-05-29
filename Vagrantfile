require './userConfig.rb'

Vagrant.configure(2) do |config|

  config.vm.box = "ubuntu/trusty64"

  # stop vagrant from generating a random ssh key on each up
  config.ssh.insert_key = false

  # use ssh keys from host machine for ssh connections (handy for cloning git repos)
  config.ssh.forward_agent = true

  # shared folders
  config.vm.synced_folder "./code", "/var/www"
  config.vm.synced_folder "./log", "/var/log/apache2"

  # map local ports
  config.vm.network "forwarded_port", guest: 80, host: $webPort

  config.vm.provision "ansible" do |ansible|
    ansible.playbook   = "ansible/playbook.yml"
    ansible.extra_vars = { ansible_ssh_user: 'vagrant' }
    ansible.sudo       = true
  end

end
