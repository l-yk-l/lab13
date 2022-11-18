# Лабораторная работа №13

**Установка и настройка nginx**

1. Установка
```
$ sudo pacman -S nginx
```
2. Настройка файла `/etc/nginx/nginx.conf`
```
$ curl https://raw.githubusercontent.com/l-yk-l/lab13/master/proxy/todos.conf | sudo tee /etc/nginx/nginx.conf > /dev/null
```

**Проверка работоспособности**
1. Запуск nginx
```bash
$ sudo systemctl start nginx
```
2. Билд и запуск проекта
```bash
$ cd path/to/project/directory
$ cargo run
```
3. Проверка
```bash
$ curl http://127.0.0.1/v1/todos/63443a02-2137-48e8-8db5-79fa54e8bfdf
> {"assigned":"user@example.com","id":"63443a02-2137-48e8-8db5-79fa54e8bfdf","message":"Just do it!","priority":"A"}
```
