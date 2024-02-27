Для запуска плейбука провериль запущен ли Docker и установлен модуль python3-docker

Запуск - ansible-playbook playbook.yml
Доступные роли - NGINX

До запуска отредактировать playbook.yml:

nginx_setup: true/false - Включить/выключить установку Nginx в контейнере
configure_nginx: true/false - Включить/выключить Обновление конфигурации Nginx 
nginx_test: true/false - Включить/выключить тестирование доступности хостов после развертывания

в роли по пути ../nginx_role/task/configure_nginx.yml указать пути где находится текущая конфигурация (dest) и где находится желаемая конфигурация (src)

в роли по пути ../nginx_role/task/nginx_sutep.yml указать пути для монтирования папок с конфигурациями для nginx в разделе volumes 
