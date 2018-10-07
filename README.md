# ansible-davfs2

ansible-davfs2 is an Ansible role to install and configure davfs2 mounts a debian based OS

It performs: 

* installation of davfs2
* disable lock in davfs2 configuration
* manage secrets for davfs2 mount
* mount davfs2 resources

## Install
### Clone
```bash
git clone https://github.com/lgaggini/ansible-davfs2.git
```
## Configuration

The configuration is done by vars listed and explained in [defaults/main.yml](https://github.com/lgaggini/ansible-davfs2/blob/master/defaults/main.yml) file.

## Usage

```
- name: bootstrap an ubuntu cloud image for davfs2
  hosts: webserver
  vars_files:
    - group_vars/davfs2.yml

  roles:
    - { role: davfs2, tags: ['davfs2'] }
```
