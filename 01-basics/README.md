# 01 — Основы Java

## Типы данных

| Тип | Размер | Пример |
|-----|--------|--------|
| `int` | 4 байта | `int x = 10;` |
| `long` | 8 байт | `long x = 100L;` |
| `double` | 8 байт | `double x = 3.14;` |
| `boolean` | 1 бит | `boolean b = true;` |
| `char` | 2 байта | `char c = 'A';` |
| `String` | объект | `String s = "hello";` |

## Управляющие конструкции

```java
// if-else
if (x > 0) {
    System.out.println("Положительное");
} else {
    System.out.println("Отрицательное");
}

// for
for (int i = 0; i < 10; i++) {
    System.out.println(i);
}

// while
while (x > 0) {
    x--;
}

// switch
switch (day) {
    case 1 -> System.out.println("Понедельник");
    case 2 -> System.out.println("Вторник");
    default -> System.out.println("Другой день");
}
```
