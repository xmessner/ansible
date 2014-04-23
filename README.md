Ansible playbook to download and deploy Pharo 3
===============================================

# Installation

This playbook is the first version to help you download and deploy **Pharo 3** on all your serveurs or in cloud.

All you need is **Ansible version 1.6** (1.5 should work but not tested) on your main server and a recent Linux distrib on your remote servers.

To download the latest version you need to use this

```
ansible-playbook -i hosts download.yml
```

To deploy it on all your servers

```
ansible-playbook -i hosts deploy.yml
```

You must edit the hosts file to adapt it for your needs and declare all your servers. In this playbook the host named **controler** is always localhost.
Then you have to change **destRemoteDir** in every **host_vars/<srv>** files. Pharo will be installed in the directory. Each remote can have its own directory.

Now you have no excuse to not test Pharo 3 !

# Login on remote servers

By default Ansible will use ssh keys to login. I use this configuration to have keys (**~/.ansible.cfg**)

```
[defaults]
host_key_checking=false
private_key_file=/path/to/key/file
```

Then to use the right user in playbook you have to add this

```
  user: optimus
  sudo: yes
```

When playbook is lauch it will use the ssh key and then log into the remote server with **optimus** as user. All actions will be launched with sudo (root). So be really carfull when you write playooks.

# Future playbooks (wishes)

- Deploy latest version of Pillar
- Deploy Seaside
- Launch Zn with listeners
