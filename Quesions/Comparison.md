# Java Type System

## Comparison

### Example

```java
public class Product {
    private String name;
    private double price;

    public Product(String name, double price) {
        this.name = name;
        this.price = price;
    }

    @Override
    public boolean equals(Object o) {
        if (this == o) return true; // References are equal - objects are equal
        if (o == null || this.getClass() != o.getClass()) return false;
        Product product = (Product) o; // Why is casting necessary?
        return Double.compare(product.price, price) == 0 &&
               name.equals(product.name);
    }
}
```

#### Questions

1. **'==' vs. 'equals'**:
   What's the distinction?

2. **Overriding 'equals'**
   Why is it a recommended for custom objects?

3. **'equals' and 'hashCode'**
    Why should they be overridden together?

4. **Floating-point**:
   What problems may arise, and how to avoid them?

5. **Double values comparison**:
   Why use `Double.compare` instead of '=='

6. **Special cases in Double.compare**
   How does it deal with
   - NaN,
   - positive infinity and negative infinity?

7. **Casting 'o' to Product type**
    Why is it necessary?
