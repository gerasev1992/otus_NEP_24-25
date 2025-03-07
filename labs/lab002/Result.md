## Ответвы на вопросы ##

#### Проверьте способность компьютеров обмениваться эхо-запросами. ####

1. Успешно ли выполняется эхо-запрос от коммутатора S1 на коммутатор S2?
2. Успешно ли выполняется эхо-запрос от коммутатора S1 на коммутатор S3?

**`SW1->SW2 | SW1->SW3`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_ping.png)

3. Успешно ли выполняется эхо-запрос от коммутатора S2 на коммутатор S3?

**`SW2->SW3`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_ping2-3.png)

#### Отобразите данные протокола spanning-tree. ####

**`SW1`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_SW1(def).png)

**`SW2`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_SW2(def).png)

**`SW3`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_SW3(def).png)

**С учетом выходных данных, поступающих с коммутаторов, ответьте на следующие вопросы.** **`SW2`**


Какой коммутатор является корневым мостом? **`Ответ: SW1`**

Почему этот коммутатор был выбран протоколом spanning-tree в качестве корневого моста?
**`Ответ: min MAC-address SW1`**

Какие порты на коммутаторе являются корневыми портами? **`Ответ: Fa0/1`**

Какие порты на коммутаторе являются назначенными портами? **`Ответ: Fa0/3-4`**

Какой порт отображается в качестве альтернативного и в настоящее время заблокирован? **`Ответ: Fa0/2`**

Почему протокол spanning-tree выбрал этот порт в качестве невыделенного (заблокированного) порта? **`Ответ: Данный порт Fa0/2 подключен к RootSwitch вторым портом. Выбран заблокированным т.к. При одинаковом BID и COST далее оценивается PortPriority (чем меньше тем выше приоритет) => Fa0/1 - 128.1, Fa0/2 - 128.2.`**


**Определите коммутатор с заблокированным портом.**

**`SW3`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_SW3(def).png)

**Просмотрите изменения протокола spanning-tree**

**`SW2`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_SW2(cost).png)

**`SW3`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_SW3(cost).png)

Почему протокол spanning-tree заменяет ранее заблокированный порт на назначенный порт
и блокирует порт, который был назначенным портом на другом коммутаторе? **`Ответ: Понижение cost ведет к повышение приоритета, тем самым назначается раннее заблокированный порт`**

**Наблюдение за процессом выбора протоколом STP порта, исходя из приоритета портов.**

**`SW1`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_SW1(full).png)

**`SW2`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_SW2(full).png)

**`SW3`**

![](https://github.com/gerasev1992/otus_NEP_24-25/blob/main/labs/lab002/img/lab002_SW3(full).png)

Какой порт выбран протоколом STP в качестве порта корневого моста на каждом коммутаторе
некорневого моста? **`Ответ: SW2 => Fa0/1 | SW3 => Fa0/3`**

Почему протокол STP выбрал эти порты в качестве портов корневого моста на этих коммутаторах? **`Ответ: При одинаковом BID и COST далее оценивается PortPriority (чем меньше тем выше приоритет).`**

**Вопросы для повторения**
1. Какое значение протокол STP использует первым после выбора корневого моста, чтобы определить
выбор порта? **`Ответ: cost`**

3. Если первое значение на двух портах одинаково, какое следующее значение будет использовать
протокол STP при выборе порта? **`Ответ: PortPriority`**

4. Если оба значения на двух портах равны, каким будет следующее значение, которое использует
протокол STP при выборе порта? **`Ответ: PortPriority`**
