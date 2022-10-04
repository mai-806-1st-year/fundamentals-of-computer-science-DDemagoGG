# Отчёт по лабораторной работе №5 по курсу “Фундаментальная информатика”

<b>Студент группы:</b> <ins>М80-108Б-22 Формалёв Александр Сергеевич, № по списку 21</ins> 

<b>Контакты e-mail:</b> <ins>lyadiez@mail.ru</ins>

<b>Работа выполнена:</b> «30» <ins>сентября</ins> <ins>2022</ins> г.

<b>Преподаватель:</b> <ins>асп. каф. 806 Сахарин Никита Александрович</ins>

<b>Входной контроль знаний с оценкой:</b> <ins></ins>

<b>Отчет сдан</b> «3» <ins>октября</ins> <ins>2022</ins> г., <b>итоговая оценка</b> <ins></ins>

<b>Подпись преподавателя:</b> ________________

## 1. Тема
Программирование машин Тъюринга
## 2. Цель работы
Изучение и освоение навыка программирования машин Тъюринга
## 3. Задание (вариант № 8)
Перевоод числа из восьмеричной СС в двоичную
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
1.	Перейти в начало числа
2.	Удалить первую цифру и перейти в конец числа
3.	Начать построение нового числа через пробел после исходного
    a. Записываем цифру, которую мы удалили, в двоичной СС тройкой цифр (например, 1 – 001, 4 – 100, 3 – 011 и т.д.).
    b. Далее каждая следующая удалённая цифра из исходного числа записывается как следующая тройка цифр нового числа.
4.	Вернуться к месту удаления цифры и вернуть её
5.	Перейти к следующей цифре и удалить её
6.	Повторять пункты 3-5, пока не дойдём до конца числа
7.	Затереть ведущие 0 у нового числа
8.	Перейти в конец нового числа и закончить


## 7. Сценарий выполнения работы [план работы, первоначальный текст программы в черновике (можно на отдельном листе) и тесты либо соображения по тестированию]. 
- Изучить литературу по машине Тьюринга
- Понять принцип работы машины Тьюринга
- Приобрести основные навыки работы с машиной Тьюринга
- Освоить различные функции машины Тьюринга
- Решить поставленную задачу с помощью машины Тьюринга
- Оформить отчёт установленной формы 


