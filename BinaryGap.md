```java
// you can also use imports, for example:
// import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int solution(int N) {
        // write your code in Java SE 8
        int gap = 0;
        boolean foundOne = false;
        
        for (int zeroCnt = 0; 0 < N; N /= 2) {
            if (N % 2 == 0) {
                zeroCnt++;
            } else {
                if (zeroCnt > gap && foundOne) {
                    gap = zeroCnt;
                }
                foundOne = true;
                zeroCnt = 0;
            }
        }
        
        return gap;
    }
}
```
