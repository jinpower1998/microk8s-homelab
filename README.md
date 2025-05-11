# Simple playbook to spin up microk8s on any plattform !


![](docs/images/ansible+microk8s.png)

## Instructions

This Ansible-Playbook creates a [microk8s](https://microk8s.io/)-Cluster with custom amount of nodes. 

You can run this playbook anywhere you want: locally, On-Premise or on Cloud-Instances.

### Prerequisites:

  - SSH-access on your machines
  - [snap](https://snapcraft.io/) installed on your hosts and running
  - user for previlige escalation on your hosts

###  Fill in your inventory file

Your Kubernetes-Nodes/Hosts should be grouped into masters and workers.

Localhost should also be in your hosts file

Example:

![](docs/images/screenshot-hosts.png)

### Run the Playbook



#### Single-Node

If you simply want to deploy a single-node cluster

```
ansible-playbook  --inventory [Hostname/IP-Address],  ansible/site.yaml --ask-become-pass
``` 

Locally:

```
ansible-playbook  --connection=local --inventory 127.0.0.1,  ansible/site.yaml --ask-become-pass       
``` 
