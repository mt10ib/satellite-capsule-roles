# satellite-capsule-roles

### Install Satellite and Capsule servers

###### run.yaml:
```
 ---
- hosts: all
    
  vars_files:
    - ../satellite-capsule-roles/roles/capsule_install/vars/vars.yml
    - ../satellite-capsule-roles/roles/satellite_install/vars/vars1.yml

  tasks:
    # - import_role:
    #     name: satellite_install

    - import_role:
        name: capsule_install
```

###### Run the playbook:
```
 ansible-playbook  -i inventory run.yaml 
```