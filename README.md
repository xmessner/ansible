Ansible playbook to download and deploy Pharo 3
===============================================

This playbook is the first version to help you download and deploy **Pharo 3** on all your serveur or in cloud.

All you need is **Ansible 1.6** (1.5 should work but not tested) on your controler server and a recent Linux distrib on your remote server.

To download the latest version you need to use this

```
ansible-playbook -i hosts download.yml
```

To deploy it on all your servers

```
ansible-playbook -i hosts deploy.yml
```

You must edit the hosts file to adapt it for you environment.

