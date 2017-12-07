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

## Configuration
The main configuration file: `roles/kubeadm/defaults/main.yml`
* pod cidr is defined by the variable `POD_CIDR`
* To use Flannel `flannel: true`
* To use Calico `calico: true`

>Note:  only one network add-on can be used.

## Roadmap
- [x] Support Calico network add-on
- [ ] Support Weave network add-on
- [ ] End-to-end tests

## License
The source code in this repo is licensed under the GPL 3
