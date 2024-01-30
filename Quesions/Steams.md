# Streams

## Task 15.7.2

Каков результат выполнения данного кода?

```java
public static void main(String[] args) {
   Stream<String> stream = Stream.iterate("", (s) -> s + "1");
   System.out.println(stream.limit(2).map(x -> x + "2"));
}
```

- 12112
- 212
- 212112
- +Будет вызван метод toString на объекте типа Stream.
- Код не компилируется.
- Будет выброшено исключение при запуске.

---

## Task 15.7.4

Какой из следующих фрагментов кода мы можем добавить после данного кода, чтобы при запуске не было ошибок и не было записей в консоли?

```java
LongStream ls = LongStream.of(1, 2, 3);
OptionalLong opt = ls.map(n -> n * 10).filter(n -> n < 5).findFirst();
```

Может быть несколько правильных вариантов

- ```java
  if (opt.isPresent()) System.out. println(opt.get());
  ```

- ```java
  //+
  if (opt.isPresent()) System.out.println(opt.getAsLong());
  ```

- ```java
  opt.ifPresent(System.out.println)
  ```

- ```java
  //+
  opt.ifPresent(System.out::println);
  ```

- Ничего. Код не скомпилируется.

- Ничего. Код на последней строчке бросит ошибку в Runtime.

---

## Task 15.7.5

Какой из следующих фрагментов кода мы можем добавить в пропущенное место, чтобы код напечатал в консоль false?

```java
Stream<String> s = Stream.generate(() -> "meow");
boolean match = s._________(String::isEmpty);
System.out.println(match);
```

- +allMatch
- anyMatch
- findAny
- findFirst
- noneMatch
- Ничего из вышеперечисленного.
- верно
