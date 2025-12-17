A HashMap in [[Java]] stores items in **key/values pairs**, where each key maps to a specific value.

It is part of the `java.util` package and implements the `Map` interface.

#### Creating a HashMap
```java
import java.util.HashMap; // Import the HashMap class

HashMap<String, String> capitalCities = new HashMap<>();
```

#### Add Items
To add items to a `HashMap`, use the `put()` method:
```java
// Import the HashMap class
import java.util.HashMap;

public class Main {
  public static void main(String[] args) {
    // Create a HashMap object called capitalCities
    HashMap<String, String> capitalCities = new HashMap<String, String>();

    // Add keys and values (Country, City)
    capitalCities.put("England", "London");
    capitalCities.put("India", "New Dehli");
    capitalCities.put("Austria", "Wien");
    capitalCities.put("Norway", "Oslo");
    capitalCities.put("Norway", "Oslo"); // Duplicate
    capitalCities.put("USA", "Washington DC");

    System.out.println(capitalCities);
  }
}
```

#### Access an Item
To access a value in the `HashMap`, use the `get()` method and refer to its key:
```java
capitalCities.get("England");
```

#### Remove an Item
To remove an item, use the `remove()` method and refer to the key:
```java
capitalCities.remove("England");
```

To remove all items, use the `clear()` method:
```java
capitalCities.clear();
```