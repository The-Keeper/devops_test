dns
=========

Обновляет конфигурацию DNS-серверов.

Примеры использования
----------------

- hosts: servers
  roles:
    - role: dns
      nameservers: ["1.1.1.1", "8.8.8.8"]

- hosts: servers
  roles:
    - role: dns
      nameservers: 
        - "1.1.1.1"
        - "8.8.8.8"