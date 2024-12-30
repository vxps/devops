# devops
## **Цель работы**

Научиться писать Molecule-тесты для ролей

## **Рекомендуемая документация**

- [Habr об OpenVPN](https://habr.com/ru/post/233971/)
- [VPN: ещё раз просто о сложном](https://habr.com/ru/post/534250/)
- [Урок из Школы DevOps: Тестирование ролей в Molecule](https://www.youtube.com/watch?v=0b3YXlffo1Q)
- [Статья про Molecule — тестируем роли Ansible](https://habr.com/ru/post/437216/)

## **Ход работы**

1. Написать Ansible Playbook поднимающий OpenVPN сервер
2. Через Molecule инициировать структуру для роли и вынести задачи поднятия сервера, с конфигурацией через переменные
3. При завершении работы плейбук должен разместить в playbook-dir артефактный ovpn-файл для подключения
4. Роль должна проходить стандартные тестами molecule test
5. Плейбук подключает роль через ansible-galaxy

## **Ход выполнения лабораторной** ##
1. Установили молекул командой ```pipx install molecule```
2. Создали роль openvpn и инициализировали сценарий молекул командой
``` molecule init scenario ```
3. Создали репо для роли openvpn(https://github.com/vxps/openvpn)
4. Установили роль
``` ansible-galaxy install -r requirements.yml ```
5.Запустили плейбук
``` ansible-playbook -i /inventory/local/hosts.ini lab4.yml ```
6. Запустили тесты
``` molecule test```
