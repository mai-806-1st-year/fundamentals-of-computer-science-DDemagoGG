# Отчёт по лабораторной работе №2 по курсу “Фундаментальная информатика”

<b>Студент группы:</b> <ins>М80-108Б-22 Формалёв Александр Сергеевич, № по списку 21</ins> 

<b>Контакты e-mail:</b> <ins>lyadiez@mail.ru</ins>

<b>Работа выполнена:</b> «7» <ins>октября</ins> <ins>2022</ins> г.

<b>Преподаватель:</b> <ins>асп. каф. 806 Сахарин Никита Александрович</ins>

<b>Входной контроль знаний с оценкой:</b> <ins></ins>

<b>Отчет сдан</b> «8» <ins>октября</ins> <ins>2022</ins> г., <b>итоговая оценка</b> <ins></ins>

<b>Подпись преподавателя:</b> ________________

## 1. Тема
Сети и телекоммуникации в ОС UNIX
## 2. Цель работы
Изучение и освоение удалённых команд UNIX и приобретение навыков, необходимых для выполнения курсовых и лабораторных работ в среде UNIX.
## 3. Задание (вариант № —)
Изучение удалённых команд.
## 4. Оборудование:
<b>Процессор:</b> AMD A9-9425 RADEON R5, 5 COMPUTE CORES 2C+3G 3.10 GHz <br/>
<b>ОП:</b> 8 ГБ <br/>
<b>SSD:</b> 256 ГБ<br/>
<b>Монитор:</b> 1920 х 1080 <br/>
## 5. Программное обеспечение:
<b>Операционная система семейства:</b> VirtualBox 6.1.38 - Ubuntu 22.04.01 LTS<br/>
<b>Интерпретатор команд:</b> bash версия 4.4.19<br/>
<b>Система программирования:</b> не использовалась версия —<br/>
<b>Редактор текстов:
<b>Утилиты операционной системы:
<b>Прикладные системы и программы:</b> <br/>
<b>Местонахождение и имена файлов программ и данных на домашнем компьютере:</b><br/>
## 6. Идея, метод, алгоритм решения задачи (в формах: словесной, псевдокода, графической [блок-схема, диаграмма, рисунок, таблица] или формальные спецификации с пред- и постусловиями)
Изучить литературу по удалённым командам UNIX. Запустить удалённый сервер. Подключиться к нему. Опробовать команды. Запротоколировать результат. Заполнить отчёт.

## 7. Сценарий выполнения работы [план работы, первоначальный текст программы в черновике (можно на отдельном листе) и тесты либо соображения по тестированию]. 
- Изучить литературу по OC UNIX
- Просмотреть демонстрационный материал в лабораторной аудитории
- Освоить удалённые команды OC UNIX
- Научиться удалённо манипулировать с файлами 
- Запротоколировать сеанс

