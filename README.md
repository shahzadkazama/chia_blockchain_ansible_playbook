# chia_blockchain_ansible_playbook

#Step by step chia blockchain installation on ubuntu 20 with lates code 1.1.1

	#Use the below repo to install chia blockchain
	https://github.com/shahzadkazama/chia_blockchain_ansible_playbook.git

1-
  # install ansible and git on base machine
	apt install ansible git -y

2-
  # git clone the ansible playbook for chia blockchain
	git clone https://github.com/shahzadkazama/chia_blockchain_ansible_playbook.git

3-
  # update the hosts file according to your chia machine
	my_vm ansible_ssh_host=54.176.214.34 ansible_ssh_user=root ansible_ssh_port=22 ansible_ssh_pass=redhat_1

4-
  # install the sshpass utility on base machine
	apt install sshpass -y
	
5-
  # execute the playbook
	cd chia_blockchain_ansible_playbook/playbook
	ansible-playbook -i hosts -l vm site.yaml
