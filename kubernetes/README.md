# Выполнение задания по Kubernetes

Находясь в данном каталоге:

1. Собрать контейнер:
```console
docker build --tag python-webapp-docker python-webapp-docker/
```

2. Запустить контейнер, открыв порт:
```
docker run -p 8080:8080 python-webapp-docker
```
3. Убедиться, что приложение работает, перейдя по ссылке:
http://localhost:8080/

