# lab_101. Проектирование сети

###  Задание: Распланировать адресное пространство. Настроить IP на всех активных портах. Адресное пространство должно быть задокументировано.

- Разработаете и задокументируете адресное пространство для лабораторного стенда.
- Настроите ip адреса на каждом активном порту.
- Настроите каждый VPC в каждом офисе в своем VLAN.
- Настроите VLAN/Loopbackup interface управления для сетевых устройств.
- Настроите сети офисов так, чтобы не возникало broadcast штормов, а использование линков было максимально оптимизировано.
----------------------------------------------------------------------------------------------------------------------------------------------------------------------

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab005/Full_schema_OTUS.png)

### MSK AS1001 ###

| Location  | Device | Interface  |  IPv4  | 
| ------------- | ------------- | ------------- | ------------- | 
| MSK  | R14  | GigabitEthernet0/0  | 101.101.101.2  | 
| MSK  | R14  | GigabitEthernet0/1  | 10.0.12.1  |
| MSK  | R14  | GigabitEthernet0/2  | 10.0.19.1  | 
| MSK  | R14  | GigabitEthernet0/3  | 10.0.13.1  |
| MSK  | R14  | Loo0  | 10.14.15.1   | 10.0.0.0/8 |
| MSK  | R14  | Tunnel101  | 172.16.31.1   |
| MSK  | R15  | GigabitEthernet0/0  | 102.102.102.2  | 
| MSK  | R15  | GigabitEthernet0/1  | 10.0.23.1  | 
| MSK  | R15  | GigabitEthernet0/2  | 10.0.20.1  |
| MSK  | R15  | GigabitEthernet0/3  | 10.0.22.1  | 
| MSK  | R15  | Loo0  | 10.14.15.2   |
| MSK  | R15  | Tunnel102  | 172.16.30.1   | -- |
| MSK  | R12  | Ethernet0/0.100  | 10.10.100.254  |   
| MSK  | R12  | Ethernet0/0.101  | 10.10.101.254 |    
| MSK  | R12  | Ethernet0/2.100  | 10.10.100.252  |   
| MSK  | R12  | Ethernet0/2.101  | 10.10.101.253   |  
| MSK  | R12  | Ethernet0/1  | 10.0.12.2         | 
| MSK  | R12  | Ethernet0/3   | 10.0.22.2         | 
| MSK  | R12  | Loo0  | 10.0.10.1         | 
| MSK  | R13 | Ethernet0/0.100   | 10.10.100.253    | 
| MSK  | R13  | Ethernet0/0.101  | 10.10.102.254       | 
| MSK  | R13  | Ethernet0/2.100  | 10.10.100.251     | 
| MSK  | R13  | Ethernet0/2.101  | 10.10.102.253     | 
| MSK  | R13  | Ethernet0/1  | 10.0.23.2               | 
| MSK  | R13  | Ethernet0/3   | 10.0.13.2               | 
| MSK  | R13  | Loo0  | 10.0.30.1              |
| MSK  | R19  | Ethernet0/2  | 10.0.19.2        | 
| MSK  | R19  | Loo0  | 10.0.19.2               | 
| MSK  | R20  | Ethernet0/2   | 10.0.20.2              | 
| MSK  | R20  | Loo0  | 10.15.20.1              | 
| MSK  | SW2  | Vlan100  | 10.10.100.2  | 
| MSK  | SW3  | Vlan100  | 10.10.100.3  |
| MSK  | SW4  | Vlan100  | 10.10.100.4  | 
| MSK  | SW5  | Vlan100  |10.10.100.5  | 
| MSK  | VPC1  | eth0  | DHCP(R12)  | 
| MSK  | VPC7  | eth0  | DHCP(R13)  | 

### SPB AS2042 ###

