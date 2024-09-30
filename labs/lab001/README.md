# Фильтрация в OSPF

###  Задание:


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
