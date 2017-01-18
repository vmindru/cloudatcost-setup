Cloud At Cost - quick setup
=========

role to quick setup your virtual servers hosted @ Cloud At Cost

Requirements
------------

None

I recommend to use this one in tandem with [cloudatcost-ansible]https://github.com/vmindru/cloudatcostapi

### E.G. Doing first run against your env. 

```
ansible-playbook -i cloudatcost-ansible playbooks/cloudatcost/test.yml -e "ansible_ssh_pass={{hostvars[inventory_hostname].rootpass}}" -u root
```


Role Variables
--------------

user var defines, user , name , and private key 

```
user: 
  name: "user" 
  comment: "User Name"
  ssh_key_path: "/home/user/.ssh/cloudatcost.pub"
```


Dependencies
------------

None

Example Playbook
----------------

```
---
- hosts: cloudatcost
  roles:
    - {role: cloudatcost-setup }
```

License
-------

BSD

Author Information
------------------

Veaceslav Mindru - vmindru@redhat.com 

