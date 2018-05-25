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
 ansible-playbook  -i inventory run.yaml 
```