# Type safety

## Compile error

### Example

```java
public static void main(String[] args) {
   List list = new ArrayList();
   list.add("One");
   list.add("Two");
   list.add(7); // Compile error
   for (String s : list) {
       System.out.println(s);
   }
}
```

#### Questions

1. **Compile error**:
   Why does it occur?
2. **Fix**:
   How to fix it?
3. **Store different types**:
    How to store elements of different types in a list?
4. **Retrieve different types**:
    How to retrieve elements of different types from a list?
