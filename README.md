# satellite-capsule-roles

### Install Satellite and Capsule servers

###### run.yaml:
```
---
- hosts: satellite
  tasks:
    - import_role:
        name: satellite_install
    
- hosts: capsule
  tasks:
    - import_role:
        name: capsule_install
```

###### Run the playbook:
```
running ssh_setup role: ansible-playbook  -i inventory run.yaml --ask-pass
ansible-playbook  -i inventory run.yaml 
```