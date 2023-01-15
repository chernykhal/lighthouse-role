Lighthouse-role
=========

Requirements
------------
Для установки роли создайте 'requirements.yml'
```
- name: lighthouse-role
  src: git@github.com/chernykhal/lighthouse-role.git
  scm: git
  version: "[last version]"
```
Role Variables
--------------
[defaults/main.yml](./defaults/main.yml) - изменяемые параметры;

[tasks/install/git.yml](./tasks/install/git.yml) - установка Git, на случай если на сервере нет гита;

[tasks/install/lighthouse.yml](./tasks/install/lighthouse.yml) - установка сервиса Lighthouse;

[tasks/configure.yml](./tasks/configure.yml) - развертывание конфига Lighthouse для Nginx;

[vars/main.yml](./vars/main.yml) - постоянные параметры для сервиса Lighthouse;

Example usage:
----------------
```
- name: Install Lighthouse
  hosts: [host]
  roles:
    - lighthouse_role
```
-------

