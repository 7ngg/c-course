# Циклы

`Цикл` - мезанизм в языке программирования, который позволяет выполнить некоторое действие несколько раз в зависимости от условия

В языке `C` существуют следующие виды циклов: `for`, `while`, `do while`

## While

Цикл `while` проверяет условие и переходит к выполнению тела цикла, если условие - истина

```c
// while (statement) { body }
while (true) {
    printf("Doing some job");
}

while (false) {
    printf("Doing some job");
}

int i = 10;
while (i > 0) {
    printf("i = %d", i);
    i--;
}
```

## Do while

Цикл `do while` сначала выполняет тело цикла, а потом проверяет условие

```c
// do { body } while (statement)
do {
    printf("Doing some job");
} while (true);

do {
    printf("Doing some job");
} while (false);

int i = 10;
do {
    printf("i = %d", i);
    i--;
} while (i > 0);
```

## For

Цикл `for` - это способ сократить запись при использовании цикла `while`. На деле он работает точно так же. Каждый из блоков цикла `for` можно опускать

```c
// for (init; statement; expression) { body }
for (int i = 10; i > 0; i--) {
    printf("i = %d", i);
}

for (;;) {
    printf("Doing some job");
}
```
