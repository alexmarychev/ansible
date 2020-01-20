#Playbook для деплоя nginx

1. Запускается командой ```ansible-playbook nginx.yml``` в корне репозитория.
2. Файл ```ansible.cfg``` содержит информацию о пользователе и инвентарном файле ```hosts```
3. Playbook ```nginx.yml``` содержит конфигурацию для установки репозитория epel, установки nginx и конфигурирования nginx с помощью шаблона jinja2.

#Роль для деплоя nginx

1. Запускается командой ```ansible-playbook site.yml``` в корне репозитория.
2. Файл ```site.yml``` для запуска роли nginx.
3. Директория ```roles``` содержит роль для деплоя nginx.
4. Директория ```roles/nginx/defaults``` содержит файл main.yml с переменными по умолчанию.
5. Директория ```roles/nginx/handlers``` содержит файл main.yml с handlers.
6. Директория ```roles/nginx/tasks``` содержит файлы:

- ```main.yml``` включает все необходимые tasks
- ```epel.yml``` установка репозитория epel
- ```nginx.yml``` установка nginx
- ```nginx_conf.yml``` конфигурация nginx

7. Директория ```roles/nginx/templates``` содержит шаблон jinja2 для конфигурации nginx.
