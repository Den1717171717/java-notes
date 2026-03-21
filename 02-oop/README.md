# 02 — ООП в Java

## Основные принципы

- **Инкапсуляция** — скрытие внутреннего состояния через `private` + геттеры/сеттеры
- **Наследование** — `extends` для классов, `implements` для интерфейсов
- **Полиморфизм** — один интерфейс, разные реализации
- **Абстракция** — `abstract` классы и интерфейсы

## Пример класса

```java
public class Animal {
    private String name;

    public Animal(String name) {
        this.name = name;
    }

    public String getName() { return name; }

    public void speak() {
        System.out.println(name + " говорит...");
    }
}

public class Dog extends Animal {
    public Dog(String name) { super(name); }

    @Override
    public void speak() {
        System.out.println(getName() + ": Гав!");
    }
}
```

## Интерфейсы vs Абстрактные классы

| | Интерфейс | Абстрактный класс |
|--|-----------|-------------------|
| Поля | только `static final` | любые |
| Конструктор | нет | есть |
| Множественное наследование | да | нет |
| Методы по умолчанию | `default` | обычные методы |
