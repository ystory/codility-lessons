```java
// you can also use imports, for example:
// import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int solution(int[] A) {
        // write your code in Java SE 8
        final long n = A.length + 1;
        int sum = 0;
        for (int num : A) {
            sum += num;
        }
        
        // System.out.println(sum + ":" + ((n + 1) * n / 2));
        return (int) (((n + 1) * n / 2) - sum);
    }
}
```
