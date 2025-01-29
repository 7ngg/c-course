# Строки

Мы уже знаем, что есть тип данных `char`, который может содержать один символ (ASCII).

`Строка` - массив из таких `char` cимволов. Определяется абсолютно так же, как массив друго типа данных, т.е:

```c
// символ
char c = 'a';
// строка (массив символов)
char str[] = "Hello";
```

При определении строки, все символы хранятся последовательно. Чтобы определять конец строки, используется символ `\0` - нуль терминатор.

Для вывода или ввода строк используется символ `%s`

## Методы строк

- `strlen` - string length - длина строки (количество символов до нуль-терминатора)
- `strcmp` - string compare - функция для сравнения строк. `0`, если строки равны, `-1` иначе
- `strcpy` - string copy - функция, для копировния или перемещения строк
- `strcat` - string concatenate - функция, для объединения строк
- `strstr` - string substring - функция, для поиска подстроки

```c
#include <stdio.h>
#include <string.h>

int main() {
  char str[] = "Hello"; // -> Hello\0
  printf("size: %llu\n", sizeof(str));
  printf("%s\n", str);

  char inputStr[10];
  /*scanf("%s", inputStr);*/
  /*printf("%s\n", inputStr);*/

  // Размер строки - количество символов до нуль-терминатора
  /*printf("size: %llu\n", strlen(inputStr));*/

  // Сравнение строк
  printf("%d\n", strcmp(str, inputStr));

  // Копирование строк
  // inputStr = str; - так делать нельзя
  strcpy(inputStr, str);
  printf("Input str = %s\n", inputStr);

  // Объединение строк
  strcat(inputStr, str);
  printf("Input str = %s\n", inputStr);

  // Поиск подстроки
  char* c = strstr(inputStr, "magomed");
  printf("%p\n", c);

  char some[32] = "some string";
  printf("sizeof = %llu\n", sizeof(some));
  printf("strlen = %llu\n", strlen(some));

  return 0;
}
```
