University: [ITMO University](https://itmo.ru/ru/)
Faculty: [FICT](https://fict.itmo.ru)
Course: [Network programming](https://github.com/itmo-ict-faculty/network-programming)
Year: 2024/2025
Group: K34212
Author: Shelyagov Alexey
Lab: Lab3
Date of create: 20.03.2025
Date of finished: 20.03.2025

## Лабораторная работа №3 "Развертывание Netbox, сеть связи как источник правды в системе технического учета Netbox"

## Описание

В данной лабораторной работе ознакомитcя с интеграцией Ansible и Netbox и изучить методы сбора информации с помощью данной интеграции.

## Цель работы

С помощью Ansible и Netbox собрать всю возможную информацию об устройствах и сохранить их в отдельном файле.

## Ход работы

Первым делом была проверена связность узлов для дальнейшей работы

<img src="./img/1.png" width=900>

Netbox будет развернут в контейнере, так что для начала добавим в конфигурацию трансляцию портов.

<img src="./img/2.png" width=900>

Запустим контейнер, который подкачает все необходимые зависимости.

<img src="./img/3.png" width=900>

Создадим пользователя для доступа к web-интерфейсу.

<img src="./img/4.png" width=900>

Netbox успешно поднялся в контейнере.

<img src="./img/5.png" width=900>

Добавим всю информацию об устройствах.

<img src="./img/6.png" width=900>

С помощью ansible выгрузим данные из Netbox в файл.

<img src="./img/7.png" width=900>

Убедимся в успешности выгрузки.

<img src="./img/8.png" width=900>

Создадим playbook для изменения IP и имен узлов.

<img src="./img/9.png" width=900>

Запустим данный playbook.

<img src="./img/10.png" width=900>

Заметим что playbook успешно выполнился, поменяв IP и имена на узлах.

<img src="./img/11.png" width=900>

В окончании напишем playbook, котрорый добавит данные в Netbox.

<img src="./img/12.png" width=900>



## Вывод

В результате лабораторной работы был развернут Netbox, с помощью которого была задокументирована система. Также, были созданны 2 playbook'а, работающие с данными из playbook'ов.
