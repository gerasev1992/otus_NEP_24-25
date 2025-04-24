### MSK AS1001 ###

| Location  | Device | Interface  |  IPv4  | IPv4 sum net |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| MSK  | R14  | GigabitEthernet0/0  | 101.101.101.2  | -- |
| MSK  | R14  | GigabitEthernet0/1  | 10.0.12.1  |10.0.0.0/8 |
| MSK  | R14  | GigabitEthernet0/2  | 10.0.19.1  | 10.0.0.0/8 |
| MSK  | R14  | GigabitEthernet0/3  | 10.0.13.1  |10.0.0.0/8 |
| MSK  | R14  | Loo0  | 10.14.15.1   | 10.0.0.0/8 |
| MSK  | R14  | Tunnel101  | 172.16.31.1   | -- |
| MSK  | R15  | GigabitEthernet0/0  | 102.102.102.2  | -- |
| MSK  | R15  | GigabitEthernet0/1  | 10.0.23.1  | 10.0.0.0/8|
| MSK  | R15  | GigabitEthernet0/2  | 10.0.20.1  |10.0.0.0/8 |
| MSK  | R15  | GigabitEthernet0/3  | 10.0.22.1  | 10.0.0.0/8 |
| MSK  | R15  | Loo0  | 10.14.15.2   | 10.0.0.0/8 |
| MSK  | R15  | Tunnel102  | 172.16.30.1   | -- |
| MSK  | R12  | Ethernet0/0.100              | 10.10.100.254     | 10.0.0.0/8 |
| MSK  | R12  | Ethernet0/0.101  | 10.10.101.254     | 10.0.0.0/8 |
| MSK  | R12  | Ethernet0/1  | 10.0.12.2         | 10.0.0.0/8 |
| MSK  | R12  | Ethernet0/3   | 10.0.22.2         | 10.0.0.0/8 |
| MSK  | R12  | Loo0  | 10.0.10.1         | 10.0.0.0/8 |
| MSK  | R13 | Ethernet0/0.100              | 10.10.100.254    | 10.0.0.0/8 |
| MSK  | R13  | Ethernet0/0.101  | 10.10.102.254       | 10.0.0.0/8 |
| MSK  | R13  | Ethernet0/1  | 10.0.23.2               | 10.0.0.0/8 |
| MSK  | R13  | Ethernet0/3   | 10.0.13.2               | 10.0.0.0/8 |
| MSK  | R13  | Loo0  | 10.0.30.1              | 10.0.0.0/8 |
| MSK  | R19  | Ethernet0/2  | 10.0.19.2        | 10.0.0.0/8 |
| MSK  | R19  | Loo0  | 10.0.19.2               | 10.0.0.0/8 |
| MSK  | R20  | Ethernet0/2   | 10.0.20.2              | 10.0.0.0/8 |
| MSK  | R20  | Loo0  | 10.15.20.1              | 10.0.0.0/8 |
| MSK  | SW2  | Vlan100  | 10.10.100.2  | 10.0.0.0/8 |
| MSK  | SW3  | Vlan100  | 10.10.100.3  |10.0.0.0/8 |
| MSK  | SW4  | Vlan100  | 10.10.100.4  | 10.0.0.0/8 |
| MSK  | SW5  | Vlan100  |10.10.100.5  | 10.0.0.0/8 |
| MSK  | VPC1  | eth0  | DHCP(R12)  | -- |
| MSK  | VPC7  | eth0  | DHCP(R13)  | -- |

### SPB AS2042 ###

