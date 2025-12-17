Are an implementation of the `List` interface in [[Java]]

LinkedList uses a **doubly linked list**, where each element contains data and references to the previous and next nodes. LinkedList is suited for applications with frequent **insertions** and **deletions**, especially at the beginning or middle of the list.

LinkedList implements both `List` and `Deque` interfaces, allowing it to function as a queue or deque.

#### Example
```Java
import java.util.LinkedList;
public class Main {
   public static void main(String[] args) {
       LinkedList<String> linkedList = new LinkedList<>();
       linkedList.add("A");
       linkedList.add("B");
       linkedList.addFirst("C");
       System.out.println("LinkedList: " + linkedList);
   }
}
```

Use **LinkedList** for **write-heavy** operations or when working with queues