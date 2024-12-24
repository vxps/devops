# devops
## **Цель работы**

Запустить приложение при помощи ansible, научиться писать плейбуки и пользоваться group vars

**Docker-образ:** https://hub.docker.com/repository/docker/timurbabs/django

Универсальный файл для вагранта: [Vagrantfile](https://drive.google.com/file/d/1Q5deuz9kcm9VeXDiX44iuHZZSp66VuAY/view?usp=share_link)

## **Рекомендуемая документация**

- [Инфраструктура как код #1: понятие инфраструктурного кода (Лекция)](https://www.youtube.com/watch?v=RS9fAJM0tf0&ab_channel=DeusOps)
- [Инфраструктура как код #2: Знакомство с Ansible (Лекция)](https://youtu.be/GFL6-DlSQH0)
- [Как поднимать виртуальные машины в Vagrant](https://www.youtube.com/watch?v=dgm5MtCcIMs&t=5150s)
- [Документация Ansible](https://docs.ansible.com/ansible/latest/user_guide/index.html#writing-tasks-plays-and-playbooks)
- [Подборка по Ansible](https://gitlab.com/deusops/lessons/documentation/ansible)

## **Ход работы**

1. Установить Ansible используя ([Гайд по установке](https://docs.ansible.com/ansible/latest/installation_guide/intro_installation.html))
2. Установить Vagrant ([Гайд по установке](https://developer.hashicorp.com/vagrant/downloads))
3. Поднять Vagrant хост из ссылки при помощи файла Vagrantfile используя команду ***vagrant up** ([VagrantFile](https://drive.google.com/drive/u/0/folders/1Ev8N8LijxNR2npEwhoUFlxBuznf--ujP))
4. Написать inventory-файл для развернутых хостов
5. Написать плейбук для установки Docker
6. Клонировать репо ([Репозиторий](https://github.com/mdn/django-locallibrary-tutorial)) на ноды группы [app]
7. Запустить приложение на нодах группы [app] используя ansible
