Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty32"

#  config.vm.provision :shell do |shell|
#    shell.inline = "touch $1 && chmod 0440 $1 && echo $2 > $1"
#    shell.args = %q{/etc/sudoers.d/root_ssh_agent "Defaults env_keep += \"SSH_AUTH_SOCK\""}
#  end


  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "playbook.yml"
  end

  config.ssh.forward_agent = true
end
