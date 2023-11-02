# Generics

## Wildcards

### Examples

```java
// 1
HashSet<Number> hs = new HashSet<Integer>();

```

```java
// 2
HashSet<? super ClassCastException> set = new HashSet<Exception>();
```

```java
// 3
List<Object> values = new HashSet<Object>();
```

```java
// 4
List<? extends Object> objects = new ArrayList<Object>();
```

#### Questions

1. **Compile successfully** snippets:
  Which of these snippets compile successfully?
1. **Fail to compile** snippet:
    - Why do the others fail?
    - How to fix them?
2. **`? super` vs. `? extends`**
  What is the difference between `? super` and `? extends`
