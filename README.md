# Docker homework

### Требования

GIT, docker, docker-compose

### Установка

```
git clone https://gitlab.school.noveogroup.com/kussainovyerlan/lesson-9_docker.git
```
```
make build
```

#### Возможные проблемы

Порт, на котором вы запусткаете проект, может быть занят другим процессом на вашей машине. Чтобы это исправить, вы можете изменить значение переменной среды *NGINX_PORT* в файле *.env*.

### Запуск проекта

```
docker-compose up -d
```

Теперь вы можете обратиться к проекту по адресу 127.0.0.1:8888

### Задание

- [ ] Добавить в *Makefile* полезные команды для ускорения ввода команд docker-compose.

- [ ] К имеющимся контейнерам добавить контейнер с базой данных MySQL. При конфигурации контейнера необходимо использовать переменные среды из файла *.env*.

- [ ] Импортировать файл дампа базы данных в базу, располагающуюся внутри контейнера.

  Подсказки:
  > Вы можете пробросить порт базы данных из контейнера в вашу машину и подключиться к базе, используя функционал WebStorm.
  > 
  > Вы можете добавить контейнер с adminer, пробросить порт adminer наружу и подключиться к базе данных с помощью него.
  >
  > Также вы можете использовать следуюшую bash команду:
  >
  > ```
  > docker exec -i lesson9-db mysql -uuser -ppasswd --database=lesson9 < lesson9.sql
  > ```
  >
  > Но для этого у контейнера должен быть указан *container_name: lesson9-db* 