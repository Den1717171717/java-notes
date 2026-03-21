# 05 — Многопоточность в Java

## Создание потока

```java
// Способ 1: extends Thread
class MyThread extends Thread {
    public void run() {
        System.out.println("Поток: " + Thread.currentThread().getName());
    }
}
new MyThread().start();

// Способ 2: Runnable (предпочтительно)
Thread t = new Thread(() -> System.out.println("Lambda-поток"));
t.start();
```

## ExecutorService

```java
ExecutorService executor = Executors.newFixedThreadPool(4);
executor.submit(() -> System.out.println("Задача выполнена"));
executor.shutdown();
```

## synchronized

```java
public synchronized void increment() {
    count++;
}

// Или через блок
synchronized (this) {
    count++;
}
```

## volatile и AtomicInteger

```java
// volatile — видимость изменений между потоками
private volatile boolean running = true;

// AtomicInteger — атомарные операции без synchronized
AtomicInteger counter = new AtomicInteger(0);
counter.incrementAndGet();
```

## Состояния потока

```
NEW → RUNNABLE → RUNNING → BLOCKED/WAITING → TERMINATED
```