| Location  | Device | Interface  |  IPv4  |
| ------------- | ------------- | ------------- | ------------- |
| SPB  | R18  | GigabitEthernet0/0  | 110.110.110.2  | 
| SPB  | R18  | GigabitEthernet0/1  | 111.111.111.2  | 
| SPB  | R18  | GigabitEthernet0/2  | 10.21.42.1  |
| SPB  | R18  | GigabitEthernet0/3  | 10.21.42.5   | 
| SPB  | R18  | Loo0  | 10.0.42.18  | 
| SPB  | R18 | Tunnel101  | 172.16.31.2   | 
| SPB  | R17 | Ethernet0/2  | 10.21.42.2   | 
| SPB  | R17 | Ethernet0/1.100  |  10.21.100.254  | 
| SPB  | R17 | Ethernet0/1.101  |  10.21.101.254  | 
| SPB  | R17 | Ethernet0/0.100  |  10.21.100.252  | 
| SPB  | R17 | Ethernet0/0.101  |  10.21.101.253  | 
| SPB  | R17  | Loo0  | 10.0.42.17   | 
| SPB  | R16 | Ethernet0/0 | 10.21.42.9  | 
| SPB  | R16 | Ethernet0/3 | 10.21.42.6  | 
| SPB  | R16 | Ethernet0/1.100 | 10.21.100.253 | 
| SPB  | R16 | Ethernet0/1.102 | 10.21.102.254 | 
| SPB  | R16 | Ethernet0/2.100  |  10.21.100.251  |
| SPB  | R16 | Ethernet0/2.102 |  10.21.101.253  | 
| SPB  | R16  | Loo0  | 10.0.42.16   |
| SPB  | R32 | Ethernet0/0      |          10.21.42.10  | 
| SPB  | R32  | Loo0  | 10.0.42.32   | 
| SPB  | SW9  | Vlan100  | 10.21.100.9  | 
| SPB  | SW10  | Vlan100  | 10.21.100.10  |
| SPB  | VPC  | eth0  | DHCP(R16)  | 
| SPB  | VPC8  | eth0  | DHCP(R17)  |

### Chokurdakh ###

| Location  | Device | Interface  |  IPv4  | 
| ------------- | ------------- | ------------- | ------------- | 
| CHKR  | R28  | GigabitEthernet0/0  | 150.150.10.2  | 
| CHKR   | R28   | GigabitEthernet0/1  | 150.150.10.10  | 
| CHKR   | R28   | GigabitEthernet0/2.100  | 10.50.100.254  |
| CHKR   | R28   | GigabitEthernet0/2.101  | 10.50.101.254  | 
| CHKR   | R28   | GigabitEthernet0/2.102 | 10.50.102.254  | 
| CHKR   | R28   | Tunnel102  | 172.16.30.2   | 
| CHKR   | R28  | Loo0  | 10.190.10.254  | 
| CHKR  | SW29  | Vlan100  | 10.50.100.29  | 
| CHKR  | VPC30  | eth0  | DHCP(R28.101)  | 
| CHKR  | VPC31 | eth0  | DHCP(R28.101)  | 

### Labytnangi ###

| Location  | Device | Interface  |  IPv4  | 
| ------------- | ------------- | ------------- | ------------- | 
| LBT | R27 | Ethernet0/0      |          150.150.10.18  |
| LBT  | R27  | Tunnel102  | 172.16.30.3   | 
| LBT  | R27  | Loo0  | 10.150.150.27   | 10.150.150.0/25 |

### Kitor AS101 ###

| Location  | Device | Interface  |  IPv4  | 
| ------------- | ------------- | ------------- | ------------- | 
| KTR | R22 | Ethernet0/0      |          101.101.101.1  | 
| KTR  | R22  | Ethernet0/1 | 104.104.104.1   | 
| KTR  | R22  | Ethernet0/2  | 100.100.100.1  | 


### Lamas AS301 ###

| Location  | Device | Interface  |  IPv4  | 
| ------------- | ------------- | ------------- | ------------- |
| LMS | R21 | Ethernet0/0      |          102.102.102.1  |
| LMS | R21  | Ethernet0/1 | 104.104.104.2   | 
| LMS | R21  | Ethernet0/2  | 103.103.103.1  |

### Threeada AS520 ###

| Location  | Device | Interface  |  IPv4  | 
| ------------- | ------------- | ------------- | ------------- | 
| TA | R23 | Ethernet0/0      |          10.23.25.1  |
| TA | R23  | Ethernet0/1 | 10.23.24.1   | 
| TA | R23  | Ethernet0/2  | 100.100.100.2  | 
| TA | R23  | Loopback0      |  10.0.0.23  | 
| TA | R24 | Ethernet0/0      |          110.110.110.1  |
| TA | R24  | Ethernet0/1 | 10.23.24.2   | 10.0.0.0/8 |
| TA | R24  | Ethernet0/2  | 103.103.103.2  | 
| TA | R24  | Ethernet0/3  |  10.24.26.1   | 
| TA | R24  | Loopback0      | 10.0.0.24  | 
| TA | R25 | Ethernet0/0      |          10.23.25.2 | 
| TA | R25 | Ethernet0/2  | 10.25.26.1   | 
| TA | R25 | Ethernet0/1  | 150.150.10.17   | 
| TA | R25 | Ethernet0/3  |  150.150.10.9  |
| TA | R25  | Loopback0      | 10.0.0.25  |
| TA | R26  | Ethernet0/1 |   111.111.111.1    | 
| TA | R26 | Ethernet0/2  | 10.24.26.2   | 
| TA | R26 | Ethernet0/3    | 10.25.26.2   | 
| TA | R26 | Ethernet0/0   | 150.150.10.1  | 
| TA | R26  | Loopback0      | 10.0.0.26    |
