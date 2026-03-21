# 04 — Исключения в Java

## Иерархия

```
Throwable
├── Error         (не перехватываем: OutOfMemoryError)
└── Exception
    ├── Checked   (нужно обрабатывать: IOException, SQLException)
    └── Unchecked (RuntimeException: NullPointerException, ArrayIndexOutOfBoundsException)
```

## Обработка

```java
try {
    int result = 10 / 0;
} catch (ArithmeticException e) {
    System.out.println("Ошибка: " + e.getMessage());
} catch (Exception e) {
    System.out.println("Общая ошибка: " + e.getMessage());
} finally {
    System.out.println("Выполняется всегда");
}
```

## Своё исключение

```java
public class MyException extends RuntimeException {
    public MyException(String message) {
        super(message);
    }
}

// Использование
throw new MyException("Что-то пошло не так");
```

## try-with-resources

```java
try (BufferedReader br = new BufferedReader(new FileReader("file.txt"))) {
    String line = br.readLine();
} catch (IOException e) {
    e.printStackTrace();
} // br закроется автоматически
```
