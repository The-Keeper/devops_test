elk
=========

Устанавливает ELK-стек на ноду с помощью docker-compose.

Примеры использования
----------------

---
- name: Install ELK stack
  hosts: hosts
  become: true

  roles:
    - elk