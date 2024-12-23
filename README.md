# АНАЛИЗ ДАННЫХ И ИСКУССТВЕННЫЙ ИНТЕЛЛЕКТ [in GameDev]
Отчет по лабораторной работе #4 выполнил(а):
- Быкова Екатерина Владимировна
- РИ-230910

Отметка о выполнении заданий (заполняется студентом):

| Задание | Выполнение | Баллы |
| ------ | ------ | ------ |
| Задание 1 | * | 60 |
| Задание 2 | * | 20 |
| Задание 3 | * | 20 |

знак "*" - задание выполнено; знак "#" - задание не выполнено;

Работу проверили:
- к.т.н., доцент Денисов Д.В.
- к.э.н., доцент Панов М.А.
- ст. преп., Фадеев В.О.

[![N|Solid](https://cldup.com/dTxpPi9lDf.thumb.png)](https://nodesource.com/products/nsolid)

[![Build Status](https://travis-ci.org/joemccann/dillinger.svg?branch=master)](https://travis-ci.org/joemccann/dillinger)

## Цель работы
Реализовать принцип работы перцептрона, визуализировать ход его обучения и результаты работы.


## Задание 1
### в проекте Unity реализовать перцептрон, который умеет производить вычисления:

### OR | дать комментарии о корректности работы

### AND | дать комментарии о корректности работы

### NAND | дать комментарии о корректности работы

### XOR | дать комментарии о корректности работы


В процессе проверки было установлено, что все операторы, за исключением XOR, функционируют корректно и выдают ожидаемые результаты. Однако даже после 1000 эпох обучения XOR не смог достичь удовлетворительной точности, выдавая только два правильных значения при нескольких попытках.

Таким образом, из десяти эпох обучения мы получаем три корректно работающих оператора: OR, AND и NAND. Это обусловлено тем, что эти операторы являются линейно разделимыми, что является ключевым критерием для моделирования перцептрона, поскольку он использует только линейные функции.

Для XOR перцептрон не способен понять логику, поскольку в нём отсутствует свойство линейной разделимости, и невозможно построить прямую линию, которая однозначно разделит точки и определит кластеры. Для реализации XOR требуются нелинейные функции, и поэтому данная нейросеть не способна моделировать сложные зависимости. 


## Задание 2
### Построить графики зависимости количества эпох от ошибки  обучения. Указать от чего зависит необходимое количество эпох обучения.

![task 2](https://github.com/4ayka205/DA-in-GameDev-lab4/blob/main/img/and.png)

![task 2](https://github.com/4ayka205/DA-in-GameDev-lab4/blob/main/img/or.png)

![task 2](https://github.com/4ayka205/DA-in-GameDev-lab4/blob/main/img/nand.png)

![task 2](https://github.com/4ayka205/DA-in-GameDev-lab4/blob/main/img/xor.png)


В основном, количество эпох, необходимых для обучения перцептрона, зависит от типа оператора, для которого мы его обучаем. Однако, в целом, для обучения достаточно 10 эпох, за исключением оператора XOR, который, как мы выяснили, не может быть обучен с помощью перцептрона.

Для оператора NAND требуется больше эпох, чем для операторов OR и AND, в среднем 8, как показано на графиках. Операторы OR и AND обычно обучаются за 4–5 эпох. Я предполагаю, что это связано с тем, что у оператора NAND более сложные комбинации входных данных, и поэтому перцептрону требуется больше времени для установления чёткой зависимости. В результате этим операторам требуется больше итераций обучения для достижения стабильного и верного результата.


## Задание 3
### Построить визуальную модель работы перцептрона на сцене Unity.

В рамках проекта, реализованного в среде Unity, были созданы два куба. На каждый из них можно навесить объект, представляющий собой перцептрон, и в инспекторе указать номер входа, который будет соответствовать результату, подлежащему визуализации.

При взаимодействии с кубами и в зависимости от исходных входных значений, они меняют свой цвет: белый, если значение равно 0, и чёрный, если значение равно 1.


## Выводы

Реализованный перцептрон демонстрирует впечатляющие результаты в обучении для операций OR, AND и NAND, однако с операцией XOR у него возникают затруднения. В среднем перцептрону требуется 8 эпох обучения для корректного выполнения этой операции, что наглядно представлено на полученных графиках.

В процессе обучения общее количество ошибок может как уменьшаться от эпохи к эпохе, так и увеличиваться. Также было реализовано визуальное представление одного из входов перцептрона с помощью двух кубов.


## Powered by

**BigDigital Team: Denisov | Fadeev | Panov**
