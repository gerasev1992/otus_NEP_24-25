## 1. Проверьте связь. ##

#### Проверьте способность компьютеров обмениваться эхо-запросами. ####

1. Успешно ли выполняется эхо-запрос от коммутатора S1 на коммутатор S2?
2. Успешно ли выполняется эхо-запрос от коммутатора S1 на коммутатор S3?

**`SW1->SW2 | SW1->SW3`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_ping.png)

3. Успешно ли выполняется эхо-запрос от коммутатора S2 на коммутатор S3?

**`SW2->SW3`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_ping2-3.png)

#### Отобразите данные протокола spanning-tree. ####

**`SW1`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_SW1(def).png)

**`SW2`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_SW2(def).png)

**`SW3`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_SW3(def).png)

**С учетом выходных данных, поступающих с коммутаторов, ответьте на следующие вопросы. **`SW2`****

Какой коммутатор является корневым мостом? **Ответ: SW1**

Почему этот коммутатор был выбран протоколом spanning-tree в качестве корневого моста? **Ответ: min MAC-address SW1**

Какие порты на коммутаторе являются корневыми портами? **Fa0/1**

Какие порты на коммутаторе являются назначенными портами? **Fa0/3-4**

Какой порт отображается в качестве альтернативного и в настоящее время заблокирован? **Fa0/2**

Почему протокол spanning-tree выбрал этот порт в качестве невыделенного (заблокированного) порта? **Данный порт Fa0/2 подключен к RootSwitch вторым портом. Выбран заблокированным т.к. При одинаковом BID и COST далее оценивается PortPriority (чем меньше тем выше приоритет) => Fa0/1 - 128.1, < Fa0/2 - 128.2.

Определите коммутатор с заблокированным портом.

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_SW3(def).png)

Просмотрите изменения протокола spanning-tree

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_SW2(cost).png)

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_SW3(cost).png)

Почему протокол spanning-tree заменяет ранее заблокированный порт на назначенный порт
и блокирует порт, который был назначенным портом на другом коммутаторе?



Наблюдение за процессом выбора протоколом STP порта, исходя из приоритета портов.

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_SW1(full).png)

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_SW2(full).png)

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/lab002_SW3(full).png)
