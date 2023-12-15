# Mosh VM

VM with Mosh

## Basic VM

Setup you VM using [basic-vm](https://github.com/andrtell/basic-vm).

## Ansible

Create the file `inventory.yaml`.

```
ungrouped:
  hosts:
    vm01:
      ansible_host: vm01
```

## Mosh VM

Run the playbook `playbooks/01_mosh.yaml`.

```
ansible-playbook -i inventory.yaml --ask-become-pass playbooks/01_mosh.yaml
```

## Mosh

Connect to your server using Mosh

```
mosh agent@vm01
```
