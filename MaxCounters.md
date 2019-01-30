```java
// you can also use imports, for example:
// import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int[] solution(int N, int[] A) {
        // write your code in Java SE 8
        final int[] opts = new int[N];
        int max = 0;
        int maximize = 0;
        
        for (final int idx : A) {
            if (idx <= N) {
                
                int current = Math.max(maximize, opts[idx-1]);
                opts[idx-1] = current + 1;
                max = Math.max(opts[idx-1], max);
                // System.out.println("max : " + max + ", opts : " + opts[idx]);
            } else {
                maximize = max;
                /*
                for (int i = 0; i < N; i++) {
                    opts[i] = max;
                }
                */
            }
        }
        
        for (int i = 0; i < N; i++) {
            opts[i] = Math.max(maximize, opts[i]);
        }
        return opts;
    }
}
```
