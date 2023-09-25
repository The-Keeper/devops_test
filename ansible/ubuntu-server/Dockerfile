# Используем Ubuntu 18.04 как базовый образ
FROM ubuntu:18.04

# установим sudo и службу ssh (требуются для ansible) 
RUN apt update 
RUN apt install -y openssh-server 
RUN apt install -y sudo
RUN apt install -y openresolv 

# Создадим пользователя admin
RUN adduser --shell /bin/bash admin\
    && echo "admin ALL=(ALL) NOPASSWD: ALL " >> /etc/sudoers 
RUN adduser admin root

# пароль админа = test. Не применять в проде!
RUN echo 'admin:test' | chpasswd

# настраиваем SSH
RUN mkdir /var/run/sshd

# открываем порт 22
EXPOSE 22

# запускаем службу ssh
CMD ["/usr/sbin/sshd", "-D"]

