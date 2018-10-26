### Ansible Roles: Package
Module to install a list of packages.  


[![Build Status](https://travis-ci.org/engonzal/ansible_role_package.svg?branch=master)](https://travis-ci.org/engonzal/ansible_role_package)
#### Role Variables
For general packages when not using mixed Operating Systems you can use the following:
```
package_list:
- git
- curl
```

If you have mixed operating systems you may need to use the following:
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
