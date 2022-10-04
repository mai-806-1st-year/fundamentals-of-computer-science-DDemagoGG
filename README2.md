# Отчёт по лабораторной работе №2 по курсу “Фундаментальная информатика”

<b>Студент группы:</b> <ins>М80-108Б-22 Формалёв Александр Сергеевич, № по списку 21</ins> 

<b>Контакты e-mail:</b> <ins>lyadiez@mail.ru</ins>

<b>Работа выполнена:</b> «26» <ins>сентября</ins> <ins>2022</ins> г.

<b>Преподаватель:</b> <ins>асп. каф. 806 Сахарин Никита Александрович</ins>

<b>Входной контроль знаний с оценкой:</b> <ins></ins>

<b>Отчет сдан</b> «1» <ins>октября</ins> <ins>2022</ins> г., <b>итоговая оценка</b> <ins></ins>

<b>Подпись преподавателя:</b> ________________

## 1. Тема
Операционная среда OC UNIX
## 2. Цель работы
Изучение и освоение программного обеспечения ОС UNIX и приобретение навыков, необходимых для выполнения курсовых и лабораторных работ в среде UNIX.
## 3. Задание (вариант № —)
Изучение команд и утилит bash.
## 4. Оборудование:
<b>Процессор:</b> AMD A9-9425 RADEON R5, 5 COMPUTE CORES 2C+3G 3.10 GHz <br/>
<b>ОП:</b> 8 ГБ <br/>
<b>SSD:</b> 256 ГБ<br/>
<b>Монитор:</b> 1920 х 1080 <br/>
## 5. Программное обеспечение:
<b>Операционная система семейства:</b> VirtualBox 6.1.38 - Ubuntu 22.04.01 LTS<br/>
<b>Интерпретатор команд:</b> bash версия 4.4.19<br/>
<b>Система программирования:</b> не использовалась версия —<br/>
<b>Редактор текстов:</b> emacs версия 25.2.2<br/>
<b>Утилиты операционной системы:</b> gnuplot <br/>
<b>Прикладные системы и программы:</b> <br/>
<b>Местонахождение и имена файлов программ и данных на домашнем компьютере:</b><br/>
## 6. Идея, метод, алгоритм решения задачи (в формах: словесной, псевдокода, графической [блок-схема, диаграмма, рисунок, таблица] или формальные спецификации с пред- и постусловиями)
Изучить основы программного обеспечения ОС UNIX
Ввод команд:
1. ```ls -l/-A/-lAF``` – просмотр содержимого директории
2. ```whoami``` – определение имени пользователя
3. ```hostname``` – определение терминала, котором ведётся работа
4. ```date``` – определение даты
5. ```tty``` – определение номера группы имени пользователя
6. ```uname -a``` – определение сетевого имени машины
7. ```finger username``` – отображение полного имени и другой информации о пользователе
8. ```pwd``` – отображение полного пути к текущей директории
9. ```sudo ruptime``` – узнать, какие узлы сети в настоящий момент доступны, а какие нет
10. ```sudo rwho``` – узнать, какие пользователи работают на всех доступных UNIX-машинах
11. ```uptime``` – показывает текущее время, время работы после загрузки, количество  текущих пользователей и  нагрузку за последние 1, 5, 15 минут
12. ```man``` – получение оперативной документации по командам UNIX
13. ```cd``` – переход в другую директорию
14. ```ps``` - процессор
15. ```emacs``` – вызов текстового редакторф
16. ```cp``` – копирование
17. ```cat``` – создание нового файла с возможностью записи/копирования, просмотр содержимого файла
18. ```touch``` – создание пустого файла, если его нет. Если файл есть, то команда установит дату обращения в текущий момент времени 
19. ```rm``` – удаление
20. ```mv``` – перемещение
21. ```mkdir``` – создание директории
22. ```rmdir``` – удаление директории
23. ```gnuplot``` – утилита графики для построения двух- и трехмерных графиков
24. ```exit``` – выход

## 7. Сценарий выполнения работы [план работы, первоначальный текст программы в черновике (можно на отдельном листе) и тесты либо соображения по тестированию]. 
- Изучить литературу по OC UNIX
- Просмотреть демонстрационный материал в лабораторной аудитории
- Приобрести основные навыки работы в OC UNIX
- Освоить навигацию в иерархической файловой системе OC UNIX
- Научиться манипулировать с файлами 
- Ознакомиться с утилитой графики 
- Научиться писать и запускать скрипты
- Запротоколировать сеанс

