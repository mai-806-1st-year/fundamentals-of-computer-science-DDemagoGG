# Отчёт по лабораторной работе №11 по курсам “Основы информатики” и "Программно-аппаратные средства информатики"

<b>Студент группы:</b> <ins>М80-108Б-22 Формалёв Александр Сергеевич, № по списку 21</ins> 

<b>Контакты e-mail:</b> <ins>lyadiez@mail.ru</ins>

<b>Работа выполнена:</b> «9» <ins>ноября</ins> <ins>2022</ins> г.

<b>Преподаватель:</b> <ins>асп. каф. 806 Сахарин Никита Александрович</ins>

<b>Входной контроль знаний с оценкой:</b> <ins> </ins>

<b>Отчет сдан</b> «17» <ins>ноября</ins> <ins>2022</ins> г., <b>итоговая оценка</b> <ins> </ins>

<b>Подпись преподавателя:</b> ________________


## 1. Тема
Техника работы с целыми числами.

## 2. Цель работы
Составить программу на языке Си, выполняющую анализ и обработку вводимого текста и работающую без ограничений на количество и длину строк исходного текста.

## 3. Задание (вариант № 4)
Перевести все мерные расстояния из миль в километры.

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
• Разобраться с поставленной задачей

• Найти решение с помощью программы на языке С

•	Скомпилировать программу

•	Запустить программу

## 7. Сценарий выполнения работы [план работы, первоначальный текст программы в черновике (можно на отдельном листе) и тесты либо соображения по тестированию]. 
```
#include <stdio.h>
#include <ctype.h>

typedef enum {
    STATE_OUT_OF_WORD,
    STATE_IN_NUMBER,
    STATE_IN_ZEROES,
    STATE_IN_ASH,
    STATE_IN_MAYBE_MILE,
    STATE_IN_MILE
} state;

int is_digit_without_zero(char ch){
    if(('0' < ch ) && (ch <= '9')){
        return 1;
    } else{
        return 0;
    }
}

int to_km(int mile){
    return (int)(1.609 * mile);
}

int main(){
    state state = STATE_OUT_OF_WORD;
    char c;
    int num = 0; 
    c = getchar();
    while (c != EOF){
        switch (state){
            case STATE_OUT_OF_WORD:
                if (is_digit_without_zero(c)){
                    state = STATE_IN_NUMBER;
                    num += (c - '0');
                } else if(c == '0'){
                    state = STATE_IN_ZEROES;
                    putchar('0');
                } else if((c == ' ') || (c == '\n') || (c == '\t')){
                    putchar(c);
                } else{
                    putchar(c);
                    state = STATE_IN_ASH;
                }
                break;
            case STATE_IN_NUMBER:
                if(isdigit(c)){
                    num = num * 10 + (c - '0');
                } else if(c == 'm'){
                    state = STATE_IN_MAYBE_MILE;
                } else if((c == ' ') || (c == '\n') || (c == '\t')){
                    printf("%d%c", num, c);
                    num = 0;
                    state = STATE_OUT_OF_WORD;
                } else{
                    state = STATE_IN_ASH;
                    printf("%d", num);
                    num = 0;
                    putchar(c);
                }
                break;
            case STATE_IN_ZEROES:
                if(c == '0'){
                    putchar('0');
                } else if(is_digit_without_zero(c)){
                    state = STATE_IN_NUMBER;
                    num += (c - '0');
                } else if((c == ' ') || (c == '\n') || (c == '\t')){
                    putchar(c);
                    state = STATE_OUT_OF_WORD;
                } else{
                    putchar(c);
                    state = STATE_IN_ASH;
                }
                break;
            case STATE_IN_ASH:
                if ((c == ' ') || (c == '\n') || (c == '\t')){
                    putchar(c);
                    state = STATE_OUT_OF_WORD;
                } else{
                    putchar(c);
                }
                break;
            case STATE_IN_MAYBE_MILE:
                if (c == 'i'){
                    state = STATE_IN_MILE;
                } else if((c == ' ') || (c == '\n') || (c == '\t')){
                    printf("%dm%c", num, c);
                    num = 0;
                    state = STATE_OUT_OF_WORD;
                } else{
                    printf("%dm", num);
                    num = 0;
                    putchar(c);
                    state = STATE_IN_ASH;
                }
                break;
            case STATE_IN_MILE:
                if((c == ' ') || (c == '\n') || (c == '\t')){
                    printf("%dkm%c", to_km(num), c);
                    num = 0;
                    state = STATE_OUT_OF_WORD;
                } else{
                    state = STATE_IN_ASH;
                    printf("%dmi", num);
                    num = 0;
                    putchar(c);
                }
                break;
    }
        c = getchar();
    }
    return 0;
}
```

Пункты 1-7 отчета составляются сторого до начала лабораторной работы.
Допущен к выполнению работы.  
Подпись преподавателя _____________________
## 8. Распечатка протокола 

```
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ gcc zlaba11.c
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./a.out << eof
> 1000
> 1000mi
> 1000mik
> 4523km
> skdjfsdj sdf 10mi d12n3d3
> eof
1000
1609km
1000mik
4523km
skdjfsdj sdf 16km d12n3d3
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ 
```

## 9. Дневник отладки должен содержать дату и время сеансов отладки и основные события (ошибки в сценарии и программе, нестандартные ситуации) и краткие комментарии к ним. В дневнике отладки приводятся сведения об использовании других ЭВМ, существенном участии преподавателя и других лиц в написании и отладке программы.

| № |  Лаб. или дом. | Дата | Время | Событие | Действие по исправлению | Примечание |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 1 | дом. | 09.11.22 | 18:00 | Выполнение лабораторной работы | - | - |
## 10. Замечания автора по существу работы — Написание команд для отработки навыков работы в ОС UNIX.

Замечаний не было

## 11. Выводы
Были приобретены навыки написания программ, анализирующих и обрабатывающих входные данные и работающих все зависимости от длины входного слова и количества строк, на языке Си. Изучена работа функций getchar и putchar.

Недочёты при выполнении задания могут быть устранены следующим образом: —

Подпись студента _________________


