Role Nginx
=========
Роль включает в себя два этапа:

* Установка версии nginx-1.16.1 на RedHat Family OS с конфигурацией по шаблону.
* Создание по шаблону двух тестовых виртуал хостов в /etc/nginx/conf.d/

Далее можно проводить тестирование работы этих виртуал хостов на порту 80.

Requirement
----------------
Отсутствуют.

Configuration templates
----------------
Основной шаблон конфигурации и шаблон для виртуал хостов
* nginx_conf: "nginx.conf.j2"
* nginx_vhost: "vhost.conf.j2"

Имена vhost указываются в loop блоке смотри tasks - name:Add Nginx vhosts.

Example Playbook
----------------
```
- hosts: server
  roles:
        - { role: nginx }
```

Author Information
------------------
ramon_st for Rebrain
