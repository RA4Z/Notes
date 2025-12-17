In [[Java]], Streams are used to process collections of objects. It represents a sequence of elements and allows you to chain methods to produce results without changing the original collection.
#### Example
```Java
import java.io.*;

import java.util.*;

class GFG {
    public static void main(String[] args)
    {
        // Creating an empty Arraylist
        List<String> companyList = new ArrayList<>();

        // Adding elements to above ArrayList
        companyList.add("Google");
        companyList.add("Apple");
        companyList.add("Microsoft");

        // Sorting the list using sorted() method and  using for-each loop
        companyList.stream().sorted().forEach(
            System.out::println);
    }
}
```

| **Streams**                                                          |
| -------------------------------------------------------------------- |
| Do not store data, operate on source data (like Collections/Arrays). |
| Use functional style (lambdas, method references).                   |
| Consumable once used, must be recreated to traverse again.           |
| Support sequential and parallel processing.                          |
| Belong to java.util.stream package.                                  |
| Not modifiable, cannot add or remove elements.                       |
| Internal iteration (handled by the Stream API).                      |