Пункты 1-7 отчета составляются сторого до начала лабораторной работы.
Допущен к выполнению работы.  
<b>Подпись преподавателя</b> ________________
## 8. Распечатка протокола 
```
demaggog@demaggog-VirtualBox:~$ ls
 f1.txt~   snap             Видео       Изображения    'Рабочий стол'
 gnuplot   test-directory   Документы   Музыка          Шаблоны
 set       trange           Загрузки    Общедоступные
demaggog@demaggog-VirtualBox:~$ ls -l
итого 44
-rw-rw-r-- 1 demaggog demaggog   25 сен 26 20:09  f1.txt~
-rw-rw-r-- 1 demaggog demaggog    0 сен 26 20:42  gnuplot
-rw-rw-r-- 1 demaggog demaggog    0 сен 26 20:39  set
drwx------ 3 demaggog demaggog 4096 сен 10 23:27  snap
drwxrwxr-x 2 demaggog demaggog 4096 сен 22 11:10  test-directory
-rw-rw-r-- 1 demaggog demaggog    0 сен 26 20:38  trange
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Видео
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Документы
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Загрузки
drwxr-xr-x 3 demaggog demaggog 4096 сен 26 19:54  Изображения
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Музыка
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Общедоступные
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21 'Рабочий стол'
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Шаблоны
demaggog@demaggog-VirtualBox:~$ ls -a
 .               f1.txt~            set                         Документы
 ..              .gnupg             snap                        Загрузки
 .bash_history   gnuplot            .ssh                        Изображения
 .bash_logout    .gnuplot_history   .sudo_as_admin_successful   Музыка
 .bashrc         .lesshst           test-directory              Общедоступные
 .cache          .local             trange                     'Рабочий стол'
 .config         .profile           Видео                       Шаблоны
demaggog@demaggog-VirtualBox:~$ ls -F
 f1.txt~   snap/             Видео/       Изображения/    'Рабочий стол'/
 gnuplot   test-directory/   Документы/   Музыка/          Шаблоны/
 set       trange            Загрузки/    Общедоступные/
demaggog@demaggog-VirtualBox:~$ ls -laF
итого 96
drwxr-x--- 17 demaggog demaggog 4096 сен 26 20:42  ./
drwxr-xr-x  3 root     root     4096 сен 10 13:28  ../
-rw-------  1 demaggog demaggog   97 сен 22 11:18  .bash_history
-rw-r--r--  1 demaggog demaggog  220 сен 10 13:28  .bash_logout
-rw-r--r--  1 demaggog demaggog 3771 сен 10 13:28  .bashrc
drwx------ 11 demaggog demaggog 4096 сен 26 20:35  .cache/
drwx------ 13 demaggog demaggog 4096 сен 26 20:10  .config/
-rw-rw-r--  1 demaggog demaggog   25 сен 26 20:09  f1.txt~
drwx------  2 demaggog demaggog 4096 сен 22 11:09  .gnupg/
-rw-rw-r--  1 demaggog demaggog    0 сен 26 20:42  gnuplot
-rw-------  1 demaggog demaggog  811 сен 26 21:15  .gnuplot_history
-rw-------  1 demaggog demaggog   20 сен 26 20:16  .lesshst
drwx------  3 demaggog demaggog 4096 сен 10 23:21  .local/
-rw-r--r--  1 demaggog demaggog  807 сен 10 13:28  .profile
-rw-rw-r--  1 demaggog demaggog    0 сен 26 20:39  set
drwx------  3 demaggog demaggog 4096 сен 10 23:27  snap/
drwxrwxr-x  2 demaggog demaggog 4096 сен 17 10:59  .ssh/
-rw-r--r--  1 demaggog demaggog    0 сен 17 09:59  .sudo_as_admin_successful
drwxrwxr-x  2 demaggog demaggog 4096 сен 22 11:10  test-directory/
-rw-rw-r--  1 demaggog demaggog    0 сен 26 20:38  trange
drwxr-xr-x  2 demaggog demaggog 4096 сен 10 23:21  Видео/
drwxr-xr-x  2 demaggog demaggog 4096 сен 10 23:21  Документы/
drwxr-xr-x  2 demaggog demaggog 4096 сен 10 23:21  Загрузки/
drwxr-xr-x  3 demaggog demaggog 4096 сен 26 19:54  Изображения/
drwxr-xr-x  2 demaggog demaggog 4096 сен 10 23:21  Музыка/
drwxr-xr-x  2 demaggog demaggog 4096 сен 10 23:21  Общедоступные/
drwxr-xr-x  2 demaggog demaggog 4096 сен 10 23:21 'Рабочий стол'/
drwxr-xr-x  2 demaggog demaggog 4096 сен 10 23:21  Шаблоны/
demaggog@demaggog-VirtualBox:~$ whoami
demaggog
demaggog@demaggog-VirtualBox:~$ hostname
demaggog-VirtualBox
demaggog@demaggog-VirtualBox:~$ date
Пн 26 сен 2022 21:21:13 MSK
demaggog@demaggog-VirtualBox:~$ tty
/dev/pts/0
demaggog@demaggog-VirtualBox:~$ uname -a
Linux demaggog-VirtualBox 5.15.0-43-generic #46-Ubuntu SMP Tue Jul 12 10:30:17 UTC 2022 x86_64 x86_64 x86_64 GNU/Linux
demaggog@demaggog-VirtualBox:~$ finger demaggog
Login: demaggog       			Name: demaggog
Directory: /home/demaggog           	Shell: /bin/bash
On since Mon Sep 26 19:33 (MSK) on tty2 from tty2
   1 hour 48 minutes idle
No mail.
No Plan.
demaggog@demaggog-VirtualBox:~$ pwd
/home/demaggog
demaggog@demaggog-VirtualBox:~$ sudo ruptime
demaggog-Vir  up       1:51,     1 user,   load 0.52, 0.17, 0.11
demaggog@demaggog-VirtualBox:~$ sudo rwho
demaggog demaggog-VirtualBox:pts/1 Sep 26 21:22
demaggog@demaggog-VirtualBox:~$ uptime
 21:23:21 up  1:51,  1 user,  load average: 0,28, 0,17, 0,12
demaggog@demaggog-VirtualBox:~$ man ls
demaggog@demaggog-VirtualBox:~$ 
demaggog@demaggog-VirtualBox:~$ cd /
demaggog@demaggog-VirtualBox:/$ ls
bin    dev     home   lib64       media  proc  sbin  swapfile  usr
boot   etc     lib    libx32      mnt    root  snap  sys       var
qwerty                                                                         
12345                                                              
                                                                               
^X   INS  f1.txt                                              1:1  altH=help Em
demaggog@demaggog-VirtualBox:~$ cp f1.txt f2.txt
demaggog@demaggog-VirtualBox:~$ ls
 f1.txt    gnuplot   test-directory   Документы     Музыка          Шаблоны
 f1.txt~   set       trange           Загрузки      Общедоступные
 f2.txt    snap      Видео            Изображения  'Рабочий стол'
demaggog@demaggog-VirtualBox:~$ 
demaggog@demaggog-VirtualBox:~$ cat f2.txt
qwerty
12345
demaggog@demaggog-VirtualBox:~$ cat f1.txt f2.txt > f3.txt
demaggog@demaggog-VirtualBox:~$ ls
 f1.txt    gnuplot          trange      Изображения     Шаблоны
 f1.txt~   set              Видео       Музыка
 f2.txt    snap             Документы   Общедоступные
 f3.txt    test-directory   Загрузки   'Рабочий стол'
demaggog@demaggog-VirtualBox:~$ cat f3.txt
qwerty
12345
qwerty
12345
demaggog@demaggog-VirtualBox:~$ rm f2.txt
demaggog@demaggog-VirtualBox:~$ rm f3.txt
demaggog@demaggog-VirtualBox:~$ ls
 f1.txt    set              trange      Загрузки      Общедоступные
 f1.txt~   snap             Видео       Изображения  'Рабочий стол'
 gnuplot   test-directory   Документы   Музыка        Шаблоны
demaggog@demaggog-VirtualBox:~$ mkdir course
demaggog@demaggog-VirtualBox:~$ mkdir lab
demaggog@demaggog-VirtualBox:~$ ls -l
итого 56
drwxrwxr-x 2 demaggog demaggog 4096 сен 26 21:33  course
-rw-rw-r-- 1 demaggog demaggog   13 сен 26 21:29  f1.txt
-rw-rw-r-- 1 demaggog demaggog   25 сен 26 20:09  f1.txt~
-rw-rw-r-- 1 demaggog demaggog    0 сен 26 20:42  gnuplot
drwxrwxr-x 2 demaggog demaggog 4096 сен 26 21:33  lab
-rw-rw-r-- 1 demaggog demaggog    0 сен 26 20:39  set
drwx------ 3 demaggog demaggog 4096 сен 10 23:27  snap
drwxrwxr-x 2 demaggog demaggog 4096 сен 22 11:10  test-directory
-rw-rw-r-- 1 demaggog demaggog    0 сен 26 20:38  trange
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Видео
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Документы
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Загрузки
drwxr-xr-x 3 demaggog demaggog 4096 сен 26 19:54  Изображения
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Музыка
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Общедоступные
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21 'Рабочий стол'
drwxr-xr-x 2 demaggog demaggog 4096 сен 10 23:21  Шаблоны
demaggog@demaggog-VirtualBox:~$ cp f1.txt course
demaggog@demaggog-VirtualBox:~$ cp f1.txt lab
demaggog@demaggog-VirtualBox:~$ ls
 course    lab              trange      Изображения     Шаблоны
 f1.txt    set              Видео       Музыка
 f1.txt~   snap             Документы   Общедоступные
 gnuplot   test-directory   Загрузки   'Рабочий стол'
demaggog@demaggog-VirtualBox:~$ cd course
demaggog@demaggog-VirtualBox:~/course$ ls
f1.txt
demaggog@demaggog-VirtualBox:~/course$ cd
demaggog@demaggog-VirtualBox:~$ cd lab
demaggog@demaggog-VirtualBox:~/lab$ ls
f1.txt
demaggog@demaggog-VirtualBox:~/lab$ cd
demaggog@demaggog-VirtualBox:~$ rm course
rm: невозможно удалить 'course': Это каталог
demaggog@demaggog-VirtualBox:~$ rm -R course
demaggog@demaggog-VirtualBox:~$ rm -R lab
demaggog@demaggog-VirtualBox:~$ ls
 f1.txt    set              trange      Загрузки      Общедоступные
 f1.txt~   snap             Видео       Изображения  'Рабочий стол'
 gnuplot   test-directory   Документы   Музыка        Шаблоны
demaggog@demaggog-VirtualBox:~$ rm f1.txt
demaggog@demaggog-VirtualBox:~$ ls
 f1.txt~   snap             Видео       Изображения    'Рабочий стол'
 gnuplot   test-directory   Документы   Музыка          Шаблоны
 set       trange           Загрузки    Общедоступные
demaggog@demaggog-VirtualBox:~$ gnuplot

	G N U P L O T
	Version 5.4 patchlevel 2    last modified 2021-06-01 

	Copyright (C) 1986-1993, 1998, 2004, 2007-2021
	Thomas Williams, Colin Kelley and many others

	gnuplot home:     http://www.gnuplot.info
	faq, bugs, etc:   type "help FAQ"
	immediate help:   type "help"  (plot window: hit 'h')

Terminal type is now 'unknown'
gnuplot> set term dumb

Terminal type is now 'dumb'
Options are 'feed  size 79, 24 aspect 2, 1 mono'
gnuplot> plot sin(x)*cos(x)

                                                                               
  0.5 +--------------------------------------------------------------------+   
      |   * *        * *        **       + **        * *  +      **        |   
  0.4 |-+*  *        * *        **        * *        *i*(x)*cos(*)********-|   
      |  *  *       *  *       *  *       * *        * *        * *       *|   
  0.3 |-+*  *       *  *       *  *       *  *       * *       *   *     +*|   
      |  *  *       *  *      *   *       *  *      *   *      *   *      *|   
  0.2 |-+*   *      *  *      *    *      *  *      *   *      *   *     +*|   
      |  *   *     *    *     *    *     *    *     *   *     *    *      *|   
  0.1 |-*    *     *    *     *    *     *    *     *   *     *    *     +*|   
      | *    *     *    *     *    *     *    *    *     *    *    *      *|   
    0 |-*     *    *    *     *    *     *    *    *     *    *     *    *-|   
      | *     *    *     *    *    *    *     *    *     *    *     *    * |   
 -0.1 |*+     *    *     *    *    *    *     *    *     *    *     *    *-|   
      |*      *    *     *   *      *   *     *    *      *   *     *   *  |   
 -0.2 |*+     *   *      *   *      *   *     *    *      *   *      *  *+-|   
      |*      *   *       *  *      *  *       *   *      *  *       *  *  |   
 -0.3 |*+     *   *       * *       *  *       *  *       *  *       *  *+-|   
      |*       * *        * *        * *       *  *       *  *       *  *  |   
 -0.4 |*+      * *        * *        * *        * *       * *        *  *+-|   
      |         **     +  * *        * * +      **        +**        *  *  |   
 -0.5 +--------------------------------------------------------------------+   
     -10              -5                 0                5                10  
                                                                               
gnuplot> splot sin(x*x+y*y)

                                                                               
                                                                               
                                                                               
                                                     sin(x*x+y*y) *******      
                               **** * **                                       
                         * *****************  *   **  *                        
                     **************************************** * ***            
               ****************************************************            
       1   +*******************************************************            
     0.8   +*******************************************************            
     0.4   +*******************************************************            
    -0 0   +*******************************************************            
    -0.6   +***************************************************   +            
      -1   +-**  **************************************   *       |            
           +-+       ----*  --* **********************---+---     |  10        
           |     ----+---+             **  ***** *      +    -+---+            
        -10| ---+---+                         +          +------               
           +--------++      0                 |     +------                    
                    ------------------+    10 |+------                         
                                     +--------+--                              
                                                                               
                                                                               
                                                                               
                                                                               
gnuplot> set parametric

	dummy variable is t for curves, u/v for surfaces
gnuplot> set trange [0 to 2*pi]
gnuplot> set xrange [-1 to 1]
gnuplot> set yrange [-1 to 1]
gnuplot> plot sin(t),cos(t)

                                                                               
    1 +--------------------------------------------------------------------+   
      |                ******            +          ******+                |   
      |           *****                              sin(t******t) ******* |   
      |        ***                                              ***        |   
      |     ***                                                    ***     |   
  0.5 |-+ **                                                          ** +-|   
      | **                                                              ** |   
      | *                                                                * |   
      |*                                                                  *|   
      |                                                                    |   
    0 |-+                                                                +-|   
      |                                                                    |   
      |*                                                                  *|   
      |**                                                                **|   
      |  **                                                            **  |   
 -0.5 |-+  *                                                          *  +-|   
      |     **                                                      **     |   
      |       *****                                             ****       |   
      |            ****                                     ****           |   
      |                ********          +          ********               |   
   -1 +--------------------------------------------------------------------+   
     -1              -0.5                0               0.5               1   
                                                                               
gnuplot> set zrange [-1 to 1]
gnuplot> set urange [0 to 2*pi]
gnuplot> set vrange [0 to 2*pi]
gnuplot> unset hidden3d
gnuplot> splot sin(u)*sin(v),sin(u)*cos(v),cos(u)

                                                                               
                                                                               
                                                                               
                               sin(u)*sin(v),sin(u)*cos(v),cos(u) *******      
                                                                               
                                                                               
                                 *************                                 
                          ***************************                          
       1   +-+        ***********************************                      
           |        ***************************************                    
     0.5   +-+      *** **********   *   *   ********** ***                    
    -0 0   +-+      ***************************************                    
           +-+          *******************************                        
      -1   |             -+-- + ***************--                              
           +-+       ----   --+                 ++-------+---        1         
           |     ----+---+                              +    -+---+            
         -1| ---+---+                                    +------               
           +--------++      0                       +------                    
                    ------------------+     1  +------                         
                                     +--------+--                              
                                                                               
                                                                               
                                                                               
                                                                               
gnuplot> upset parametric
         ^
         invalid command

gnuplot> unset parametric

	dummy variable is x for curves, x/y for surfaces
gnuplot> exit

```
## 9. Дневник отладки должен содержать дату и время сеансов отладки и основные события (ошибки в сценарии и программе, нестандартные ситуации) и краткие комментарии к ним. В дневнике отладки приводятся сведения об использовании других ЭВМ, существенном участии преподавателя и других лиц в написании и отладке программы.

| № |  Лаб. или дом. | Дата | Время | Событие | Действие по исправлению | Примечание |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
## 10. Замечания автора по существу работы — Написание команд для отработки навыков работы в ОС UNIX.
```

```
## 11. Выводы
 Было изучено и освоено программное обеспечение OC UNIX и приобретены навыки, необходимые для выполнения курсовых и лабораторных работ в среде UNIX.

Недочёты при выполнении задания могут быть устранены следующим образом: —

<b>Подпись студента:</b> ____________________
