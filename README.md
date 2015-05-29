# dev-vm
Basic LAMP Development VM with a few added extras (Mongo, Redis, NodeJS etc)

## How to use
1. Install VirtualBox https://www.virtualbox.org
2. Install Vagrant https://www.vagrantup.com
3. Install Ansible http://docs.ansible.com/intro_installation.html
4. Clone the dev-vm repo `git clone git@github.com:barrycrayon/dev-vm.git`
5. Copy userConfig.rb.example to userConfig.rb and edit the new file to change any parameters to your preferred values `cp userConfig.rb.example userConfig.rb` 
6. Run the VM
```
cd dev-vm
vagrant up
```

Any html/php code you place in the `code` dir will be available at http://localhost:[webPort]
