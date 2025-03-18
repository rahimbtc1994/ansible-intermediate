# Ansible course

## Getting started
Ansible is an open-source IT automation tool used for configuration management, application deployment, infrastructure provisioning, and orchestration.
Env : Three VMs to do the hadns-on labs

## SSH overview
- ssh key : more secure connexion 
- password : the default 

Steps to do :
1. We ensure that openssh is installed on all server/nodes...
2. Make connections between the workstations and servers
3. Create SSH key pair with passphrase for normal usage
4. Copy that key to every server
5. Create SSh key pair without passphrase for ansible
6. Copy that key to each server

Generate ssh key pair (private key and public key)
$ ssh-keygen -t ed25519 -C "User default"
- path to save the file
- passphrase
you can check the workstation ~/.ssh folder

Use the key
$ ssh-copy-id -i /path/to/publickey serverip@
- password
you can see the content of the server ~/.ssh/authorized_keys

If you try to connect to a server using ssh it ask you for the passphrase and not the password
$ ssh serverip@

Generate ssh key pair for ansible
$ ssh-keygen -t ed25519 -C "Ansible"
- path : customize it
- passphrase : none
$ ssh-copy-id -i /path/to/ansiblepublickey serverip@

If you try to connect to a server using ssh it will not ask you for the passphrase nor the password
$ ssh -i /path/to/ansiblekey serverip@

To avoid typing ssh passphrase everytime (for normal usage), not permanent:
$ eval $(ssh-agent) 
$ ssh-add 

To avoid typing ssh passphrase everytime (for normal usage), semi permanent, create an alias:
$ alias ssha='eval $(ssh-agent) && ssh-add'

To avoid typing ssh passphrase everytime (for normal usage), permanent, add  this to ~/.bashrc:
eval $(ssh-agent) && ssh-add