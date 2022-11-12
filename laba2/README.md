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
<b>Подпись преподавателя:</b> ________________
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
| 1 | дом. | 26.09.2022 | 14:00 | выполнение лабораторной работы | - | - |
## 10. Замечания автора по существу работы — Написание команд для отработки навыков работы в ОС UNIX.
```
demaggog@demaggog-VirtualBox:~$ ls -lAF
итого 120
-rw-------  1 demaggog demaggog  3383 окт  4 19:40  .bash_history
-rw-r--r--  1 demaggog demaggog   220 сен 10 13:28  .bash_logout
-rw-r--r--  1 demaggog demaggog  3771 сен 10 13:28  .bashrc
drwx------ 11 demaggog demaggog  4096 сен 26 20:35  .cache/
drwx------ 15 demaggog demaggog  4096 окт  1 10:07  .config/
-rw-rw-r--  1 demaggog demaggog    25 сен 26 20:09  f1.txt~
drwx------  2 demaggog demaggog  4096 окт  4 19:30  .gnupg/
-rw-rw-r--  1 demaggog demaggog     0 сен 26 20:42  gnuplot
-rw-------  1 demaggog demaggog  1800 окт  1 11:24  .gnuplot_history
-rw-rw-r--  1 demaggog demaggog 22918 сен 26 22:16  laba.txt
-rw-------  1 demaggog demaggog    20 сен 26 21:23  .lesshst
drwx------  3 demaggog demaggog  4096 сен 10 23:21  .local/
-rw-rw-r--  1 demaggog demaggog  1397 окт  1 11:01  out.txt
-rw-r--r--  1 demaggog demaggog   807 сен 10 13:28  .profile
-rw-rw-r--  1 demaggog demaggog     0 сен 26 21:57  scr
-rw-rw-r--  1 demaggog demaggog     0 сен 26 20:39  set
drwx------  4 demaggog demaggog  4096 сен 26 22:01  snap/
drwxrwxr-x  2 demaggog demaggog  4096 сен 17 10:59  .ssh/
-rw-r--r--  1 demaggog demaggog     0 сен 17 09:59  .sudo_as_admin_successful
drwxrwxr-x  2 demaggog demaggog  4096 сен 22 11:10  test-directory/
-rw-rw-r--  1 demaggog demaggog    18 окт  4 19:40  test.txt
-rw-rw-r--  1 demaggog demaggog     0 сен 26 20:38  trange
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21  Видео/
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21  Документы/
drwxr-xr-x  2 demaggog demaggog  4096 окт  1 11:28  Загрузки/
drwxrwxrwx  3 demaggog demaggog  4096 сен 26 19:54  Изображения/
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21  Музыка/
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21  Общедоступные/
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21 'Рабочий стол'/
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21  Шаблоны/
demaggog@demaggog-VirtualBox:~$ chmod ugo+rwx Музыка/
demaggog@demaggog-VirtualBox:~$ ls -lAF
итого 120
-rw-------  1 demaggog demaggog  3383 окт  4 19:40  .bash_history
-rw-r--r--  1 demaggog demaggog   220 сен 10 13:28  .bash_logout
-rw-r--r--  1 demaggog demaggog  3771 сен 10 13:28  .bashrc
drwx------ 11 demaggog demaggog  4096 сен 26 20:35  .cache/
drwx------ 15 demaggog demaggog  4096 окт  1 10:07  .config/
-rw-rw-r--  1 demaggog demaggog    25 сен 26 20:09  f1.txt~
drwx------  2 demaggog demaggog  4096 окт  4 19:30  .gnupg/
-rw-rw-r--  1 demaggog demaggog     0 сен 26 20:42  gnuplot
-rw-------  1 demaggog demaggog  1800 окт  1 11:24  .gnuplot_history
-rw-rw-r--  1 demaggog demaggog 22918 сен 26 22:16  laba.txt
-rw-------  1 demaggog demaggog    20 сен 26 21:23  .lesshst
drwx------  3 demaggog demaggog  4096 сен 10 23:21  .local/
-rw-rw-r--  1 demaggog demaggog  1397 окт  1 11:01  out.txt
-rw-r--r--  1 demaggog demaggog   807 сен 10 13:28  .profile
-rw-rw-r--  1 demaggog demaggog     0 сен 26 21:57  scr
-rw-rw-r--  1 demaggog demaggog     0 сен 26 20:39  set
drwx------  4 demaggog demaggog  4096 сен 26 22:01  snap/
drwxrwxr-x  2 demaggog demaggog  4096 сен 17 10:59  .ssh/
-rw-r--r--  1 demaggog demaggog     0 сен 17 09:59  .sudo_as_admin_successful
drwxrwxr-x  2 demaggog demaggog  4096 сен 22 11:10  test-directory/
-rw-rw-r--  1 demaggog demaggog    18 окт  4 19:40  test.txt
-rw-rw-r--  1 demaggog demaggog     0 сен 26 20:38  trange
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21  Видео/
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21  Документы/
drwxr-xr-x  2 demaggog demaggog  4096 окт  1 11:28  Загрузки/
drwxrwxrwx  3 demaggog demaggog  4096 сен 26 19:54  Изображения/
drwxrwxrwx  2 demaggog demaggog  4096 сен 10 23:21  Музыка/
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21  Общедоступные/
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21 'Рабочий стол'/
drwxr-xr-x  2 demaggog demaggog  4096 сен 10 23:21  Шаблоны/
demaggog@demaggog-VirtualBox:~$ ps
    PID TTY          TIME CMD
  24224 pts/0    00:00:00 bash
  24972 pts/0    00:00:00 ps
demaggog@demaggog-VirtualBox:~$ ps -A
    PID TTY          TIME CMD
      1 ?        00:00:12 systemd
      2 ?        00:00:00 kthreadd
      3 ?        00:00:00 rcu_gp
      4 ?        00:00:00 rcu_par_gp
      5 ?        00:00:00 netns
      7 ?        00:00:00 kworker/0:0H-events_highpri
      9 ?        00:02:50 kworker/0:1H-kblockd
     10 ?        00:00:00 mm_percpu_wq
     11 ?        00:00:00 rcu_tasks_rude_
     12 ?        00:00:00 rcu_tasks_trace
     13 ?        00:00:50 ksoftirqd/0
     14 ?        00:00:10 rcu_sched
     15 ?        00:00:00 migration/0
     16 ?        00:00:00 idle_inject/0
     18 ?        00:00:00 cpuhp/0
     19 ?        00:00:00 kdevtmpfs
     20 ?        00:00:00 inet_frag_wq
     21 ?        00:00:00 kauditd
     22 ?        00:00:00 khungtaskd
     23 ?        00:00:00 oom_reaper
     24 ?        00:00:00 writeback
     25 ?        00:00:05 kcompactd0
     26 ?        00:00:00 ksmd
     27 ?        00:00:00 khugepaged
     73 ?        00:00:00 kintegrityd
     74 ?        00:00:00 kblockd
     75 ?        00:00:00 blkcg_punt_bio
     76 ?        00:00:00 tpm_dev_wq
     77 ?        00:00:00 ata_sff
     78 ?        00:00:00 md
     79 ?        00:00:00 edac-poller
     80 ?        00:00:00 devfreq_wq
     81 ?        00:00:00 watchdogd
     84 ?        00:00:15 kswapd0
     85 ?        00:00:00 ecryptfs-kthrea
     87 ?        00:00:00 kthrotld
     88 ?        00:00:00 acpi_thermal_pm
     90 ?        00:00:00 scsi_eh_0
     91 ?        00:00:00 scsi_tmf_0
     92 ?        00:00:00 scsi_eh_1
     93 ?        00:00:00 scsi_tmf_1
     95 ?        00:00:00 vfio-irqfd-clea
     96 ?        00:00:00 mld
     97 ?        00:00:00 ipv6_addrconf
    109 ?        00:00:00 kstrp
    112 ?        00:00:00 zswap-shrink
    113 ?        00:00:00 kworker/u3:0
    118 ?        00:00:00 charger_manager
    157 ?        00:00:00 scsi_eh_2
    158 ?        00:00:00 scsi_tmf_2
    182 ?        00:00:14 jbd2/sda3-8
    183 ?        00:00:00 ext4-rsv-conver
    223 ?        00:00:04 systemd-journal
    246 ?        00:00:00 kworker/0:3-cgroup_destroy
    252 ?        00:00:00 ipmi-msghandler
    275 ?        00:00:00 systemd-udevd
    334 ?        00:00:00 ttm_swap
    335 ?        00:00:00 irq/18-vmwgfx
    336 ?        00:00:00 card0-crtc0
    337 ?        00:00:00 card0-crtc1
    338 ?        00:00:00 card0-crtc2
    339 ?        00:00:00 card0-crtc3
    340 ?        00:00:00 card0-crtc4
    341 ?        00:00:00 card0-crtc5
    342 ?        00:00:00 card0-crtc6
    343 ?        00:00:00 card0-crtc7
    405 ?        00:00:17 systemd-oomd
    406 ?        00:00:03 systemd-resolve
    408 ?        00:00:00 systemd-timesyn
    552 ?        00:00:00 accounts-daemon
    555 ?        00:00:00 acpid
    560 ?        00:00:00 avahi-daemon
    563 ?        00:00:00 cron
    565 ?        00:00:03 dbus-daemon
    569 ?        00:00:02 NetworkManager
    581 ?        00:00:00 networkd-dispat
    585 ?        00:00:01 polkitd
    588 ?        00:00:00 power-profiles-
    590 ?        00:00:00 rsyslogd
    597 ?        00:00:00 switcheroo-cont
    603 ?        00:00:00 systemd-logind
    605 ?        00:00:01 udisksd
    608 ?        00:00:00 wpa_supplicant
    622 ?        00:00:00 avahi-daemon
    664 ?        00:00:00 ModemManager
    681 ?        00:00:00 cupsd
    698 ?        00:00:00 unattended-upgr
    726 ?        00:00:00 sshd
    740 ?        00:00:00 gdm3
    749 ?        00:00:00 gdm-session-wor
    780 ?        00:00:00 cups-browsed
    795 ?        00:00:00 kerneloops
    797 ?        00:00:00 kerneloops
    798 ?        00:00:00 rwhod
    799 ?        00:00:00 rwhod
    814 ?        00:00:03 systemd
    817 ?        00:00:00 (sd-pam)
    824 ?        00:00:00 pipewire
    826 ?        00:00:00 pipewire-media-
    827 ?        00:00:05 pulseaudio
    828 ?        00:00:00 rtkit-daemon
    830 ?        00:00:00 gnome-keyring-d
    838 tty2     00:00:00 gdm-wayland-ses
    841 ?        00:00:03 dbus-daemon
    847 tty2     00:00:00 gnome-session-b
    866 ?        00:00:00 gvfsd
    886 ?        00:00:00 gvfsd-fuse
    926 ?        00:00:00 gnome-session-c
    939 ?        00:00:00 gnome-session-b
    969 ?        00:00:00 at-spi-bus-laun
    973 ?        00:04:26 gnome-shell
    980 ?        00:00:00 dbus-daemon
   1006 ?        00:00:00 xdg-document-po
   1009 ?        00:00:00 xdg-permission-
   1019 ?        00:00:00 fusermount3
   1094 ?        00:00:01 snapd-desktop-i
   1154 ?        00:00:00 xdg-desktop-por
   1158 ?        00:00:01 xdg-desktop-por
   1167 ?        00:00:00 gnome-shell-cal
   1174 ?        00:00:00 evolution-sourc
   1178 ?        00:00:01 upowerd
   1182 ?        00:00:01 goa-daemon
   1190 ?        00:00:00 evolution-calen
   1193 ?        00:00:00 gvfs-udisks2-vo
   1201 ?        00:00:01 gvfs-afc-volume
   1206 ?        00:00:00 gvfs-mtp-volume
   1212 ?        00:00:00 gvfs-goa-volume
   1218 ?        00:00:00 dconf-service
   1224 ?        00:00:00 evolution-addre
   1238 ?        00:00:00 goa-identity-se
   1243 ?        00:00:00 gvfs-gphoto2-vo
   1251 ?        00:00:00 packagekitd
   1258 ?        00:00:00 gvfsd-trash
   1268 ?        00:00:00 at-spi2-registr
   1270 ?        00:00:00 gjs
   1278 ?        00:00:00 sh
   1279 ?        00:00:00 gsd-a11y-settin
   1280 ?        00:00:00 gsd-color
   1282 ?        00:00:00 gsd-datetime
   1284 ?        00:00:03 ibus-daemon
   1285 ?        00:00:00 gsd-housekeepin
   1290 ?        00:00:00 gsd-keyboard
   1296 ?        00:00:00 gsd-media-keys
   1299 ?        00:00:00 gsd-power
   1303 ?        00:00:00 gsd-print-notif
   1306 ?        00:00:00 gsd-rfkill
   1310 ?        00:00:00 gsd-screensaver
   1313 ?        00:00:00 gsd-sharing
   1319 ?        00:00:00 gsd-smartcard
   1324 ?        00:00:00 gsd-sound
   1326 ?        00:00:00 gsd-wacom
   1357 ?        00:00:00 ibus-memconf
   1360 ?        00:00:05 ibus-extension-
   1361 ?        00:00:01 evolution-alarm
   1371 ?        00:00:00 ibus-portal
   1379 ?        00:00:00 gsd-disk-utilit
   1402 ?        00:00:00 gsd-printer
   1445 ?        00:00:00 ibus-engine-sim
   1465 ?        00:00:00 gvfsd-metadata
   1493 ?        00:00:00 xdg-desktop-por
   1508 ?        00:00:00 colord
   1513 ?        00:00:12 tracker-miner-f
   1581 ?        00:00:00 gjs
   1701 ?        00:00:01 update-notifier
   1740 ?        00:00:49 snapd
  18647 ?        00:00:19 kworker/u2:2-ext4-rsv-conversion
  21400 ?        00:00:14 kworker/u2:0-events_unbound
  22173 ?        00:00:06 gjs
  22245 ?        00:00:05 kworker/0:1-events
  22580 ?        00:00:01 gnome-calendar
  22584 ?        00:00:00 seahorse
  23257 ?        00:00:12 kworker/u2:3-events_unbound
  23258 ?        00:00:03 kworker/u2:4-ext4-rsv-conversion
  23377 ?        00:00:06 Xwayland
  23382 ?        00:00:01 gsd-xsettings
  23434 ?        00:00:00 ibus-x11
  23667 ?        00:00:00 snap
  24122 ?        00:00:00 kworker/0:0-events
  24155 ?        00:00:02 gnome-terminal-
  24224 pts/0    00:00:00 bash
  24234 ?        00:00:16 firefox
  24347 ?        00:00:00 Socket Process
  24365 ?        00:00:02 Privileged Cont
  24520 ?        00:00:01 WebExtensions
  24665 ?        00:00:00 Web Content
  24912 ?        00:00:00 Web Content
  24918 ?        00:00:00 Web Content
  24973 pts/0    00:00:00 ps
demaggog@demaggog-VirtualBox:~$ ps aux | grep firefox
demaggog   24234 12.4  9.5 2806044 288388 ?      Sl   19:40   0:16 /snap/firefox/1918/usr/lib/firefox/firefox
demaggog   24347  0.3  1.3 220176 39448 ?        Sl   19:41   0:00 /snap/firefox/1918/usr/lib/firefox/firefox -contentproc -parentBuildID 20221003201138 -prefsLen 25179 -prefMapSize 226994 -appDir /snap/firefox/1918/usr/lib/firefox/browser {e01653f6-5f14-4b96-ae25-ce14d6841c6f} 24234 true socket
demaggog   24365  1.7  3.5 2427628 106612 ?      Sl   19:41   0:02 /snap/firefox/1918/usr/lib/firefox/firefox -contentproc -childID 1 -isForBrowser -prefsLen 25320 -prefMapSize 226994 -jsInitLen 246848 -parentBuildID 20221003201138 -appDir /snap/firefox/1918/usr/lib/firefox/browser {fd3c847d-e93d-4254-83ef-884f833e73ab} 24234 true tab
demaggog   24520  1.5  2.9 2429220 88516 ?       Sl   19:41   0:01 /snap/firefox/1918/usr/lib/firefox/firefox -contentproc -childID 2 -isForBrowser -prefsLen 29941 -prefMapSize 226994 -jsInitLen 246848 -parentBuildID 20221003201138 -appDir /snap/firefox/1918/usr/lib/firefox/browser {ead66b7b-b42e-489e-ab26-29cd88da3322} 24234 true tab
demaggog   24665  0.4  2.0 2401188 60716 ?       Sl   19:41   0:00 /snap/firefox/1918/usr/lib/firefox/firefox -contentproc -childID 3 -isForBrowser -prefsLen 30721 -prefMapSize 226994 -jsInitLen 246848 -parentBuildID 20221003201138 -appDir /snap/firefox/1918/usr/lib/firefox/browser {7f139bc7-7474-4c3f-9ef3-6c47f0560ebf} 24234 true tab
demaggog   24912  0.3  2.0 2401728 63388 ?       Sl   19:41   0:00 /snap/firefox/1918/usr/lib/firefox/firefox -contentproc -childID 4 -isForBrowser -prefsLen 30721 -prefMapSize 226994 -jsInitLen 246848 -parentBuildID 20221003201138 -appDir /snap/firefox/1918/usr/lib/firefox/browser {b23afff3-6246-4694-81d9-c3f7533692e6} 24234 true tab
demaggog   24918  0.4  2.0 2401724 61156 ?       Sl   19:41   0:00 /snap/firefox/1918/usr/lib/firefox/firefox -contentproc -childID 5 -isForBrowser -prefsLen 30721 -prefMapSize 226994 -jsInitLen 246848 -parentBuildID 20221003201138 -appDir /snap/firefox/1918/usr/lib/firefox/browser {a909549b-c3af-47b1-a9d6-2be088ee0242} 24234 true tab
demaggog   24976  0.0  0.0  17756  2400 pts/0    S+   19:43   0:00 grep --color=auto firefox
demaggog@demaggog-VirtualBox:~$ killall firefox
demaggog@demaggog-VirtualBox:~$ ps aux
USER         PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root           1  0.3  0.4 168008 13096 ?        Ss   18:40   0:12 /sbin/init sp
root           2  0.0  0.0      0     0 ?        S    18:40   0:00 [kthreadd]
root           3  0.0  0.0      0     0 ?        I<   18:40   0:00 [rcu_gp]
root           4  0.0  0.0      0     0 ?        I<   18:40   0:00 [rcu_par_gp]
root           5  0.0  0.0      0     0 ?        I<   18:40   0:00 [netns]
root           7  0.0  0.0      0     0 ?        I<   18:40   0:00 [kworker/0:0H
root           9  4.4  0.0      0     0 ?        I<   18:40   2:50 [kworker/0:1H
root          10  0.0  0.0      0     0 ?        I<   18:40   0:00 [mm_percpu_wq
root          11  0.0  0.0      0     0 ?        S    18:40   0:00 [rcu_tasks_ru
root          12  0.0  0.0      0     0 ?        S    18:40   0:00 [rcu_tasks_tr
root          13  1.3  0.0      0     0 ?        S    18:40   0:50 [ksoftirqd/0]
root          14  0.2  0.0      0     0 ?        I    18:40   0:11 [rcu_sched]
root          15  0.0  0.0      0     0 ?        S    18:40   0:00 [migration/0]
root          16  0.0  0.0      0     0 ?        S    18:40   0:00 [idle_inject/
root          18  0.0  0.0      0     0 ?        S    18:40   0:00 [cpuhp/0]
root          19  0.0  0.0      0     0 ?        S    18:40   0:00 [kdevtmpfs]
root          20  0.0  0.0      0     0 ?        I<   18:40   0:00 [inet_frag_wq
root          21  0.0  0.0      0     0 ?        S    18:40   0:00 [kauditd]
root          22  0.0  0.0      0     0 ?        S    18:40   0:00 [khungtaskd]
root          23  0.0  0.0      0     0 ?        S    18:40   0:00 [oom_reaper]
root          24  0.0  0.0      0     0 ?        I<   18:40   0:00 [writeback]
root          25  0.1  0.0      0     0 ?        S    18:40   0:05 [kcompactd0]
root          26  0.0  0.0      0     0 ?        SN   18:40   0:00 [ksmd]
root          27  0.0  0.0      0     0 ?        SN   18:40   0:00 [khugepaged]
root          73  0.0  0.0      0     0 ?        I<   18:40   0:00 [kintegrityd]
root          74  0.0  0.0      0     0 ?        I<   18:40   0:00 [kblockd]
root          75  0.0  0.0      0     0 ?        I<   18:40   0:00 [blkcg_punt_b
root          76  0.0  0.0      0     0 ?        I<   18:40   0:00 [tpm_dev_wq]
root          77  0.0  0.0      0     0 ?        I<   18:40   0:00 [ata_sff]
root          78  0.0  0.0      0     0 ?        I<   18:40   0:00 [md]
root          79  0.0  0.0      0     0 ?        I<   18:40   0:00 [edac-poller]
root          80  0.0  0.0      0     0 ?        I<   18:40   0:00 [devfreq_wq]
root          81  0.0  0.0      0     0 ?        S    18:40   0:00 [watchdogd]
root          84  0.4  0.0      0     0 ?        S    18:40   0:15 [kswapd0]
root          85  0.0  0.0      0     0 ?        S    18:40   0:00 [ecryptfs-kth
root          87  0.0  0.0      0     0 ?        I<   18:40   0:00 [kthrotld]
root          88  0.0  0.0      0     0 ?        I<   18:40   0:00 [acpi_thermal
root          90  0.0  0.0      0     0 ?        S    18:40   0:00 [scsi_eh_0]
root          91  0.0  0.0      0     0 ?        I<   18:40   0:00 [scsi_tmf_0]
root          92  0.0  0.0      0     0 ?        S    18:40   0:00 [scsi_eh_1]
root          93  0.0  0.0      0     0 ?        I<   18:40   0:00 [scsi_tmf_1]
root          95  0.0  0.0      0     0 ?        I<   18:40   0:00 [vfio-irqfd-c
root          96  0.0  0.0      0     0 ?        I<   18:40   0:00 [mld]
root          97  0.0  0.0      0     0 ?        I<   18:40   0:00 [ipv6_addrcon
root         109  0.0  0.0      0     0 ?        I<   18:40   0:00 [kstrp]
root         112  0.0  0.0      0     0 ?        I<   18:40   0:00 [zswap-shrink
root         113  0.0  0.0      0     0 ?        I<   18:40   0:00 [kworker/u3:0
root         118  0.0  0.0      0     0 ?        I<   18:40   0:00 [charger_mana
root         157  0.0  0.0      0     0 ?        S    18:40   0:00 [scsi_eh_2]
root         158  0.0  0.0      0     0 ?        I<   18:40   0:00 [scsi_tmf_2]
root         182  0.3  0.0      0     0 ?        S    18:40   0:14 [jbd2/sda3-8]
root         183  0.0  0.0      0     0 ?        I<   18:40   0:00 [ext4-rsv-con
root         223  0.1  0.5  48220 16292 ?        S<s  18:40   0:04 /lib/systemd/
root         246  0.0  0.0      0     0 ?        I    18:40   0:00 [kworker/0:3-
root         252  0.0  0.0      0     0 ?        I<   18:40   0:00 [ipmi-msghand
root         275  0.0  0.2  26460  6672 ?        Ss   18:40   0:00 /lib/systemd/
root         334  0.0  0.0      0     0 ?        I<   18:40   0:00 [ttm_swap]
root         335  0.0  0.0      0     0 ?        S    18:40   0:00 [irq/18-vmwgf
root         336  0.0  0.0      0     0 ?        S    18:40   0:00 [card0-crtc0]
root         337  0.0  0.0      0     0 ?        S    18:40   0:00 [card0-crtc1]
root         338  0.0  0.0      0     0 ?        S    18:40   0:00 [card0-crtc2]
root         339  0.0  0.0      0     0 ?        S    18:40   0:00 [card0-crtc3]
root         340  0.0  0.0      0     0 ?        S    18:40   0:00 [card0-crtc4]
root         341  0.0  0.0      0     0 ?        S    18:40   0:00 [card0-crtc5]
root         342  0.0  0.0      0     0 ?        S    18:40   0:00 [card0-crtc6]
root         343  0.0  0.0      0     0 ?        S    18:40   0:00 [card0-crtc7]
systemd+     405  0.4  0.2  14824  6180 ?        Ss   18:40   0:17 /lib/systemd/
systemd+     406  0.0  0.4  25396 12796 ?        Ss   18:40   0:03 /lib/systemd/
systemd+     408  0.0  0.2  89376  6564 ?        Ssl  18:40   0:00 /lib/systemd/
root         552  0.0  0.2 249020  7708 ?        Ssl  18:40   0:00 /usr/libexec/
root         555  0.0  0.0   2812  1120 ?        Ss   18:40   0:00 /usr/sbin/acp
avahi        560  0.0  0.1   7624  3368 ?        Ss   18:40   0:00 avahi-daemon:
root         563  0.0  0.0  18148  2984 ?        Ss   18:40   0:00 /usr/sbin/cro
message+     565  0.0  0.1  10112  5936 ?        Ss   18:40   0:03 @dbus-daemon 
root         569  0.0  0.6 344120 18680 ?        Ssl  18:40   0:02 /usr/sbin/Net
root         581  0.0  0.6  49676 20716 ?        Ss   18:40   0:00 /usr/bin/pyth
root         585  0.0  0.3 252344 11036 ?        Ssl  18:40   0:01 /usr/libexec/
root         588  0.0  0.2 249080  6376 ?        Ssl  18:40   0:00 /usr/libexec/
syslog       590  0.0  0.1 222400  4764 ?        Ssl  18:40   0:00 /usr/sbin/rsy
root         597  0.0  0.2 245308  6636 ?        Ssl  18:40   0:00 /usr/libexec/
root         603  0.0  0.2  23628  7696 ?        Ss   18:40   0:00 /lib/systemd/
root         605  0.0  0.4 393036 13196 ?        Ssl  18:40   0:01 /usr/libexec/
root         608  0.0  0.1  16492  5376 ?        Ss   18:40   0:00 /sbin/wpa_sup
avahi        622  0.0  0.0   7440   344 ?        S    18:40   0:00 avahi-daemon:
root         664  0.0  0.3 316936 10800 ?        Ssl  18:40   0:00 /usr/sbin/Mod
root         681  0.0  0.4  81288 13104 ?        Ss   18:40   0:00 /usr/sbin/cup
root         698  0.0  0.7 126800 22820 ?        Ssl  18:40   0:00 /usr/bin/pyth
root         726  0.0  0.2  15424  7516 ?        Ss   18:40   0:00 sshd: /usr/sb
root         740  0.0  0.3 250056  9304 ?        Ssl  18:40   0:00 /usr/sbin/gdm
root         749  0.0  0.3 326944 10996 ?        Sl   18:40   0:00 gdm-session-w
root         780  0.0  0.3 172612 11164 ?        Ssl  18:40   0:00 /usr/sbin/cup
kernoops     795  0.0  0.0  13080   376 ?        Ss   18:40   0:00 /usr/sbin/ker
kernoops     797  0.0  0.0  13080   460 ?        Ss   18:40   0:00 /usr/sbin/ker
rwhod        798  0.0  0.0   2780   112 ?        Ss   18:40   0:00 /usr/sbin/rwh
rwhod        799  0.0  0.0   2780   128 ?        S    18:40   0:00 /usr/sbin/rwh
demaggog     814  0.0  0.3  17964 10528 ?        Ss   18:40   0:03 /lib/systemd/
demaggog     817  0.0  0.0 104276  2204 ?        S    18:40   0:00 (sd-pam)
demaggog     824  0.0  0.2  48220  6440 ?        S<sl 18:41   0:00 /usr/bin/pipe
demaggog     826  0.0  0.2  32108  6224 ?        Ssl  18:41   0:00 /usr/bin/pipe
demaggog     827  0.1  0.8 1693804 26196 ?       S<sl 18:41   0:05 /usr/bin/puls
rtkit        828  0.0  0.0 153992  1524 ?        SNsl 18:41   0:00 /usr/libexec/
demaggog     830  0.0  0.2 249828  6548 ?        SLl  18:41   0:00 /usr/bin/gnom
demaggog     838  0.0  0.2 171256  6152 tty2     Ssl+ 18:41   0:00 /usr/libexec/
demaggog     841  0.0  0.2  11172  6884 ?        Ss   18:41   0:03 /usr/bin/dbus
demaggog     847  0.0  0.4 231900 14204 tty2     Sl+  18:41   0:00 /usr/libexec/
demaggog     866  0.0  0.2 249548  8104 ?        Ssl  18:41   0:00 /usr/libexec/
demaggog     886  0.0  0.2 380884  6488 ?        Sl   18:41   0:00 /usr/libexec/
demaggog     926  0.0  0.1 100556  5028 ?        Ssl  18:41   0:00 /usr/libexec/
demaggog     939  0.0  0.5 668288 17004 ?        Ssl  18:41   0:00 /usr/libexec/
demaggog     969  0.0  0.2 309612  7584 ?        Sl   18:41   0:00 /usr/libexec/
demaggog     973  7.3 13.3 4128056 403724 ?      Rsl  18:41   4:34 /usr/bin/gnom
demaggog     980  0.0  0.1   8560  4180 ?        S    18:41   0:00 /usr/bin/dbus
demaggog    1006  0.0  0.2 546972  7572 ?        Ssl  18:41   0:00 /usr/libexec/
demaggog    1009  0.0  0.1 245188  5192 ?        Ssl  18:41   0:00 /usr/libexec/
root        1019  0.0  0.0   2792   992 ?        Ss   18:41   0:00 fusermount3 -
demaggog    1094  0.0  0.8 457164 26148 ?        Ssl  18:41   0:01 /snap/snapd-d
demaggog    1154  0.0  0.4 632812 13840 ?        Ssl  18:41   0:00 /usr/libexec/
demaggog    1158  0.0  0.8 385220 25652 ?        Ssl  18:41   0:01 /usr/libexec/
demaggog    1167  0.0  0.4 582728 14452 ?        Sl   18:41   0:00 /usr/libexec/
demaggog    1174  0.0  0.7 688116 23992 ?        Ssl  18:41   0:00 /usr/libexec/
root        1178  0.0  0.2 251108  8836 ?        Ssl  18:42   0:01 /usr/libexec/
demaggog    1182  0.0  1.0 570316 30776 ?        Sl   18:42   0:01 /usr/libexec/
demaggog    1190  0.0  0.9 734940 27908 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1193  0.0  0.3 325160  9988 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1201  0.0  0.2 324104  8388 ?        Ssl  18:42   0:01 /usr/libexec/
demaggog    1206  0.0  0.2 245332  6744 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1212  0.0  0.2 245536  6504 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1218  0.0  0.1 156960  6064 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1224  0.0  0.8 681412 27076 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1238  0.0  0.4 347456 13588 ?        Sl   18:42   0:00 /usr/libexec/
demaggog    1243  0.0  0.2 246288  6868 ?        Ssl  18:42   0:00 /usr/libexec/
root        1251  0.0  0.6 307376 20088 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1258  0.0  0.2 323952  8100 ?        Sl   18:42   0:00 /usr/libexec/
demaggog    1268  0.0  0.2 162676  7288 ?        Sl   18:42   0:00 /usr/libexec/
demaggog    1270  0.0  0.7 2608464 23160 ?       Sl   18:42   0:00 /usr/bin/gjs 
demaggog    1278  0.0  0.0   2888   944 ?        Ss   18:42   0:00 sh -c /usr/bi
demaggog    1279  0.0  0.2 319556  6988 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1280  0.0  0.8 608148 25412 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1282  0.0  0.5 384584 15288 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1284  0.0  0.3 250124 11808 ?        Sl   18:42   0:03 /usr/bin/ibus
demaggog    1285  0.0  0.2 321052  7368 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1290  0.0  0.6 350176 20992 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1296  0.0  0.8 726392 25492 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1299  0.0  0.7 460084 24212 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1303  0.0  0.3 258788 11592 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1306  0.0  0.2 466796  6296 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1310  0.0  0.2 245224  6676 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1313  0.0  0.2 474928  8796 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1319  0.0  0.2 395172  8216 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1324  0.0  0.3 328476  9272 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1326  0.0  0.7 424584 21836 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1357  0.0  0.2 172516  7372 ?        Sl   18:42   0:00 /usr/libexec/
demaggog    1360  0.1  0.8 356792 27152 ?        Sl   18:42   0:05 /usr/libexec/
demaggog    1361  0.0  1.9 820328 59828 ?        Sl   18:42   0:01 /usr/libexec/
demaggog    1371  0.0  0.2 246268  7600 ?        Sl   18:42   0:00 /usr/libexec/
demaggog    1379  0.0  0.2 232260  6384 ?        Sl   18:42   0:00 /usr/libexec/
demaggog    1402  0.0  0.4 351296 14176 ?        Sl   18:42   0:00 /usr/libexec/
demaggog    1445  0.0  0.2 172516  7460 ?        Sl   18:42   0:00 /usr/libexec/
demaggog    1465  0.0  0.2 171932  6836 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1493  0.0  0.8 354044 25776 ?        Ssl  18:42   0:00 /usr/libexec/
colord      1508  0.0  0.4 607060 13312 ?        Ssl  18:42   0:00 /usr/libexec/
demaggog    1513  0.3  0.8 726280 26216 ?        SNsl 18:42   0:12 /usr/libexec/
demaggog    1581  0.0  0.7 2608596 23212 ?       Sl   18:42   0:00 /usr/bin/gjs 
demaggog    1701  0.0  1.0 504264 30752 ?        Sl   18:43   0:01 update-notifi
hello, world!                                                                   
123                                                                             
aoaooaoaoa                                                                      
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
                                                                                
   SAVE:  text1.txt                                           3:11  altH=help Em
demaggog@demaggog-VirtualBox:~$ cat text1.txt
hello, world!
123
aoaooaoaoademaggog@demaggog-VirtualBox:~$
```
## 11. Выводы
 Было изучено и освоено программное обеспечение OC UNIX и приобретены навыки, необходимые для выполнения курсовых и лабораторных работ в среде UNIX.

Недочёты при выполнении задания могут быть устранены следующим образом: —

<b>Подпись студента:</b> ____________________
