# Отчёт по лабораторной работе №10 по курсам “Основы информатики” и "Программно-аппаратные средства информатики"

<b>Студент группы:</b> <ins>М80-108Б-22 Формалёв Александр Сергеевич, № по списку 21</ins> 

<b>Контакты e-mail:</b> <ins>lyadiez@mail.ru</ins>

<b>Работа выполнена:</b> «16» <ins>ноября</ins> <ins>2022</ins> г.

<b>Преподаватель:</b> <ins>асп. каф. 806 Сахарин Никита Александрович</ins>

<b>Входной контроль знаний с оценкой:</b> <ins> </ins>

<b>Отчет сдан</b> «17» <ins>ноября</ins> <ins>2022</ins> г., <b>итоговая оценка</b> <ins> </ins>

<b>Подпись преподавателя:</b> ________________

## 1. Тема:
Отладчик системы программирования на языке Си.              
## 2. Цель работы:
Научиться работать в отладчике.
## 3. Задание:
Поставить точку останова в коде программы из задания номер 9.
## 4. Оборудование:

<b>Процессор:</b> AMD A9-9425 RADEON R5, 5 COMPUTE CORES 2C+3G 3.10 GHz <br/>

<b>ОП:</b> 8 ГБ <br/>

<b>SSD:</b> 256 ГБ<br/>

<b>Монитор:</b> 1920 х 1080 <br/>

## 5. Программное обеспечение:
<b>Операционная система семейства:</b> VirtualBox 6.1.38 - Ubuntu 22.04.01 LTS<br/>

<b>Интерпретатор команд:</b> bash версия 4.4.19<br/>

<b>Система программирования:</b> не использовалась версия —<br/>

<b>Редактор текстов:</b> -

<b>Утилиты операционной системы:</b> -

<b>Прикладные системы и программы:</b> -

<b>Местонахождение и имена файлов программ и данных на домашнем компьютере:</b>

## 6. Идея, метод, алгоритм решения задачи (в формах: словесной, псевдокода, графической [блок-схема, диаграмма, рисунок, таблица] или формальные спецификации с пред- и постусловиями)
| qdb |  Описание |
| ------ | ------ | 
| help | подсказка по разделу помощи отладчика. help без параметров выводит список разделов |
| list | распечатка текста функции/процедуры/файла или всей программы, начиная с указанной строки. По умолчанию рассчитываются следующие 10 строк программы. Распечатываемый файл становится текущим файлом исходного текста отлаживаемой программы |
| break | задание точки останова на указанной строке/функции текущего исходного файла программы | 
| run | запуск программы на выполнение | 
| set args | предварительная установка параметров командной строки | 
| print | печать значения выражения, которое может включать и переменные, и вызовы функций программы | 
| next |  выполнение очередной строки программы при пошаговой трассировке (процедуры и функкии нс трассируются, а выполняются за один такт). Необязательный параметр n указывает число строк программы для выполнения (по умолчанию — 1)  |  
| step | выполнение очередной строки программы (с трассировкой вызовов функций/процедур). Перед выполнением next/step программа должна быть запущена командой run | 
| set var | присваивание значения переменной | 
| ptype | распечатка определения типа переменной (на языке программирования) | 
| backtrace или bt | распечатка содержимого стека вызовов |  
| continue | продолжение выполнения программы после остановки | 
| quit | выход из отладчика | 

## 7. Сценарий выполнения работы [план работы, первоначальный текст программы в черновике (можно на отдельном листе) и тесты либо соображения по тестированию].
Ставим точку останова (breakpoint) на 53 строке и смотрим, что программа выводит на каждом шаге.

Пункты 1-7 отчета составляются сторого до начала лабораторной работы.
Допущен к выполнению работы.  
<b>Подпись преподавателя</b> ________________

