In [[Java]], ConcurrentHashMap is a **thread-safe** implementation of the `Map` interface that allows **concurrent read and write operations** without locking the entire map.

It is part of the `java.util.concurrent` package and is designed for **high-performance multi-threaded applications**.

ConcurrentHashMap is similar to [[HashMap]], with the skill to multi-threading.

```Java
import java.util.concurrent.ConcurrentHashMap;

public class ConcurrentHashMapExample {
    public static void main(String[] args) {
        // Create a ConcurrentHashMap
        ConcurrentHashMap<String, Integer> map = new ConcurrentHashMap<>();

        // Put values
        map.put("Apple", 3);
        map.put("Banana", 5);

        // Update value atomically
        map.computeIfPresent("Apple", (key, val) -> val + 2);

        // Add value if absent
        map.putIfAbsent("Orange", 4);

        // Read values
        System.out.println("Apple count: " + map.get("Apple"));
        System.out.println("Map: " + map);

        // Remove a key
        map.remove("Banana");

        System.out.println("After removal: " + map);
    }
}

```