Пункты 1-7 отчета составляются сторого до начала лабораторной работы.
Допущен к выполнению работы.  
<b>Подпись преподавателя</b> ________________
## 8. Распечатка протокола 
```
00, ,<,qq

qq,1,<,qq
qq,2,<,qq
qq,3,<,qq
qq,4,<,qq
qq,5,<,qq
qq,6,<,qq
qq,7,<,qq
qq,8,<,qq
qq,0,<,qq
qq, ,>,qqq

qqq,0, ,q0
qqq,1, ,q1
qqq,2, ,q2
qqq,3, ,q3
qqq,4, ,q4
qqq,5, ,q5
qqq,6, ,q6
qqq,7, ,q7





q0,0,>,q0
q0,1,>,q0
q0,2,>,q0
q0,3,>,q0
q0,4,>,q0
q0,5,>,q0
q0,6,>,q0
q0,7,>,q0
q0, ,>,q0c

q0c,0,>,q0c
q0c,1,>,q0c
q0c,2,>,q0c
q0c,3,>,q0c
q0c,4,>,q0c
q0c,5,>,q0c
q0c,6,>,q0c
q0c,7,>,q0c
q0c, ,>,q00c

q00c, , ,q02
q00c,0,>,q00c
q00c,1,>,q00c
q00c,2,>,q00c
q00c,3,>,q00c
q00c,4,>,q00c
q00c,5,>,q00c
q00c,6,>,q00c
q00c,7,>,q00c

q02, ,0,q02
q02,0,>,q002
q002, ,0,q002
q002,0,>,q0002
q0002, ,0,q0002
q0002,0,<,q0cc

q0cc,0,<,q0cc
q0cc,1,<,q0cc
q0cc, ,<,q0ccc

q0ccc,0,<,q0ccc
q0ccc,1,<,q0ccc
q0ccc,2,<,q0ccc
q0ccc,3,<,q0ccc
q0ccc,4,<,q0ccc
q0ccc,5,<,q0ccc
q0ccc,6,<,q0ccc
q0ccc,7,<,q0ccc
q0ccc, ,0,cc





q1,0,>,q1
q1,1,>,q1
q1,2,>,q1
q1,3,>,q1
q1,4,>,q1
q1,5,>,q1
q1,6,>,q1
q1,7,>,q1
q1, ,>,q1c

q1c,0,>,q1c
q1c,1,>,q1c
q1c,2,>,q1c
q1c,3,>,q1c
q1c,4,>,q1c
q1c,5,>,q1c
q1c,6,>,q1c
q1c,7,>,q1c
q1c, ,>,q11c

q11c, , ,q12
q11c,0,>,q11c
q11c,1,>,q11c
q11c,2,>,q11c
q11c,3,>,q11c
q11c,4,>,q11c
q11c,5,>,q11c
q11c,6,>,q11c
q11c,7,>,q11c

q12, ,0,q12
q12,0,>,q112
q112, ,0,q112
q112,0,>,q1112
q1112, ,1,q1112
q1112,1,<,q1cc

q1cc,0,<,q1cc
q1cc,1,<,q1cc
q1cc, ,<,q1ccc

q1ccc,0,<,q1ccc
q1ccc,1,<,q1ccc
q1ccc,2,<,q1ccc
q1ccc,3,<,q1ccc
q1ccc,4,<,q1ccc
q1ccc,5,<,q1ccc
q1ccc,6,<,q1ccc
q1ccc,7,<,q1ccc
q1ccc, ,1,cc





q2,0,>,q2
q2,1,>,q2
q2,2,>,q2
q2,3,>,q2
q2,4,>,q2
q2,5,>,q2
q2,6,>,q2
q2,7,>,q2
q2, ,>,q2c

q2c,0,>,q2c
q2c,1,>,q2c
q2c,2,>,q2c
q2c,3,>,q2c
q2c,4,>,q2c
q2c,5,>,q2c
q2c,6,>,q2c
q2c,7,>,q2c
q2c, ,>,q22c

q22c, , ,q22
q22c,0,>,q22c
q22c,1,>,q22c
q22c,2,>,q22c
q22c,3,>,q22c
q22c,4,>,q22c
q22c,5,>,q22c
q22c,6,>,q22c
q22c,7,>,q22c

q22, ,0,q22
q22,0,>,q222
q222, ,1,q222
q222,1,>,q2222
q2222, ,0,q2222
q2222,0,<,q2cc

q2cc,0,<,q2cc
q2cc,1,<,q2cc
q2cc, ,<,q2ccc

q2ccc,0,<,q2ccc
q2ccc,1,<,q2ccc
q2ccc,2,<,q2ccc
q2ccc,3,<,q2ccc
q2ccc,4,<,q2ccc
q2ccc,5,<,q2ccc
q2ccc,6,<,q2ccc
q2ccc,7,<,q2ccc
q2ccc, ,2,cc





q3,0,>,q3
q3,1,>,q3
q3,2,>,q3
q3,3,>,q3
q3,4,>,q3
q3,5,>,q3
q3,6,>,q3
q3,7,>,q3
q3, ,>,q3c

q3c,0,>,q3c
q3c,1,>,q3c
q3c,2,>,q3c
q3c,3,>,q3c
q3c,4,>,q3c
q3c,5,>,q3c
q3c,6,>,q3c
q3c,7,>,q3c
q3c, ,>,q33c

q33c, , ,q32
q33c,0,>,q33c
q33c,1,>,q33c
q33c,2,>,q33c
q33c,3,>,q33c
q33c,4,>,q33c
q33c,5,>,q33c
q33c,6,>,q33c
q33c,7,>,q33c

q32, ,0,q32
q32,0,>,q332
q332, ,1,q332
q332,1,>,q3332
q3332, ,1,q3332
q3332,1,<,q3cc

q3cc,0,<,q3cc
q3cc,1,<,q3cc
q3cc, ,<,q3ccc

q3ccc,0,<,q3ccc
q3ccc,1,<,q3ccc
q3ccc,2,<,q3ccc
q3ccc,3,<,q3ccc
q3ccc,4,<,q3ccc
q3ccc,5,<,q3ccc
q3ccc,6,<,q3ccc
q3ccc,7,<,q3ccc
q3ccc, ,3,cc





q4,0,>,q4
q4,1,>,q4
q4,2,>,q4
q4,3,>,q4
q4,4,>,q4
q4,5,>,q4
q4,6,>,q4
q4,7,>,q4
q4, ,>,q4c

q4c,0,>,q4c
q4c,1,>,q4c
q4c,2,>,q4c
q4c,3,>,q4c
q4c,4,>,q4c
q4c,5,>,q4c
q4c,6,>,q4c
q4c,7,>,q4c
q4c, ,>,q44c

q44c, , ,q42
q44c,0,>,q44c
q44c,1,>,q44c
q44c,2,>,q44c
q44c,3,>,q44c
q44c,4,>,q44c
q44c,5,>,q44c
q44c,6,>,q44c
q44c,7,>,q44c

q42, ,1,q42
q42,1,>,q442
q442, ,0,q442
q442,0,>,q4442
q4442, ,0,q4442
q4442,0,<,q4cc

q4cc,0,<,q4cc
q4cc,1,<,q4cc
q4cc, ,<,q4ccc

q4ccc,0,<,q4ccc
q4ccc,1,<,q4ccc
q4ccc,2,<,q4ccc
q4ccc,3,<,q4ccc
q4ccc,4,<,q4ccc
q4ccc,5,<,q4ccc
q4ccc,6,<,q4ccc
q4ccc,7,<,q4ccc
q4ccc, ,4,cc





q5,0,>,q5
q5,1,>,q5
q5,2,>,q5
q5,3,>,q5
q5,4,>,q5
q5,5,>,q5
q5,6,>,q5
q5,7,>,q5
q5, ,>,q5c

q5c,0,>,q5c
q5c,1,>,q5c
q5c,2,>,q5c
q5c,3,>,q5c
q5c,4,>,q5c
q5c,5,>,q5c
q5c,6,>,q5c
q5c,7,>,q5c
q5c, ,>,q55c

q55c, , ,q52
q55c,0,>,q55c
q55c,1,>,q55c
q55c,2,>,q55c
q55c,3,>,q55c
q55c,4,>,q55c
q55c,5,>,q55c
q55c,6,>,q55c
q55c,7,>,q55c

q52, ,1,q52
q52,1,>,q552
q552, ,0,q552
q552,0,>,q5552
q5552, ,1,q5552
q5552,1,<,q5cc

q5cc,0,<,q5cc
q5cc,1,<,q5cc
q5cc, ,<,q5ccc

q5ccc,0,<,q5ccc
q5ccc,1,<,q5ccc
q5ccc,2,<,q5ccc
q5ccc,3,<,q5ccc
q5ccc,4,<,q5ccc
q5ccc,5,<,q5ccc
q5ccc,6,<,q5ccc
q5ccc,7,<,q5ccc
q5ccc, ,5,cc





q6,0,>,q6
q6,1,>,q6
q6,2,>,q6
q6,3,>,q6
q6,4,>,q6
q6,5,>,q6
q6,6,>,q6
q6,7,>,q6
q6, ,>,q6c

q6c,0,>,q6c
q6c,1,>,q6c
q6c,2,>,q6c
q6c,3,>,q6c
q6c,4,>,q6c
q6c,5,>,q6c
q6c,6,>,q6c
q6c,7,>,q6c
q6c, ,>,q66c

q66c, , ,q62
q66c,0,>,q66c
q66c,1,>,q66c
q66c,2,>,q66c
q66c,3,>,q66c
q66c,4,>,q66c
q66c,5,>,q66c
q66c,6,>,q66c
q66c,7,>,q66c

q62, ,1,q62
q62,1,>,q662
q662, ,1,q662
q662,1,>,q6662
q6662, ,0,q6662
q6662,0,<,q6cc

q6cc,0,<,q6cc
q6cc,1,<,q6cc
q6cc, ,<,q6ccc

q6ccc,0,<,q6ccc
q6ccc,1,<,q6ccc
q6ccc,2,<,q6ccc
q6ccc,3,<,q6ccc
q6ccc,4,<,q6ccc
q6ccc,5,<,q6ccc
q6ccc,6,<,q6ccc
q6ccc,7,<,q6ccc
q6ccc, ,6,cc





q7,0,>,q7
q7,1,>,q7
q7,2,>,q7
q7,3,>,q7
q7,4,>,q7
q7,5,>,q7
q7,6,>,q7
q7,7,>,q7
q7, ,>,q7c

q7c,0,>,q7c
q7c,1,>,q7c
q7c,2,>,q7c
q7c,3,>,q7c
q7c,4,>,q7c
q7c,5,>,q7c
q7c,6,>,q7c
q7c,7,>,q7c
q7c, ,>,q77c

q77c, , ,q72
q77c,0,>,q77c
q77c,1,>,q77c
q77c,2,>,q77c
q77c,3,>,q77c
q77c,4,>,q77c
q77c,5,>,q77c
q77c,6,>,q77c
q77c,7,>,q77c

q72, ,1,q72
q72,1,>,q772
q772, ,1,q772
q772,1,>,q7772
q7772, ,1,q7772
q7772,1,<,q7cc

q7cc,0,<,q7cc
q7cc,1,<,q7cc
q7cc, ,<,q7ccc

q7ccc,0,<,q7ccc
q7ccc,1,<,q7ccc
q7ccc,2,<,q7ccc
q7ccc,3,<,q7ccc
q7ccc,4,<,q7ccc
q7ccc,5,<,q7ccc
q7ccc,6,<,q7ccc
q7ccc,7,<,q7ccc
q7ccc, ,7,cc





cc,0,>,ccc
cc,1,>,ccc
cc,2,>,ccc
cc,3,>,ccc
cc,4,>,ccc
cc,5,>,ccc
cc,6,>,ccc
cc,7,>,ccc

ccc,0, ,q0
ccc,1, ,q1
ccc,2, ,q2
ccc,3, ,q3
ccc,4, ,q4
ccc,5, ,q5
ccc,6, ,q6
ccc,7, ,q7
ccc, ,>,d0

d0,0, ,d0
d0, ,>,d0
d0,1,1,end
d0,2,2,end
d0,3,3,end
d0,4,4,end
d0,5,5,end
d0,6,6,end
d0,7,7,end

end,0,>,end
end,1,>,end
end,2,>,end
end,3,>,end
end,4,>,end
end,5,>,end
end,6,>,end
end,7,>,end
end, , ,end

```
## 9. Дневник отладки должен содержать дату и время сеансов отладки и основные события (ошибки в сценарии и программе, нестандартные ситуации) и краткие комментарии к ним. В дневнике отладки приводятся сведения об использовании других ЭВМ, существенном участии преподавателя и других лиц в написании и отладке программы.

