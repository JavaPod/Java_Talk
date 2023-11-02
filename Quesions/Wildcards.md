# Generics

## Wildcards

### Examples

- 1

```java
HashSet<Number> hs = new HashSet<Integer>();
```

- 2

```java
List<Object> values = new HashSet<Object>();
```

- 3

```java
HashSet<? super ClassCastException> set = new HashSet<Exception>();
```

- 4

```java
List<? extends Exception> list = new ArrayList<IOException>();
```

- 5

```java
List<? extends Object> objects = new ArrayList<Object>();
```

#### Questions

1. **Compile successfully** snippets:
  Which of these snippets compile successfully?
2. **Fail to compile** snippet:
    - Why do the others fail?
    - How to fix them?
3. **`? super` vs. `? extends`**
  What is the difference between `? super` and `? extends`
