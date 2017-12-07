## Introduction

Deploy K8s with Kubeadm by Ansible.

## Prerequisites
You need to install these tools in your laptop:
* Ansible
* Vagrant
* VirtualBox

## How to use
Bootstrap the VMs

```
$ Vagrant up
```
 Deploy K8s
 ```
 $ ansible-playbook kubeadm.yml
 ```

 ## Roadmap
- [ ] Support other network add-ons
- [ ] End-to-end tests

## License
The source code in this repo is licensed under the GPL 3
