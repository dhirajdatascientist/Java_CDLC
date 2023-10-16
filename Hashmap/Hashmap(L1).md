## HashMap(L1)

A HashMap is a versatile data structure in Java that offers a powerful way to store and retrieve data efficiently. Here are ten simple points about `HashMap`:

1. **Key-Value Pairs**: HashMap stores data in key-value pairs. Each key maps to exactly one value. The key acts as an index to retrieve the value.

2. **Unordered Collection**: The entries in a HashMap are not ordered by their keys or values, which means there's no guarantee on the order of entries.

3. **Allows One Null Key**: HashMap can store one null key and multiple null values.

4. **Not Synchronized**: It is not thread-safe by default, which means multiple threads can access it simultaneously and lead to data inconsistency.

5. **O(1) Average Time Complexity**: For the basic operations like `get` and `put`, assuming the hash function distributes the entries evenly among the buckets.

6. **Resizable**: The backing array (bucket) size can be automatically increased when the number of entries exceeds a threshold.

7. **Hashing Mechanism**: It uses the `hashCode` method of keys to determine their bucket location. If two keys have the same hash code, they are placed in the same bucket but as separate entries (chaining).

8. **Replacement for Arrays and Lists**: When direct access and updates are needed based on a key, rather than an index or sequential search.

9. **Replaceable Hashing**: Allows for custom hash functions through overriding the `hashCode` method.

10. **Initial Capacity and Load Factor**: You can specify the initial capacity and load factor. The load factor determines when the map will be resized based on a percentage of the capacity.

**Simple Example**:
```java
import java.util.HashMap;

public class HashMapExample {
    public static void main(String[] args) {
        // Create a new HashMap
        HashMap<String, Integer> scores = new HashMap<>();

        // Add some scores
        scores.put("Alice", 85);
        scores.put("Bob", 90);
        scores.put("Charlie", 88);

        // Retrieve a score
        int aliceScore = scores.get("Alice");  // Outputs: 85
        System.out.println("Alice's Score: " + aliceScore);

        // Check if a key exists
        boolean hasBob = scores.containsKey("Bob");  // Outputs: true
        System.out.println("Has Bob's Score? " + hasBob);

        // Remove an entry
        scores.remove("Bob");

        // Print all key-value pairs
        for (String key : scores.keySet()) {
            System.out.println(key + ": " + scores.get(key));
        }
    }
}
```