| Location  | Device | Interface  |  IPv4  | IPv4 sum net |
| ------------- | ------------- | ------------- | ------------- | ------------- |
| SPB  | R18  | GigabitEthernet0/0  | 110.110.110.2  | -- |
| SPB  | R18  | GigabitEthernet0/1  | 111.111.111.2  | -- |
| SPB  | R18  | GigabitEthernet0/2  | 10.21.42.1  | 10.0.0.0/8 |
| SPB  | R18  | GigabitEthernet0/3  | 10.21.42.5   | 10.0.0.0/8 |
| SPB  | R18  | Loo0  | 10.0.42.18  | 10.0.0.0/8 |
| SPB  | R17 | Ethernet0/2  | 10.21.42.2   | 10.0.0.0/8 |
| SPB  | R17 | Ethernet0/1.100  |  10.21.100.254  | 10.0.0.0/8 |
| SPB  | R17 | Ethernet0/1.101  |  10.21.101.254  | 10.0.0.0/8 |
| SPB  | R17  | Loo0  | 10.0.42.17   | 10.0.0.0/8 |
| SPB  | R16 | Ethernet0/0 | 10.21.42.9  | 10.0.0.0/8 |
| SPB  | R16 | Ethernet0/3 | 10.21.42.6  | 10.0.0.0/8 |
| SPB  | R16 | Ethernet0/1.100 | 10.21.100.254 | 10.0.0.0/8 |
| SPB  | R16 | Ethernet0/1.102 | 10.21.102.254 | 10.0.0.0/8 |
| SPB  | R16  | Loo0  | 10.0.42.16   | 10.0.0.0/8 |
| SPB  | R32 | Ethernet0/0      |          10.21.42.10 | | 10.0.0.0/8 |
| SPB  | SW9  | Vlan100  | 10.21.100.2  | 10.0.0.0/8 |
| SPB  | SW10  | Vlan100  | 10.21.100.3  |10.0.0.0/8 |
| SPB  | R32  | Loo0  | 10.0.42.32   | 10.0.0.0/8 |
| SPB  | VPC  | eth0  | DHCP(R16)  | -- |
| SPB  | VPC8  | eth0  | DHCP(R17)  | -- |

Ethernet0/0                10.21.42.10     YES NVRAM  up                    up      
Ethernet0/1                unassigned      YES NVRAM  administratively down down  


Ethernet0/2                10.21.42.2      YES NVRAM  up                    up      
Ethernet0/3                unassigned      YES NVRAM  administratively down down    
Loopback1                  10.20.42.1      YES NVRAM  up        


Ethernet0/0                10.21.42.9      YES NVRAM  up                    up      
Ethernet0/1                unassigned      YES NVRAM  administratively down down    
Ethernet0/2                unassigned      YES NVRAM  administratively down down    
Ethernet0/3                10.21.42.6      YES NVRAM  up                    up      
Loopback1                  10.22.42.1      YES NVRAM  up                    up     


Ethernet0/2                10.21.42.2      YES NVRAM  up                    up      
Ethernet0/3                unassigned      YES NVRAM  administratively down down    
Loopback1                  10.20.42.1      YES NVRAM  up                    up  


GigabitEthernet0/0         110.110.110.2   YES NVRAM  up                    up      
GigabitEthernet0/1         111.111.111.2   YES NVRAM  up                    up      
GigabitEthernet0/2         10.21.42.1      YES NVRAM  up                    up      
GigabitEthernet0/3         10.21.42.5      YES NVRAM  up                    up     


Ethernet0/0.100            
Ethernet0/0.101            
Ethernet0/1                
Ethernet0/3                
Loopback0


MSK	R14	GigabitEthernet0/0         	101.101.101.2   
		GigabitEthernet0/1         	10.0.12.1       
		GigabitEthernet0/2         	10.0.19.1
		GigabitEthernet0/3         	10.0.13.1       
		Loopback0   	10.14.15.1      
		Tunnel1  	172.16.31.1     

			IPv4 sum net

План адресного пространства
В данной работе используется только IPv4.

Подсети для офисов и наименование устройств
Для офисов выделены подсети с префиксом 16 (для маленьких офисов это с большим запасом).

Для Офиса "Москва" выделена подсеть 10.10.0.0/16, наименование устройств R1X, SW1X,VPC1X.
Для Офиса "Киторн" выделена подсеть 10.20.0.0/16, наименование устройств R2X, SW2X, VPC2X.
Для Офиса "Ламас" выделена подсеть 10.30.0.0/16, наименование устройств R3X, SW3X,VPC3X.
Для Офиса "Триада" выделена подсеть 10.40.0.0/16, наименование устройств R4X, SW4X, VPC4X.
Для Офиса "Санкт-Петербург" выделена подсеть 10.50.0.0/16, наименование устройств R5X, SW5X, VPC5X.
Для Офиса "Лабытнанги " выделена подсеть 10.60.0.0/16, наименование устройств R6X, SW6X, VPC6X.
Для Офиса "Чокурдак " выделена подсеть 10.70.0.0/16, наименование устройств R7X, SW7X, VPC7X.
Подсети линков между офисами
Для взаимодействия между офисами используются подсети 172.16.1.0/24 - 172.16.10.0/24
