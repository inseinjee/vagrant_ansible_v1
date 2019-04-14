# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant_API_Version ="2"

Vagrant.configure(Vagrant_API_Version) do |config|

  #==============#
  # CentOS nodes #
  #==============#
  
  #Ansible-Node201	 
  config.vm.define:"ansible-node201" do |cfg|
     cfg.vm.box = "centos/7"
	 cfg.vm.provider:virtualbox do |vb|
	   vb.name="Ansible-Node201(github_SysNet4Admin)"
	 end
	 cfg.vm.host_name="ansible-node201"
	 cfg.vm.synced_folder ".", "/vagrant", disabled: true
	 cfg.vm.network "public_network", ip: "192.168.1.201"
	 cfg.vm.network "forwarded_port", guest: 22, host: 60201, auto_correct: false, id: "ssh"
	 cfg.vm.provision "shell", path: "bash_ssh_conf_4_CentOS.sh"
  end

  #Ansible-Node202	 
  config.vm.define:"ansible-node202" do |cfg|
     cfg.vm.box = "centos/7"
	 cfg.vm.provider:virtualbox do |vb|
	   vb.name="Ansible-Node202(github_SysNet4Admin)"
	 end
	 cfg.vm.host_name="ansible-node202"
	 cfg.vm.synced_folder ".", "/vagrant", disabled: true
	 cfg.vm.network "public_network", ip: "192.168.1.202"
	 cfg.vm.network "forwarded_port", guest: 22, host: 60202, auto_correct: false, id: "ssh"
	 cfg.vm.provision "shell", path: "bash_ssh_conf_4_CentOS.sh"
  end  

  #Ansible-Node203	 
  config.vm.define:"ansible-node203" do |cfg|
     cfg.vm.box = "centos/7"
	 cfg.vm.provider:virtualbox do |vb|
	   vb.name="Ansible-Node203(github_SysNet4Admin)"
	 end
	 cfg.vm.host_name="ansible-node203"
	 cfg.vm.synced_folder ".", "/vagrant", disabled: true
	 cfg.vm.network "public_network", ip: "192.168.1.203"
	 cfg.vm.network "forwarded_port", guest: 22, host: 60203, auto_correct: false, id: "ssh"
	 cfg.vm.provision "shell", path: "bash_ssh_conf_4_CentOS.sh"
  end  

  #Ansible-Node204	 
  config.vm.define:"ansible-node204" do |cfg|
     cfg.vm.box = "centos/7"
	 cfg.vm.provider:virtualbox do |vb|
	   vb.name="Ansible-Node204(github_SysNet4Admin)"
	 end
	 cfg.vm.host_name="ansible-node204"
	 cfg.vm.synced_folder ".", "/vagrant", disabled: true
	 cfg.vm.network "public_network", ip: "192.168.1.204"
	 cfg.vm.network "forwarded_port", guest: 22, host: 60204, auto_correct: false, id: "ssh"
	 cfg.vm.provision "shell", path: "bash_ssh_conf_4_CentOS.sh"
  end  

  #================#
  # Ansible Server #
  #================#
  
  config.vm.define:"ansible-server" do |cfg|
     cfg.vm.box = "centos/7"
	 cfg.vm.provider:virtualbox do |vb|
	   vb.name="Ansible-Server(github_SysNet4Admin)"
	 end
	 cfg.vm.host_name="ansible-server"
	 cfg.vm.synced_folder ".", "/vagrant", disabled: true
	 cfg.vm.network "public_network", ip: "192.168.1.10"
	 cfg.vm.network "forwarded_port", guest: 22, host: 60010, auto_correct: false, id: "ssh"
	 cfg.vm.provision "shell", path: "bootstrap.sh"
	 cfg.vm.provision "file", source: "Ansible_env_ready.yml", destination: "Ansible_env_ready.yml"
	 cfg.vm.provision "shell", inline: "ansible-playbook Ansible_env_ready.yml"
     cfg.vm.provision "shell", path: "bash_ssh_conf_4_CentOS.sh"
  end
  
end
