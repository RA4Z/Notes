In [[Java]], a collection is an in-memory data structure that stores elements. All elements must exist before being added and you can perform operations like `search`, `sort`, `insert`, `update` or `delete`.
Examples: `List`, `Set`, `Queue`, `ArrayList`, `LinkedList`, `HashSet`, etc.

#### Example
```Java
import java.io.*;
import java.util.*;

class GfG {

    public static void main(String[] args)
    {
        // Creating an instance of list
        List<String> companyList = new ArrayList<>();

        // Adding elements using add() method
        companyList.add("Google");
        companyList.add("Apple");
        companyList.add("Microsoft");

        // Now creating a comparator
        Comparator<String> com = (String o1, String o2) -> o1.compareTo(o2);

        // Sorting the list
        Collections.sort(companyList, com);

        // Iterating using for each loop
        for (String name : companyList) {
            System.out.println(name);
        }
    }
}
```

| **Collections**                                          |
| -------------------------------------------------------- |
| Store and hold data in structures like List, Set or Map. |
| Do not use functional interfaces directly.               |
| Reusable can be traversed multiple times.                |
| Mostly sequential, parallelism requires extra effort.    |
| Belong to java.util package (e.g., List, Set, Queue).    |
| Modifiable, elements can be added or removed.            |
| External iteration (using loops/iterators).              |