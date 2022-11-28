# Отчёт по лабораторной работе №9 по курсам “Основы информатики” и "Программно-аппаратные средства информатики"

<b>Студент группы:</b> <ins>М80-108Б-22 Формалёв Александр Сергеевич, № по списку 21</ins> 

<b>Контакты e-mail:</b> <ins>lyadiez@mail.ru</ins>

<b>Работа выполнена:</b> «9» <ins>ноября</ins> <ins>2022</ins> г.

<b>Преподаватель:</b> <ins>асп. каф. 806 Сахарин Никита Александрович</ins>

<b>Входной контроль знаний с оценкой:</b> <ins> </ins>

<b>Отчет сдан</b> «» <ins></ins> <ins>2022</ins> г., <b>итоговая оценка</b> <ins> </ins>

<b>Подпись преподавателя:</b> ________________


## 1. Тема
Програмирование на языке С
## 2. Цель работы
Составление и отладка простейшей программы на языке С итеративного характера с целочисленными рекуретными соотношениями, задающими некоторое регулярное движение точки в целочисленной системе координат (i,j) с дискретными временем к и динамическим параметром l.
## 3. Задание (вариант № 20)
Полоса, ограниченная прямыми i + j + 10 = 0 и i + j + 20 = 0.
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
```
#include <stdio.h>

int sign(int a) {
    if (a < 0) return -1;
    if (a > 0) return 1;
    return 0;
}

int abs(int a) {
    if (a < 0) return -a;
    return a;
}

int mod(int a, int b) {
    return a - (a / b) * b;
}

int max(int a, int b) {
    if (a < b) return b;
    return a;
}

int min(int a, int b) {
    return (a + b) - max(a, b);
}

struct state{
    int i, j, l;
};

int check(struct state point){
    return ((point.i + point.j >= -20) && (point.i + point.j <= -10));
}

void change(struct state* pt, int index){
    int i = pt->i, j = pt->j, l = pt->l;
    pt->i = mod((abs(i - j) * l - abs(j - l) * i + abs(i - l) * j), 20) - index;
    pt->j = mod((min(i, j) * max(j, l) * min(i, l)), 25) + 5 * sign(i - l);
    pt->l = abs(l) * sign(i - j) - abs(i) * sign(j - l) + abs(j) * sign(i - l); 
}

void run(struct state pt){
    int flag = 0;
    for (int index = 0; index < 50; index++){
        if (check(pt)){
            flag = 1;
            printf("YES, time = %d i = %d j = %d l = %d\n", index, pt.i, pt.j, pt.l);
            break;
        }
        change(&pt, index);
    }
    if (flag == 0){
        printf("NO, time = %d i = %d j = %d l = %d\n", 49, pt.i, pt.j, pt.l);
    }
}

int main(){
    struct state pt = {-25, -9, -8};
    run(pt);
    return 0;
}
```
## 7. Сценарий выполнения работы [план работы, первоначальный текст программы в черновике (можно на отдельном листе) и тесты либо соображения по тестированию].
1. Подумать над решением задачи.
2. Написать программу.
3. Скомпилировать программу.
4. Запустить программу.
5. Получить ответ.

Пункты 1-7 отчета составляются сторого до начала лабораторной работы.
Допущен к выполнению работы.  
<b>Подпись преподавателя</b> ________________
## 8. Распечатка протокола 
```
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ gcc laba9.c
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./a.out
YES, time = 13 i = -20 j = 5 l = 30
```
## 9. Дневник отладки должен содержать дату и время сеансов отладки и основные события (ошибки в сценарии и программе, нестандартные ситуации) и краткие комментарии к ним. В дневнике отладки приводятся сведения об использовании других ЭВМ, существенном участии преподавателя и других лиц в написании и отладке программы.

| № |  Лаб. или дом. | Дата | Время | Событие | Действие по исправлению | Примечание |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 1 | дом. | 09.11.22 | 13:00 | Выполнение лабораторной работы | - | - |
## 10. Замечания автора по существу работы — Написание команд для отработки навыков работы в ОС UNIX.

Для защиты лабораторной работы было предложено задание: написать программу, имеющую тот же смысл, что и для задания лабораторной работы, но с другой фигурой, а именно - правильный пятиугольник, нижняя грань которого параллельно оси Ох, о котором известны координаты его центра и радиус вписанной окружности.
```
#include <stdio.h>
#include <math.h>

const double pi = 3.141592653;

int sign(int a) {
    if (a < 0) return -1;
    if (a > 0) return 1;
    return 0;
}

int abs(int a) {
    if (a < 0) return -a;
    return a;
}

int mod(int a, int b) {
    return a - (a / b) * b;
}

int max(int a, int b) {
    if (a < b) return b;
    return a;
}

int min(int a, int b) {
    return (a + b) - max(a, b);
}

struct state{
    int i, j, l;
};

struct center{
    int x, y, r;
};

int check(struct state pt, struct center penta){
    return(((pt.j - penta.y) - tan(((double)108 * pi) / 180) * (pt.i - penta.x) + penta.r * sqrt(tan(((double)108 * pi) / 180) * tan(((double)108 * pi) / 180) + 1) >= 0)
     && ((pt.j - penta.y) - tan(((double)36 * pi) / 180) * (pt.i - penta.x) - penta.r * sqrt(tan(((double)36 * pi) / 180) * tan(((double)36 * pi) / 180) + 1) <= 0)
      && ((pt.j - penta.y) - tan(((double)144 * pi) / 180) * (pt.i - penta.x) - penta.r * sqrt(tan(((double)144 * pi) / 180) * tan(((double)144 * pi) / 180) + 1) <= 0)
       && ((pt.j - penta.y) - tan(((double)72 * pi) / 180) * (pt.i - penta.x) + penta.r * sqrt(tan(((double)72 * pi) / 180) * tan(((double)72 * pi) / 180) + 1) >= 0)
        && ((pt.j - penta.y) + penta.r >= 0));
}

void change(struct state* pt, int index){
    int i = pt->i, j = pt->j, l = pt->l;
    pt->i = mod((abs(i - j) * l - abs(j - l) * i + abs(i - l) * j), 20) - index;
    pt->j = mod((min(i, j) * max(j, l) * min(i, l)), 25) + 5 * sign(i - l);
    pt->l = abs(l) * sign(i - j) - abs(i) * sign(j - l) + abs(j) * sign(i - l); 
}

void run(struct state pt, struct center penta){
    int flag = 0;
    for (int index = 0; index < 50; index++){
        if (check(pt, penta)){
            flag = 1;
            printf("YES, time = %d i = %d j = %d l = %d\n", index, pt.i, pt.j, pt.l);
            break;
        }
        change(&pt, index);
    }
    if (flag == 0){
        printf("NO, time = %d i = %d j = %d l = %d\n", 49, pt.i, pt.j, pt.l);
    }
}

int main(){
    struct center penta = {0, 0, 5};
    struct state pt = {-25, -9, -8};
    run(pt, penta);
    return 0;
}
```
## 11. Выводы
Были изучены основы работы с компилятором gcc: установка, компиляция, выполнение программ.

Недочёты при выполнении задания могут быть устранены следующим образом: —

Подпись студента _________________

