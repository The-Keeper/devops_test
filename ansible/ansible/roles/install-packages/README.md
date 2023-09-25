install-packages
=========

Устанавливает пакеты в Ubuntu через apt.

Примеры использования
----------------

- hosts: servers
  roles:
    - role: install-packages
      packages: 
      - nmap
      - traceroute
      - vim
      - nano
      - htop