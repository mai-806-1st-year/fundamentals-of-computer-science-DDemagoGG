# Отчёт по лабораторной работе №13 по курсам “Основы информатики” и "Программно-аппаратные средства информатики"

<b>Студент группы:</b> <ins>М80-108Б-22 Формалёв Александр Сергеевич, № по списку 21</ins> 

<b>Контакты e-mail:</b> <ins>lyadiez@mail.ru</ins>

<b>Работа выполнена:</b> «30» <ins>ноября</ins> <ins>2022</ins> г.

<b>Преподаватель:</b> <ins>асп. каф. 806 Сахарин Никита Александрович</ins>

<b>Входной контроль знаний с оценкой:</b> <ins> </ins>

<b>Отчет сдан</b> «3» <ins>декабря</ins> <ins>2022</ins> г., <b>итоговая оценка</b> <ins> </ins>

<b>Подпись преподавателя:</b> ________________


## 1. Тема
Работа с множествами.

## 2. Цель работы
Составить программу проверки характеристик введёных последовательностей слов и печати развёрнутого ответа на языке Си в соответствии с вариантом задания, используя битовые маски.

## 3. Задание (вариант № 20)
Есть ли слово, содержащее одну согласную, возможно несколько раз.

## 4. Оборудование:

<b>Процессор:</b> AMD A9-9425 RADEON R5, 5 COMPUTE CORES 2C+3G 3.10 GHz <br/>

<b>ОП:</b> 8 ГБ <br/>

<b>SSD:</b> 256 ГБ<br/>

<b>Монитор:</b> 1920 х 1080 <br/>

## 5. Программное обеспечение:
<b>Операционная система семейства:</b> Ubuntu 22.04.01 LTS<br/>

<b>Интерпретатор команд:</b> bash версия 4.4.19<br/>

<b>Система программирования:</b> не использовалась версия —<br/>

<b>Редактор текстов:</b> VS Code

<b>Утилиты операционной системы:</b> -

<b>Прикладные системы и программы:</b> -

<b>Местонахождение и имена файлов программ и данных на домашнем компьютере:</b>

## 6. Идея, метод, алгоритм решения задачи (в формах: словесной, псевдокода, графической [блок-схема, диаграмма, рисунок, таблица] или формальные спецификации с пред- и постусловиями)

• Разобраться с поставленной задачей

• Найти решение с помощью программы на языке С

• Скомпилировать программу

• Запустить программу

## 7. Сценарий выполнения работы [план работы, первоначальный текст программы в черновике (можно на отдельном листе) и тесты либо соображения по тестированию]. 

```
#include <stdio.h>
#include <ctype.h>

#define CONSONANTS (1u << ('b' - 'a') | 1u << ('c' - 'a') | 1u << ('d' - 'a') | 1u << ('f' - 'a') |\
1u << ('g' - 'a') | 1u << ('h' - 'a') | 1u << ('j' - 'a') | 1u << ('k' - 'a') | 1u << ('l' - 'a') |\
1u << ('m' - 'a') | 1u << ('n' - 'a') | 1u << ('p' - 'a') | 1u << ('q' - 'a') | 1u << ('r' - 'a') |\
1u << ('s' - 'a') | 1u << ('t' - 'a') | 1u << ('v' - 'a') | 1u << ('w' - 'a') | 1u << ('x' - 'a') |\
1u << ('z' - 'a'))

typedef unsigned int uint;

uint char_to_set(int ch){
    ch = tolower(ch);
    if (isalpha(ch)){
        return (1u << (ch - 'a'));
    } else{
        return 0;
    }
}

typedef enum{
    CONSONANT_IN_WORD,
    NO_CONSONANTS_IN_WORD,
    WRONG_WORD
} state;

int main(){
    uint set = 0;
    state state = NO_CONSONANTS_IN_WORD;
    int counter = 0;
    for (int c = getchar(); c != EOF; c = getchar()){
        if ((c == ' ') || (c == '\n')){
            if (state == CONSONANT_IN_WORD){
                counter++;
            }
            set = 0;
            state = NO_CONSONANTS_IN_WORD;
        } else{
            if (state == NO_CONSONANTS_IN_WORD){
                if ((char_to_set(c) & CONSONANTS) != 0){
                    state = CONSONANT_IN_WORD;
                    set = char_to_set(c);
                }
            } else if (state == CONSONANT_IN_WORD){
                if (((char_to_set(c) & CONSONANTS) | set) != set){
                    state = WRONG_WORD;
                }
            }
        }
    }
    if (counter > 0){
        printf("YES\n");
    } else{
        printf("NO\n");
    }
    return 0;
}
```

Пункты 1-7 отчета составляются сторого до начала лабораторной работы.
Допущен к выполнению работы.  
Подпись преподавателя _____________________
## 8. Распечатка протокола 
```
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"laba13" 
slfdn   
NO
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"laba13" 
aaaaaaa dskdjasd pqwke
sdkm jjjkk    
NO
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"laba13" 
aaaaaaaaaaaaaaaaaaddddddddddddddddddddddddddddddd fsdkf
fsdfmm sssdaa
YES
```
## 9. Дневник отладки должен содержать дату и время сеансов отладки и основные события (ошибки в сценарии и программе, нестандартные ситуации) и краткие комментарии к ним. В дневнике отладки приводятся сведения об использовании других ЭВМ, существенном участии преподавателя и других лиц в написании и отладке программы.

| № |  Лаб. или дом. | Дата | Время | Событие | Действие по исправлению | Примечание |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 1 | дом. | 30.11.22 | 18:00 | Выполнение лабораторной работы | - | - |

## 10. Замечания автора по существу работы — Написание команд для отработки навыков работы в ОС UNIX.

Для защиты лабораторной работы было предложено задание: https://codeforces.com/problemset/problem/579/A

```
#include <stdio.h>

int main(){
    int x, counter = 0, counter_bacteries = 1;
    scanf("%d", &x);
    while (x != 0){
        if (counter_bacteries > x){
            x -= counter_bacteries / 2;
            counter_bacteries = 1;
            counter += 1;
        } else if(counter_bacteries == x){
            x -= counter_bacteries;
            counter += 1;
        } else{
            counter_bacteries *= 2;
        }
    }
    printf("%d", counter);
}
```
<b>Тесты:</b>

```
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"sashafile" 
5
2
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"sashafile" 
8
1
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"sashafile" 
13
3
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ 
```
    
## 11. Выводы

Были приобретены навыки работы с битовыми масками и выяснен принцип составления множества на языке Си.

Недочёты при выполнении задания могут быть устранены следующим образом: —

Подпись студента _________________


