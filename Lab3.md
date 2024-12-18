## Лабораторная работа 3
***
<h5 align="center">Министерство науки и высшего образования Российской Федерации

ФЕДЕРАЛЬНОЕ ГОСУДАРСТВЕННОЕ АВТОНОМНОЕ ОБРАЗОВАТЕЛЬНОЕ УЧРЕЖДЕНИЕ ВЫСШЕГО ОБРАЗОВАНИЯНАЦИОНАЛЬНЫЙ ИССЛЕДОВАТЕЛЬСКИЙ УНИВЕРСИТЕТ ИТМО

ITMO University


Отчет по лабораторной работе № 3

По дисциплине Информатика

Короткова Алиса Александровна

Факультет инфокоммуникационных технологий

Группа К3160

Направление подготовки 45.03.04 Интеллектуальные системы в гуманитарной сфере

Образовательная программа Языковые модели и искусственный интеллект</h5>
***


В ходе выполения лабораторной работы, я настроила три виртуальные машины Ubuntu в VirtualBox (А, Б и В) и между ними организовала сетевой доступ, таким образом:

1. доступ есть из машины А в машину Б
2. доступ есть из машины А в машину В
3. нет доступа из машины Б в машину В

### Ход работы

1. Первым делом я создала три виртуальные машины Ubuntu в VirtualBox.

2. Я создала 2 NAT Networks (NATNetwork, NATNetwork1 - с разными ip адрессами) с помощью Tools в VirtualBox.

<img width="700" src="images/abctools.png"/>

3. Далее в настройках А, Б и В я подключила их к этим сетям. Таким образом, что для А на первом адапрере - NATNetwork, а на втором - NATNetwork1. Для Б - NATNetwork. Для В - NATNetwork1.

Для машины А

<img width="700" src="images/a1.png"/>

<img width="700" src="images/a2.png"/>

Для машины Б

<img width="700" src="images/b1.png"/>

Для Машины В

<img width="700" src="images/c1.png"/>


4. Для всех трех виртуальных машин я проверила доступ в сеть Интернет с помощью команды `ping google.com`.

Для машины А

<img width="700" src="images/agoogle.png"/>

Для машины Б

<img width="700" src="images/bgoogle.png"/>

Для Машины В

<img width="700" src="images/cgoogle.png"/>

Во всех трех случаях доспут есть.

4. Следущим шагом я проверила ip адреса для каждой машины с помощью команды 'ip a':

А - 10.0.2.15 и 10.0.3.4

<img width="700" src="images/aip.png"/>

Б - 10.0.2.4

<img width="700" src="images/bip.png"/>

В - 10.0.3.5

<img width="700" src="images/cip.png"/>

5. Дальше проверила как работает сетевой доступ, который я настроила. Я вводила 'ping ipaddress'

Для машины А (есть доступ в В и в Б)

<img width="700" src="images/acheck.png"/>

Для машины Б (есть доступ в А, но нет в В)

<img width="700" src="images/bcheck.png"/>

Для Машины В (есть доступ в А, но нет в Б)

<img width="700" src="images/ccheck.png"/>



Таким образом, все работает так, как было задано условием лабораторной.

