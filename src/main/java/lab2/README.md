# Lab 2
| Name:  | Student ID:  |
|--------|--------------|

## Part 1
```java
public Book(String argument[]) {
    /* construct the object with an array of chapter names */
    /* PLEASE ADD YOUR CODE HERE */

    chapters = new String[DEFAULT_CHAPTERS];

    for (int i = 0; i < (argument.length > chapters.length ? chapters.length : argument.length); i++)
        chapters[i] = argument[i];
    for (int i = (DEFAULT_CHAPTERS - 1); i >= argument.length; i--)
        chapters[i] = "n/a";
}
public String getChapter(int i) {
    /* return the chapter by the given index */
    /* PLEASE ADD YOUR CODE HERE */

    return chapters[i];
}
```

## Part 2
The way to fix the bug is adding `implements` to the class declaration of `MobileComputer`, changing it from `public class MobileComputer extends Computer {...}` to `public class MobileComputer extends Computer implements Chargeable {...}`.

By adding `implements`, a "can-do" relationship is established, allowing the method `Charger.charge()` that accepts the interface `Chargeable` to also accept the implementing class `MobileComputer`.