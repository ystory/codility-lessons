```java
// you can also use imports, for example:
// import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int[] solution(int[] A, int K) {
        // write your code in Java SE 8
        final int n = A.length;
        final int[] rotated = new int[n];
        
        for (int i = 0; i < n; i++) {
            rotated[(i + K) % n] = A[i];
        }
        
        return rotated;
    }
}
```
