## Ответвы на вопросы ##

## **`DHCPv4`** ##

#### Создайте схему адресации ####

1. Subnet A: 192.168.1.0/26 (.1-.63) (Vlan 100)
2. Subnet B: 192.168.1.64/27 (.65-.95) (Vlan 200)
3. Subnet C: 192.168.1.96/28 (.97-.111)(Client Network at R2)

#### Активируйте интерфейс G0/0/1 на маршрутизаторе. Убедитесь, что суб-интерфейсы работают. ####

**`R1`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab004/img/lab004_sub_int.png)

#### Убедитесь, что статическая маршрутизация работает, пропинговав адрес G0/0/1 маршрутизатора R2 с маршрутизатора R1. ####

**`R1->R2`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab004/img/lab004_ping_R2.png)

#### Почему интерфейс F0/5 указан в списке VLAN 1? ####

**`Ответ: Интерфейс F0/5 указан в списке VLAN 1, потому что по умолчанию все порты коммутатора находятся в этой VLAN.`**

#### На данный момент какой IP-адрес будет у ПК, если они подключены к сети с помощью DHCP? ####

**`Ответ: IP address из диапазона 169.254.0.0/16 т.к. DHCP-server еще не настроен.`**

#### Проверьте состояние магистрали. Fa0/5 ####

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab004/img/lab004_fa0.5.png)

#### Проверьте конфигурацию сервера DHCPv4 ####

**Выполните команду show ip dhcp pool, чтобы просмотреть сведения о пуле.**

**`R1`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab004/img/lab004_dhcp_pool.png)

**Выполните команду show ip dhcp bindings, чтобы просмотреть установленные назначения адресов DHCP.**

**`R1`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab004/img/lab004_dhcp_binding.png)

#### Проверьте подключение, пропинговав IP-адрес интерфейса G0/0/1 на R1. ####

**`PC-A->R1 int Gi0/1.100-Gi0/1.200`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab004/img/lab004_ping_R1_gig0.1_pcA.png)

#### Проверка полной связанности ####

**`PC-A->PC-B`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab004/img/lab004_tracert_PCA-PCB.png)

**`PC-B->PC-A`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab004/img/lab004_tracert_PCB-PCA.png)

## **`DHCPv6`** ##

DHCPv6


Убедитесь, что маршрутизация работает, пропинговав адрес G0/0/1 маршрутизатора R2 с маршрутизатора R1.

Откуда взялась часть адреса host-id?
Введите свои ответы здесь.

 Проверьте подключение, пропинговав IP-адрес интерфейса G0/0/1 на R2.

 Проверьте соединение, пропинговав IP-адрес интерфейса G0/0/1 в R1.
