Grab Virtual Machine Information from a Subscription in Azure
=========

This role extracts pertinient information regarding virtual machines and network interface cards residing under a subscription in Azure and places it in two csv files.

Requirements
------------

ansible 2.9
azure_rm

Role Variables
--------------

``` yaml
SUBSCRIPTION_ID:
CLIENT_ID:
SECRET_ID:
TENANT_ID:
```

Dependencies
------------

A list of other roles hosted on Galaxy should go here, plus any details in regards to parameters that may need to be set for other roles, or variables that are used from other roles.

Example Playbook
----------------

``` yaml
- name: Grab VM Info from Subscription
  hosts: localhost
  pre_tasks:
    - name: adding vars
      set_fact:
        SUBSCRIPTION_ID:
        CLIENT_ID:
        SECRET_ID:
        TENANT_ID:
  connection: local
  roles:
    - azure-virtualmachineinfo
```

License
-------

BSD

Author Information
------------------

Samarjit Bhullar
