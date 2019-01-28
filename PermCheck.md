```java
// you can also use imports, for example:
// import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");
import java.util.HashSet;
import java.util.Set;

class Solution {
    public int solution(int[] A) {
        // write your code in Java SE 8
        final Set<Integer> elements = new HashSet<>();

        for (final int num : A) {
            if (num > A.length || elements.contains(num)) {
                return 0;
            }
            elements.add(num);
        }
        return 1;
    }
}
```
