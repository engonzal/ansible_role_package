### Ansible Roles: Package

Module to install a list of packages.  

#### Role Variables
For general packages when not using mixed Operating Systems you can use the following:
```
package_list:
- git
- curl
```

If you have mixed Operating Systems you may need to use the following:
```
package_apt:
- python-dev

package_yum:
- python-devel
```

#### Example Playbook

```
    - hosts: servers
      vars:
        package_list:
        - curl
        - htop
      roles:
         - { role: engonzal.package, tags: [ 'package'] }
```

#### License

BSD
