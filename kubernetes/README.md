# Выполнение задания по Kubernetes

Находясь в данном каталоге:

1. Собрать контейнер:
```console
docker build --tag python-webapp-docker python-webapp-docker/
```

2. Запустить контейнер, открыв порт:
```console
docker run -p 8080:8080 python-webapp-docker
```
3. Убедиться, что приложение работает, перейдя по ссылке:
http://localhost:8080/

# Docker Hub и развёртывание с помощью helm:

Докеризованный образ размещен по ссылке: https://hub.docker.com/r/thekeepergh/python-demo-app

Сначала проверим, что чарт корректен: 
```console
helm lint helm-chart
```

Запустим чарт: 
```console
helm install python-web-app ./helm-chart/
```

Проверить, что он запущен, можно открыв дашборд: 
```console
minikube dashboard
```

