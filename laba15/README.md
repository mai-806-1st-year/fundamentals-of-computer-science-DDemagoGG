# Отчёт по лабораторной работе №15 по курсам “Основы информатики” и "Программно-аппаратные средства информатики"

<b>Студент группы:</b> <ins>М80-108Б-22 Формалёв Александр Сергеевич, № по списку 21</ins> 

<b>Контакты e-mail:</b> <ins>lyadiez@mail.ru</ins>

<b>Работа выполнена:</b> «30» <ins>ноября</ins> <ins>2022</ins> г.

<b>Преподаватель:</b> <ins>асп. каф. 806 Сахарин Никита Александрович</ins>

<b>Входной контроль знаний с оценкой:</b> <ins> </ins>

<b>Отчет сдан</b> «8» <ins>декабря</ins> <ins>2022</ins> г., <b>итоговая оценка</b> <ins> </ins>

<b>Подпись преподавателя:</b> ________________


## 1. Тема
Обработка матриц.

## 2. Цель работы
Составить программу на языке Си, производящую обработку квадратной матрицы порядка NxN (1 <= N <= N), из целых чисел, вводимой из стандартного входного текстового файла.

## 3. Задание (вариант № 20)
Замена всех минимальных элементов матрицы на сумму элементов соответствубщего столбца.

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

void input_matrix(int n, int (*massive)[n]){
    for(int i = 0;i!=n;++i){
        for (int j = 0; j != n; ++j){
            scanf ("%02d", &massive[i][j]);
        }
    }
}

int min_el(int n, int (*massive)[n]){
    int m = 10000000000;
    for(int i = 0;i!=n;++i){
        for (int j = 0; j != n; ++j){
            if (m > massive[i][j]){
                m = massive[i][j];
            }
        }
    }
    return m;
}

int sum_column(int n, int j, int (*massive)[n]){
    int s = 0;
    for (int i = 0; i != n; ++i){
        s += massive[i][j];
    }
    return s;
}

void matrix_change(int min_elem, int n, int (*massive)[n]){
    for(int j = 0; j != n; ++j){
        for (int i = 0; i != n; ++i){
            if (massive[i][j] == min_elem){
                massive[i][j] = sum_column(n, j, (int (*)[n]) massive);
            }
        }
    }
}

void matrix_print(int n, int (*massive)[n]){
    for(int i = 0;i!=n;++i){
        putchar('\n');
        for (int j = 0; j != n; ++j){
            printf("%d ", massive[i][j]);
        }
    }
}

#define N (8)

int main(){
    int massive[N * N];
    int n;
    scanf ("%d", &n);
    input_matrix(n, (int (*)[n]) massive);
    int min_elem = min_el(n, (int (*)[n]) massive);
    matrix_change(min_elem, n, (int (*)[n]) massive);
    matrix_print(n, (int (*)[n]) massive);
    putchar('\n');
    return 0;
}
```

Пункты 1-7 отчета составляются сторого до начала лабораторной работы.
Допущен к выполнению работы.  
Подпись преподавателя _____________________
## 8. Распечатка протокола 
```
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"laba15" 
4 
1 2 3 4
2 5 8 1
5 2 1 1
2 1 5 9

10 2 3 4 
2 5 8 15 
5 2 17 15 
2 10 5 9 
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"laba15"
3
1 1 1
1 1 1
1 1 1

3 3 3 
3 3 3 
3 3 3 
```
## 9. Дневник отладки должен содержать дату и время сеансов отладки и основные события (ошибки в сценарии и программе, нестандартные ситуации) и краткие комментарии к ним. В дневнике отладки приводятся сведения об использовании других ЭВМ, существенном участии преподавателя и других лиц в написании и отладке программы.

| № |  Лаб. или дом. | Дата | Время | Событие | Действие по исправлению | Примечание |
| ------ | ------ | ------ | ------ | ------ | ------ | ------ |
| 1 | дом. | 30.11.22 | 18:00 | Выполнение лабораторной работы | - | - |

## 10. Замечания автора по существу работы — Написание команд для отработки навыков работы в ОС UNIX.

Для защиты лабораторной работы было предложено задание: проверка матрицы на ортогональность.

```
#include <stdio.h>

#define N (8)

void to_transposed(int n, int (*massive)[n], int (*trans)[n]){
    for (int i = 0; i != n; ++i){
        for (int j = 0; j != n; ++j){
            trans[j][i] = massive[i][j];
        }
    }
}

void matrix_print(int n, int (*m)[n]){
    for(int i = 0;i!=n;++i){
        putchar('\n');
        for (int j = 0; j != n; ++j){
            printf("%d ", m[i][j]);
        }
    }
}

void input_matrix(int n, int (*massive)[n]){
    for(int i = 0;i!=n;++i){
        for (int j = 0; j != n; ++j){
            scanf ("%02d", &massive[i][j]);
        }
    }
}

int is_identity_matrix(int n, int (*m)[n]){
    int ans = 1;
    for (int i = 0; i != n; ++i){
        if (ans == 0){
            break;
        }
        for (int j = 0; j != n; ++j){
            if (m[i][j] != 0){
                if((i != j) || (m[i][j] != 1)){
                    ans = 0;
                    break;
                }
            }
        }
    }
    return ans;
}

void product_two_matrices(int n, int (*factor1)[n], int (*factor2)[n], int (*product)[n]){
    for (int i = 0; i != n; ++i){
        for(int j = 0; j != n; ++j){
            product[i][j] = 0;
            for (int k = 0; k != n; ++k){
                product[i][j] += factor1[i][k] * factor2[k][j];
            }
        }
    }
}

int main(){
    int n;
    int massive[N * N];
    int trans[N * N];
    int product[N * N];
    scanf("%d", &n);
    input_matrix(n, (int (*)[n]) massive);
    to_transposed(n, (int (*)[n]) massive, (int (*)[n]) trans);
    product_two_matrices(n, (int (*)[n]) massive, (int (*)[n]) trans, (int (*)[n]) product);
    printf("%d\n", is_identity_matrix(n, (int (*)[n]) product));
}
```
<b>Тесты:</b>
```
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"zlaba15"
4
1 0 0 0
0 1 0 0
0 0 1 0
0 0 0 1
YES
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"zlaba15"
4
1 0 0 1
0 1 0 0
0 0 0 1
1 0 0 0
NO
demagog@demagog-VivoBook-ASUSLaptop-X509BA-D509BA:~/Загрузки$ ./"zlaba15"
4
0 0 0 1
0 0 1 0
1 0 0 0
0 1 0 0
YES
```

## 11. Выводы

Были приобретены навыки обработки матриц на языке Си, было выяснено, как устроена матрица в Си.

Недочёты при выполнении задания могут быть устранены следующим образом: —

Подпись студента _________________


