Ansible playbook to download and deploy Pharo 3
===============================================

# Installation

This playbook is the first version to help you download and deploy **Pharo 3** on all your serveurs or in cloud.

All you need is **Ansible version 1.6** (1.5 should work but not tested) on your main server and a recent Linux distrib on your remote server.

To download the latest version you need to use this

```
ansible-playbook -i hosts download.yml
```

To deploy it on all your servers

```
ansible-playbook -i hosts deploy.yml
```

You must edit the hosts file to adapt it for your needs and declare all your servers. In this playbook the host named **controler** is always localhost. Then you have to change **destRemoteDir** in download.yml file. Pharo will be installed in the directory.

Now you have no excuse to not test Pharo 3 !

# Future playbooks (wishes)

- Deploy latest version of Pillar
- Deploy Seaside
- Launch Zn with listeners
