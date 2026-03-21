# 03 — Коллекции Java

## Иерархия

```
Collection
├── List       → ArrayList, LinkedList
├── Set        → HashSet, TreeSet, LinkedHashSet
└── Queue      → PriorityQueue, ArrayDeque

Map            → HashMap, TreeMap, LinkedHashMap
```

## Примеры

```java
// ArrayList
List<String> list = new ArrayList<>();
list.add("Java");
list.add("Python");
list.get(0); // "Java"

// HashMap
Map<String, Integer> map = new HashMap<>();
map.put("один", 1);
map.put("два", 2);
map.get("один"); // 1

// Итерация
for (Map.Entry<String, Integer> entry : map.entrySet()) {
    System.out.println(entry.getKey() + " = " + entry.getValue());
}

// Stream API (Java 8+)
list.stream()
    .filter(s -> s.startsWith("J"))
    .forEach(System.out::println);
```

## Когда что использовать

| Структура | Когда использовать |
|-----------|-------------------|
| `ArrayList` | Быстрый доступ по индексу |
| `LinkedList` | Частые вставки/удаления в середину |
| `HashSet` | Уникальные элементы, порядок не важен |
| `TreeSet` | Уникальные элементы, нужна сортировка |
| `HashMap` | Пары ключ-значение, быстрый поиск |
| `TreeMap` | Пары ключ-значение, ключи отсортированы |