Пункты 1-7 отчета составляются сторого до начала лабораторной работы.
Допущен к выполнению работы.  
<b>Подпись преподавателя</b> ________________
## 8. Распечатка протокола 
```
demaggog@demaggog-VirtualBox:~$ touch filik.txt
demaggog@demaggog-VirtualBox:~$ ssh u1802296@31.31.196.139
u1802296@31.31.196.139's password: 
-bash-4.2$ ls
file.txt  laba  test.txt
-bash-4.2$ rm file.txt
-bash-4.2$ rm test.txt
-bash-4.2$ rm -r laba
-bash-4.2$ exit
logout
Connection to 31.31.196.139 closed.
demaggog@demaggog-VirtualBox:~$ ls
 filik.txt   snap             Видео         Музыка
 gnuplot     test-directory   Документы     Общедоступные
 scr         text1.txt~       Загрузки     'Рабочий стол'
 set         trange           Изображения   Шаблоны
demaggog@demaggog-VirtualBox:~$ mkdir laba
demaggog@demaggog-VirtualBox:~$ cd laba
demaggog@demaggog-VirtualBox:~/laba$ touch f1.txt
demaggog@demaggog-VirtualBox:~/laba$ touch f2.txt
demaggog@demaggog-VirtualBox:~/laba$ ls
f1.txt  f2.txt
demaggog@demaggog-VirtualBox:~/laba$ cd ..
demaggog@demaggog-VirtualBox:~$ scp /home/demaggog/filik.txt u1802296@31.31.196.139:/var/www/u1802296/data
u1802296@31.31.196.139's password: 
filik.txt                                     100%    0     0.0KB/s   00:00    
demaggog@demaggog-VirtualBox:~$ scp -r /home/demaggog/laba u1802296@31.31.196.139:/var/www/u1802296/data
u1802296@31.31.196.139's password: 
f2.txt                                        100%    0     0.0KB/s   00:00    
f1.txt                                        100%    0     0.0KB/s   00:00    
demaggog@demaggog-VirtualBox:~$ ssh u1802296@31.31.196.139 "ls"
u1802296@31.31.196.139's password: 
filik.txt
laba
demaggog@demaggog-VirtualBox:~$ ssh u1802296@31.31.196.139 "ls ~laba"
u1802296@31.31.196.139's password: 
ls: cannot access ~laba: No such file or directory
demaggog@demaggog-VirtualBox:~$ ssh u1802296@31.31.196.139 "ls ~/laba"
u1802296@31.31.196.139's password: 
f1.txt
f2.txt
demaggog@demaggog-VirtualBox:~$ mkdir arch
demaggog@demaggog-VirtualBox:~$ cd arch
demaggog@demaggog-VirtualBox:~/arch$ touch f3.txt
demaggog@demaggog-VirtualBox:~/arch$ touch f4.txt
demaggog@demaggog-VirtualBox:~/arch$ cd ..
demaggog@demaggog-VirtualBox:~$ tar -cf archive.tar arch
demaggog@demaggog-VirtualBox:~$ ls
 arch          laba   test-directory   Документы     Общедоступные
 archive.tar   scr    text1.txt~       Загрузки     'Рабочий стол'
 filik.txt     set    trange           Изображения   Шаблоны
 gnuplot       snap   Видео            Музыка
demaggog@demaggog-VirtualBox:~$ tar -tvf archive.tar
drwxrwxr-x demaggog/demaggog 0 2022-10-07 17:54 arch/
-rw-rw-r-- demaggog/demaggog 0 2022-10-07 17:54 arch/f4.txt
-rw-rw-r-- demaggog/demaggog 0 2022-10-07 17:54 arch/f3.txt
demaggog@demaggog-VirtualBox:~$ scp /home/demaggog/archive.tar u1802296@31.31.196.139:/var/www/u1802296/data
u1802296@31.31.196.139's password: 
archive.tar                                   100%   10KB 364.0KB/s   00:00    
demaggog@demaggog-VirtualBox:~$ ssh u1802296@31.31.196.139
u1802296@31.31.196.139's password: 
-bash-4.2$ ls
archive.tar  filik.txt  laba
-bash-4.2$ tar -xf archive.tar
-bash-4.2$ ls
arch  archive.tar  filik.txt  laba
-bash-4.2$ cd laba
-bash-4.2$ ls
f1.txt  f2.txt
-bash-4.2$ cat f1.txt
-bash-4.2$ cd ..
-bash-4.2$ cd arch
-bash-4.2$ ls
f3.txt  f4.txt
-bash-4.2$ cd ..
-bash-4.2$ rm filik.txt
-bash-4.2$ ls
arch  archive.tar  laba
-bash-4.2$ rm -r arch
-bash-4.2$ rm -r laba
-bash-4.2$ rm archive.tar
-bash-4.2$ ls
-bash-4.2$ exit
logout
Connection to 31.31.196.139 closed.
demaggog@demaggog-VirtualBox:~$ 
```
## 9. Дневник отладки должен содержать дату и время сеансов отладки и основные события (ошибки в сценарии и программе, нестандартные ситуации) и краткие комментарии к ним. В дневнике отладки приводятся сведения об использовании других ЭВМ, существенном участии преподавателя и других лиц в написании и отладке программы.

| № |  Лаб. или дом. | Дата | Время | Событие | Действие по исправлению | Примечание |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
## 10. Замечания автора по существу работы — Написание команд для отработки навыков работы в ОС UNIX.
```

```
## 11. Выводы
Выяснила, что в OC UNIX есть возможность удалённого подключения к другим машинам. Освоила команды, необходимые для установления соединения и удалённых манипуляций с файлами, а также приобрела навыки, которые помогут выполнять другие лабораторные работы.

Недочёты при выполнении задания могут быть устранены следующим образом: —

<b>Подпись студента:</b> ____________________
