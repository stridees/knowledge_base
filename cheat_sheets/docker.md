# Docker

## Основные команды

### Управление контейнерами
- `docker run [OPTIONS] IMAGE [COMMAND] [ARG...]`: Запустить новый контейнер
- `docker start [OPTIONS] CONTAINER [CONTAINER...]`: Запустить один или несколько остановленных контейнеров
- `docker stop [OPTIONS] CONTAINER [CONTAINER...]`: Остановить один или несколько запущенных контейнеров
- `docker restart [OPTIONS] CONTAINER [CONTAINER...]`: Перезапустить один или несколько контейнеров
- `docker kill [OPTIONS] CONTAINER [CONTAINER...]`: Принудительно остановить один или несколько запущенных контейнеров
- `docker rm [OPTIONS] CONTAINER [CONTAINER...]`: Удалить один или несколько контейнеров
- `docker pause CONTAINER [CONTAINER...]`: Приостановить все процессы в одном или нескольких контейнерах
- `docker unpause CONTAINER [CONTAINER...]`: Возобновить все процессы в одном или нескольких контейнерах

### Управление образами
- `docker build [OPTIONS] PATH | URL | -`: Собрать образ из Dockerfile
- `docker pull [OPTIONS] NAME[:TAG|@DIGEST]`: Загрузить образ или репозиторий с реестра
- `docker push [OPTIONS] NAME[:TAG]`: Отправить образ или репозиторий в реестр
- `docker rmi [OPTIONS] IMAGE [IMAGE...]`: Удалить один или несколько образов
- `docker tag SOURCE_IMAGE[:TAG] TARGET_IMAGE[:TAG]`: Создать тег TARGET_IMAGE, ссылающийся на SOURCE_IMAGE

### Информация и мониторинг
- `docker ps [OPTIONS]`: Вывести список контейнеров
- `docker logs [OPTIONS] CONTAINER`: Получить логи контейнера
- `docker inspect [OPTIONS] NAME|ID [NAME|ID...]`: Возвращает низкоуровневую информацию об объектах Docker
- `docker events [OPTIONS]`: Получать события сервера в режиме реального времени
- `docker stats [OPTIONS] [CONTAINER...]`: Отображать потоки статистики использования ресурсов контейнерами
- `docker diff CONTAINER`: Проверить изменения в файловой системе контейнера
- `docker top CONTAINER [ps OPTIONS]`: Отобразить запущенные процессы контейнера

## Примеры использования

### Запуск контейнера
- `docker run -it --name my-container ubuntu bash`: Запустить интерактивный контейнер с именем "my-container" на основе образа Ubuntu и запустить в нем Bash
- `docker run -d -p 80:80 --name my-nginx nginx`: Запустить контейнер в фоновом режиме, пробросить порт 80 и назвать его "my-nginx" на основе образа Nginx

### Сборка образа
- `docker build -t my-image .`: Собрать образ с тегом "my-image" из Dockerfile в текущей директории
- `docker build -t my-image:v1.0 -f Dockerfile.prod .`: Собрать образ с тегом "my-image:v1.0" из Dockerfile.prod в текущей директории

### Управление контейнерами
- `docker stop my-container`: Остановить контейнер с именем "my-container"
- `docker rm -f my-container`: Принудительно удалить контейнер с именем "my-container"
- 