| № |  Лаб. или дом. | Дата | Время | Событие | Действие по исправлению | Примечание |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
## 10. Замечания автора по существу работы
```
00, ,<,qq

qq,1,<,qq
qq,2,<,qq
qq,3,<,qq
qq,4,<,qq
qq,5,<,qq
qq,6,<,qq
qq,7,<,qq
qq,8,<,qq
qq,0,<,qq
qq, ,>,qqq

qqq,0, ,q0
qqq,1, ,q1
qqq,2, ,q2
qqq,3, ,q3
qqq,4, ,q4
qqq,5, ,q5
qqq,6, ,q6
qqq,7, ,q7





q0,0,>,q0
q0,1,>,q0
q0,2,>,q0
q0,3,>,q0
q0,4,>,q0
q0,5,>,q0
q0,6,>,q0
q0,7,>,q0
q0, ,>,q0c

q0c,0,>,q0c
q0c,1,>,q0c
q0c,2,>,q0c
q0c,3,>,q0c
q0c,4,>,q0c
q0c,5,>,q0c
q0c,6,>,q0c
q0c,7,>,q0c
q0c, ,>,q00c

q00c, , ,q02
q00c,0,>,q00c
q00c,1,>,q00c
q00c,2,>,q00c
q00c,3,>,q00c
q00c,4,>,q00c
q00c,5,>,q00c
q00c,6,>,q00c
q00c,7,>,q00c

q02, ,0,q02
q02,0,>,q002
q002, ,0,q002
q002,0,>,q0002
q0002, ,0,q0002
q0002,0,<,q0cc

q0cc,0,<,q0cc
q0cc,1,<,q0cc
q0cc, ,<,q0ccc

q0ccc,0,<,q0ccc
q0ccc,1,<,q0ccc
q0ccc,2,<,q0ccc
q0ccc,3,<,q0ccc
q0ccc,4,<,q0ccc
q0ccc,5,<,q0ccc
q0ccc,6,<,q0ccc
q0ccc,7,<,q0ccc
q0ccc, ,0,cc





q1,0,>,q1
q1,1,>,q1
q1,2,>,q1
q1,3,>,q1
q1,4,>,q1
q1,5,>,q1
q1,6,>,q1
q1,7,>,q1
q1, ,>,q1c

q1c,0,>,q1c
q1c,1,>,q1c
q1c,2,>,q1c
q1c,3,>,q1c
q1c,4,>,q1c
q1c,5,>,q1c
q1c,6,>,q1c
q1c,7,>,q1c
q1c, ,>,q11c

q11c, , ,q12
q11c,0,>,q11c
q11c,1,>,q11c
q11c,2,>,q11c
q11c,3,>,q11c
q11c,4,>,q11c
q11c,5,>,q11c
q11c,6,>,q11c
q11c,7,>,q11c

q12, ,0,q12
q12,0,>,q112
q112, ,0,q112
q112,0,>,q1112
q1112, ,1,q1112
q1112,1,<,q1cc

q1cc,0,<,q1cc
q1cc,1,<,q1cc
q1cc, ,<,q1ccc

q1ccc,0,<,q1ccc
q1ccc,1,<,q1ccc
q1ccc,2,<,q1ccc
q1ccc,3,<,q1ccc
q1ccc,4,<,q1ccc
q1ccc,5,<,q1ccc
q1ccc,6,<,q1ccc
q1ccc,7,<,q1ccc
q1ccc, ,1,cc





q2,0,>,q2
q2,1,>,q2
q2,2,>,q2
q2,3,>,q2
q2,4,>,q2
q2,5,>,q2
q2,6,>,q2
q2,7,>,q2
q2, ,>,q2c

q2c,0,>,q2c
q2c,1,>,q2c
q2c,2,>,q2c
q2c,3,>,q2c
q2c,4,>,q2c
q2c,5,>,q2c
q2c,6,>,q2c
q2c,7,>,q2c
q2c, ,>,q22c

q22c, , ,q22
q22c,0,>,q22c
q22c,1,>,q22c
q22c,2,>,q22c
q22c,3,>,q22c
q22c,4,>,q22c
q22c,5,>,q22c
q22c,6,>,q22c
q22c,7,>,q22c

q22, ,0,q22
q22,0,>,q222
q222, ,1,q222
q222,1,>,q2222
q2222, ,0,q2222
q2222,0,<,q2cc

q2cc,0,<,q2cc
q2cc,1,<,q2cc
q2cc, ,<,q2ccc

q2ccc,0,<,q2ccc
q2ccc,1,<,q2ccc
q2ccc,2,<,q2ccc
q2ccc,3,<,q2ccc
q2ccc,4,<,q2ccc
q2ccc,5,<,q2ccc
q2ccc,6,<,q2ccc
q2ccc,7,<,q2ccc
q2ccc, ,2,cc





q3,0,>,q3
q3,1,>,q3
q3,2,>,q3
q3,3,>,q3
q3,4,>,q3
q3,5,>,q3
q3,6,>,q3
q3,7,>,q3
q3, ,>,q3c

q3c,0,>,q3c
q3c,1,>,q3c
q3c,2,>,q3c
q3c,3,>,q3c
q3c,4,>,q3c
q3c,5,>,q3c
q3c,6,>,q3c
q3c,7,>,q3c
q3c, ,>,q33c

q33c, , ,q32
q33c,0,>,q33c
q33c,1,>,q33c
q33c,2,>,q33c
q33c,3,>,q33c
q33c,4,>,q33c
q33c,5,>,q33c
q33c,6,>,q33c
q33c,7,>,q33c

q32, ,0,q32
q32,0,>,q332
q332, ,1,q332
q332,1,>,q3332
q3332, ,1,q3332
q3332,1,<,q3cc

q3cc,0,<,q3cc
q3cc,1,<,q3cc
q3cc, ,<,q3ccc

q3ccc,0,<,q3ccc
q3ccc,1,<,q3ccc
q3ccc,2,<,q3ccc
q3ccc,3,<,q3ccc
q3ccc,4,<,q3ccc
q3ccc,5,<,q3ccc
q3ccc,6,<,q3ccc
q3ccc,7,<,q3ccc
q3ccc, ,3,cc





q4,0,>,q4
q4,1,>,q4
q4,2,>,q4
q4,3,>,q4
q4,4,>,q4
q4,5,>,q4
q4,6,>,q4
q4,7,>,q4
q4, ,>,q4c

q4c,0,>,q4c
q4c,1,>,q4c
q4c,2,>,q4c
q4c,3,>,q4c
q4c,4,>,q4c
q4c,5,>,q4c
q4c,6,>,q4c
q4c,7,>,q4c
q4c, ,>,q44c

q44c, , ,q42
q44c,0,>,q44c
q44c,1,>,q44c
q44c,2,>,q44c
q44c,3,>,q44c
q44c,4,>,q44c
q44c,5,>,q44c
q44c,6,>,q44c
q44c,7,>,q44c

q42, ,1,q42
q42,1,>,q442
q442, ,0,q442
q442,0,>,q4442
q4442, ,0,q4442
q4442,0,<,q4cc

q4cc,0,<,q4cc
q4cc,1,<,q4cc
q4cc, ,<,q4ccc

q4ccc,0,<,q4ccc
q4ccc,1,<,q4ccc
q4ccc,2,<,q4ccc
q4ccc,3,<,q4ccc
q4ccc,4,<,q4ccc
q4ccc,5,<,q4ccc
q4ccc,6,<,q4ccc
q4ccc,7,<,q4ccc
q4ccc, ,4,cc





q5,0,>,q5
q5,1,>,q5
q5,2,>,q5
q5,3,>,q5
q5,4,>,q5
q5,5,>,q5
q5,6,>,q5
q5,7,>,q5
q5, ,>,q5c

q5c,0,>,q5c
q5c,1,>,q5c
q5c,2,>,q5c
q5c,3,>,q5c
q5c,4,>,q5c
q5c,5,>,q5c
q5c,6,>,q5c
q5c,7,>,q5c
q5c, ,>,q55c

q55c, , ,q52
q55c,0,>,q55c
q55c,1,>,q55c
q55c,2,>,q55c
q55c,3,>,q55c
q55c,4,>,q55c
q55c,5,>,q55c
q55c,6,>,q55c
q55c,7,>,q55c

q52, ,1,q52
q52,1,>,q552
q552, ,0,q552
q552,0,>,q5552
q5552, ,1,q5552
q5552,1,<,q5cc

q5cc,0,<,q5cc
q5cc,1,<,q5cc
q5cc, ,<,q5ccc

q5ccc,0,<,q5ccc
q5ccc,1,<,q5ccc
q5ccc,2,<,q5ccc
q5ccc,3,<,q5ccc
q5ccc,4,<,q5ccc
q5ccc,5,<,q5ccc
q5ccc,6,<,q5ccc
q5ccc,7,<,q5ccc
q5ccc, ,5,cc





q6,0,>,q6
q6,1,>,q6
q6,2,>,q6
q6,3,>,q6
q6,4,>,q6
q6,5,>,q6
q6,6,>,q6
q6,7,>,q6
q6, ,>,q6c

q6c,0,>,q6c
q6c,1,>,q6c
q6c,2,>,q6c
q6c,3,>,q6c
q6c,4,>,q6c
q6c,5,>,q6c
q6c,6,>,q6c
q6c,7,>,q6c
q6c, ,>,q66c

q66c, , ,q62
q66c,0,>,q66c
q66c,1,>,q66c
q66c,2,>,q66c
q66c,3,>,q66c
q66c,4,>,q66c
q66c,5,>,q66c
q66c,6,>,q66c
q66c,7,>,q66c

q62, ,1,q62
q62,1,>,q662
q662, ,1,q662
q662,1,>,q6662
q6662, ,0,q6662
q6662,0,<,q6cc

q6cc,0,<,q6cc
q6cc,1,<,q6cc
q6cc, ,<,q6ccc

q6ccc,0,<,q6ccc
q6ccc,1,<,q6ccc
q6ccc,2,<,q6ccc
q6ccc,3,<,q6ccc
q6ccc,4,<,q6ccc
q6ccc,5,<,q6ccc
q6ccc,6,<,q6ccc
q6ccc,7,<,q6ccc
q6ccc, ,6,cc





q7,0,>,q7
q7,1,>,q7
q7,2,>,q7
q7,3,>,q7
q7,4,>,q7
q7,5,>,q7
q7,6,>,q7
q7,7,>,q7
q7, ,>,q7c

q7c,0,>,q7c
q7c,1,>,q7c
q7c,2,>,q7c
q7c,3,>,q7c
q7c,4,>,q7c
q7c,5,>,q7c
q7c,6,>,q7c
q7c,7,>,q7c
q7c, ,>,q77c

q77c, , ,q72
q77c,0,>,q77c
q77c,1,>,q77c
q77c,2,>,q77c
q77c,3,>,q77c
q77c,4,>,q77c
q77c,5,>,q77c
q77c,6,>,q77c
q77c,7,>,q77c

q72, ,1,q72
q72,1,>,q772
q772, ,1,q772
q772,1,>,q7772
q7772, ,1,q7772
q7772,1,<,q7cc

q7cc,0,<,q7cc
q7cc,1,<,q7cc
q7cc, ,<,q7ccc

q7ccc,0,<,q7ccc
q7ccc,1,<,q7ccc
q7ccc,2,<,q7ccc
q7ccc,3,<,q7ccc
q7ccc,4,<,q7ccc
q7ccc,5,<,q7ccc
q7ccc,6,<,q7ccc
q7ccc,7,<,q7ccc
q7ccc, ,7,cc





cc,0,>,ccc
cc,1,>,ccc
cc,2,>,ccc
cc,3,>,ccc
cc,4,>,ccc
cc,5,>,ccc
cc,6,>,ccc
cc,7,>,ccc

ccc,0, ,q0
ccc,1, ,q1
ccc,2, ,q2
ccc,3, ,q3
ccc,4, ,q4
ccc,5, ,q5
ccc,6, ,q6
ccc,7, ,q7
ccc, ,>,d0

d0,0, ,d0
d0, ,>,d0
d0,1,<,end
d0,2,<,end
d0,3,<,end
d0,4,<,end
d0,5,<,end
d0,6,<,end
d0,7,<,end

end, ,<,endd
endd, ,>,enddd
endd,0,>,kon
endd,1,>,kon
endd,2,>,kon
endd,3,>,kon
endd,4,>,kon
endd,5,>,kon
endd,6,>,kon
endd,7,>,kon

enddd, ,>,per

per,0, ,per0
per,1, ,per1
per,2, ,per2
per,3, ,per3
per,4, ,per4
per,5, ,per5
per,6, ,per6
per,7, ,per7
per, ,<,pern

pern, ,<,pern
pern,0,<,pernn
pern,1,<,pernn
pern,2,<,pernn
pern,3,<,pernn
pern,4,<,pernn
pern,5,<,pernn
pern,6,<,pernn
pern,7,<,pernn
pernn,0,<,pernn
pernn,1,<,pernn
pernn,2,<,pernn
pernn,3,<,pernn
pernn,4,<,pernn
pernn,5,<,pernn
pernn,6,<,pernn
pernn,7,<,pernn
pernn, , ,end


prom, ,>,per

per0, ,<,per00
per00, ,0,per00
per00,0,>,prom

per1, ,<,per11
per11, ,1,per11
per11,1,>,prom

per2, ,<,per22
per22, ,2,per22
per22,2,>,prom

per3, ,<,per33
per33, ,3,per33
per33,3,>,prom

per4, ,<,per44
per44, ,4,per44
per44,4,>,prom

per5, ,<,per55
per55, ,5,per55
per55,5,>,prom

per6, ,<,per66
per66, ,6,per66
per66,6,>,prom

per7, ,<,per77
per77, ,7,per77
per77,7,>,prom

kon, ,>,konn
konn,0,>,konn
konn,1,>,konn
konn,2,>,konn
konn,3,>,konn
konn,4,>,konn
konn,5,>,konn
konn,6,>,konn
konn,7,>,konn
konn, , ,konn
```
## 11. Выводы
 В ходе выполнения данной лабораторной работы были приобретены основные навыки работы с машинами Тьюринга (копирование входных данных и их преобразование), освоены принципы работы с ней. Были изучены различные методы решения задач с помощью машин Тьюринга.

Недочёты при выполнении задания могут быть устранены следующим образом: —

<b>Подпись студента:</b> ____________________
