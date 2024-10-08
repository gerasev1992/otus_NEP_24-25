# VLAN

###  Задание:
Настройка DTP.
Добавление сетей VLAN и назначение портов.


```
R3:
conf t
 router ospf 10
  area 42 stub no-summary
  exit
 exit

R8:
conf t
 router ospf 10
  area 42 stub
  exit
 exit

R14:
conf t
 router ospf 10
  area 42 stub
  exit
 exit
```

###  Задание1:

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab001/config/test_image_git.png)

Все файлы изменений приведены [здесь](config/)

 Общая таблица сетей.

| Network IPv4     | Summary net    | Network IPv6             | Summary net         | Description   | Eq&port         |
|-----------------:|:---------------|-------------------------:|:--------------------|:-------------:|-----------------|
| 90.90.128.0/24   | 90.90.128.0/22 | 20FF:CCFF:FFFF:1::/64    | 20FF:CCFF:FFFF::/48 | ISP network   | R17e0/1 R18e0/1 |
| 90.90.129.0/24   | 90.90.128.0/22 | 20FF:CCFF:FFFF:2::/64    | 20FF:CCFF:FFFF::/48 | ISP network   | R17e0/2 R19e0/2 |
| 90.90.130.0/25   | 90.90.128.0/22 | 20FF:CCFF:FFFF:3::/64    | 20FF:CCFF:FFFF::/48 | ISP network   | R18e0/2 R20e0/2 |

