dns
=========

Обновляет конфигурацию DNS-серверов.

Примеры использования
----------------

Устанавливает вариант по умолчанию:

- hosts: servers
  roles:
    - role: dns

Устанавливает выбранные сервера:

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