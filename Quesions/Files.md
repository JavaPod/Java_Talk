# Files

**7/11   15.6. Работа с файлами**

## 1. Path initialization

**URI**: http://..., file://..., https://..., ftp://...

### Example

```java
Path path1 = Paths.get(new URI("file:///c:/zooinfo/November/employees.txt"));
Path path2 = Paths.get(new URI("http://www.wiley.com"));
```

#### My question

why the 'file' URI requires *three* slashes?

---

## 2. Large files

### Example

```java
import java.nio.file.Path;
import java.nio.file.Paths;

Path path = Paths.get("fish/sharks.log");
try {
   List<String> lines = Files.readAllLines(path);
   for (String line : lines) {
       System.out.println(line);
   }
} catch (IOException exception) {
   // Handle file I/O exception
}
```

Будьте внимательны: если вы прочитаете очень большой файл, то вы рискуете заполнить всю выделенную память для вашей JVM и будет выброшено OutOfMemoryError.

#### My Question

How to efficiently read and process a large file in Java, especially when the file size exceeds the available memory?
