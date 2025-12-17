Are an implementation of the `List` interface in [[Java]]

ArrayList uses a dynamic array to store elements. It provides fast random access as elements are stored in contiguous memory locations. ArrayList are ideal for scenarios where frequent `random access` or `search operations` are required.

ArrayList implements only the `List` interface, making it a simple list structure

#### Example
```Java
import java.util.ArrayList;
public class Main {
   public static void main(String[] args) {
       ArrayList<Integer> arrayList = new ArrayList<>();
       arrayList.add(1);
       arrayList.add(2);
       arrayList.add(3);
       System.out.println("ArrayList: " + arrayList);
   }
}
```

Use **ArrayList** for **read-heavy** operations