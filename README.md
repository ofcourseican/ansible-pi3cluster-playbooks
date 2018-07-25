# Ansible Playbook for Raspberry Pi Cluster Configuration

This is the ansible playbook repository I use to configure my RPI3 Kubernetes cluster.

## Standard Cluster Configuration

```bash
ansible-playbook setup.yml --extra-vars "hosts=cluster"
```

## Add Clusteruser on master

```bash
ansible-playbook user.yml --extra-vars "username=<username> password=<password> hosts=master" -b
```

## Add user to nodes

```bash
ansible-playbook user.yml --extra-vars "username=<username> password=<password> copy-ssh=true hosts=nodes" -b
```