### **8. Распечатка протокола**:
```
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~$ cd Загрузки
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ gcc -g -std=c18 laba9.c
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ gdb ./a.out
GNU gdb (Ubuntu 9.2-0ubuntu1~20.04.1) 9.2
Copyright (C) 2020 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<http://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from ./a.out...
(gdb) b 53
Breakpoint 1 at 0x1245: file laba9.c, line 53.
(gdb) run
Starting program: /home/demagog/Загрузки/a.out

Breakpoint 1, main () at laba9.c:53
(gdb) cont
Continuing.

Breakpoint 1, main () at laba9.c:53
(gdb) next
(gdb) next
(gdb) bt
#0  main () at laba9.c:58
(gdb) print l
$1 = 8
(gdb) print i
$2 = -16
(gdb) print j
$3 = -5
(gdb) print index
$4 = 1
(gdb) cont
Continuing.

Breakpoint 1, main () at laba9.c:53
...
(gdb) cont
Continuing.
[Inferior 1 (process 8856) exited normally]
(gdb) quit 
```

## 9. Дневник отладки должен содержать дату и время сеансов отладки и основные события (ошибки в сценарии и программе, нестандартные ситуации) и краткие комментарии к ним. В дневнике отладки приводятся сведения об использовании других ЭВМ, существенном участии преподавателя и других лиц в написании и отладке программы.

| № |  Лаб. или дом. | Дата | Время | Событие | Действие по исправлению | Примечание |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 1 | дом. | 16.11.22 | 13:00 | Выполнение лабораторной работы | - | - |

## 10. Замечания автора:

```
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ gcc -g -std=c18 zlaba9.c -lm
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ gdb ./a.out
GNU gdb (Ubuntu 9.2-0ubuntu1~20.04.1) 9.2
Copyright (C) 2020 Free Software Foundation, Inc.
License GPLv3+: GNU GPL version 3 or later <http://gnu.org/licenses/gpl.html>
This is free software: you are free to change and redistribute it.
There is NO WARRANTY, to the extent permitted by law.
Type "show copying" and "show warranty" for details.
This GDB was configured as "x86_64-linux-gnu".
Type "show configuration" for configuration details.
For bug reporting instructions, please see:
<http://www.gnu.org/software/gdb/bugs/>.
Find the GDB manual and other documentation resources online at:
    <http://www.gnu.org/software/gdb/documentation/>.

For help, type "help".
Type "apropos word" to search for commands related to "word"...
Reading symbols from ./a.out...
(gdb) b 48 if index == 4
Breakpoint 1 at 0x163e: file zlaba9.c, line 48.
(gdb) run
Starting program: /home/demagog/Загрузки/a.out 

Breakpoint 1, change (pt=0x7fffffffdf40, index=4) at zlaba9.c:48
48	    int i = pt->i, j = pt->j, l = pt->l;
(gdb) print index
$1 = 4
(gdb) list
43	       && ((pt.j - penta.y) - tan(((double)72 * pi) / 180) * (pt.i - penta.x) + penta.r * sqrt(tan(((double)72 * pi) / 180) * tan(((double)72 * pi) / 180) + 1) >= 0)
44	        && ((pt.j - penta.y) + penta.r >= 0));
45	}
46	
47	void change(struct state* pt, int index){
48	    int i = pt->i, j = pt->j, l = pt->l;
49	    pt->i = mod((abs(i - j) * l - abs(j - l) * i + abs(i - l) * j), 20) - index;
50	    pt->j = mod((min(i, j) * max(j, l) * min(i, l)), 25) + 5 * sign(i - l);
51	    pt->l = abs(l) * sign(i - j) - abs(i) * sign(j - l) + abs(j) * sign(i - l); 
52	}
(gdb) quit
A debugging session is active.

	Inferior 1 [process 51767] will be killed.

Quit anyway? (y or n) y
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ 
```

## 11. Выводы:
В ходе работы были получены навыки работы с отладчиком системы программирования на языке Си.

Недочёты при выполнении задания могут быть устранены следующим образом: —

<b>Подпись студента:</b> ____________________
