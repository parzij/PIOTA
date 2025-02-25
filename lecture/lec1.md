## **лекция 1.2: 18.02.2025**


### **Оценки трудоемкости алгоритма**


Временная сложность алгоритма - зависимость T(n) времени решения данным алгоритмом задачи от размерности задачи n

Пространственная сложность алгоритмов - зависимость V(n) объема памяти необходимого для решения задачи данным алгоритмом

При определении сложности:
1. рассматривается реализация алгоритма на некотором абстрактном устройстве
2. рассматривается худший случай задачи для каждой размерности
3. используются асимптотические оценки
---

1. Если алгоритм сводится к однократному циклу просмотра всех элементов - O(n)
2. Если в алгоритме выполняется просмотр всех пар элементов -  O(n^2)
3. Если в алгоритме предусматривается разложение задачи размерности n на k подзадач размерности n - 1 - O(k^n)
4. Если в задаче требуется найти некоторый элемент из множества мощности  n и на каждом шаге алгоритма удается сократить множество поиска вдвое то алгоритм - O(log n)
5. Если каждый шаг алгоритма сводится к однократному просмотру множества из n элементов и затем повторению такого же шага для каждой из половин этого множества,  то такой алгоритм - O(nlogn)

| Сложность f(n) | размерность задачи n | 10        | 20        | 30        | 40        | 50        | 60        |
|-----------------|----------------------|-----------|-----------|-----------|-----------|-----------|-----------|
| n               | 0.00001              | 0.00002   | 0.00003   | 0.00004   | 0.00005   | 0.00006   | 0.00007   |
| n^2             | 0.0001 c             | 0.0004 c  | 0.0009 c  | 0.0016 c  | 0.0025 c  | 0.0036 c  | 0.0049 c  |
| n^3             | 0.001 c              | 0.008 c   | 0.027 c   | 0.064 c   | 0.125 c   | 0.216 c   | 0.343 c   |
| 2^n             | 0.001 c              | 1.0 c     | 17,9 мин  | 12,7 дней | 35,7 лет  | 366 лет   | ---       |


---
## **Введение в теорию автоматов**

**Теория автоматов** - это раздел дискретной математики, который посвящен автоматным моделям реальных устройств и систем, предназначенных для обработки дискретной задачи и помощью заданного алгоритма, без учета их физических или технических характеристик

**Автоматная модель** - отражает лишь самые общие принципы строения и функционирования таких устройств, важные с точки зрения переработки и хранения информации.

**Конечные автоматы** является математической моделью устройств, перерабатывающих дискретную входную информацию в режиме "реального времени", т.е. в темпе ее поступления.

Конечный распознаватель А задается пятью множествами (V, K, M, S, Z):
входным алфавитом - V = {s1, s2, ...., sm} из символов которого составляются которого составляются входные данные последовательности.

конечным множеством  K = {q1, q2, ...., qr}, в которых может находится автомат.
функцией переходов  M : K x V -> P(K).
P(K) - bool множества K, которая ставит в соответствие любой паре (qi, si).
