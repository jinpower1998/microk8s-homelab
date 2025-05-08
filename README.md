# MicroK8s-Deploy

### Simple playbook to spin up microk8s on any plattform !


![](docs/images/ansible+microk8s.png)

## Instructions

This Ansible-Playbook creates a [mikrok8s](https://microk8s.io/)-Cluster with custom amount of nodes. 
You can run this playbook anywhere you want: locally, On-Premise or on Cloud-Instances

### Prerequisites:

  - SSH-access on your machines
  - [snap](https://snapcraft.io/) installed on your hosts and running
  - user for previlige escalation on your hosts

###  Fill in your hosts file:


### Run the Playbook

- Locally

If you simply want the playbook to run locally:

```
ansible-playbook  --connection=local --inventory 127.0.0.1,  ansible/site.yaml --ask-become-pass
``` 