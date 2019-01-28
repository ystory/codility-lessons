```java
// you can also use imports, for example:
// import java.util.*;

// you can write to stdout for debugging purposes, e.g.
// System.out.println("this is a debug message");

class Solution {
    public int solution(int[] A) {
        // write your code in Java SE 8
        final int[] totalSum = new int[A.length];
        totalSum[0] = A[0];
        for (int i = 1; i < A.length; i++) {
            totalSum[i] = totalSum[i-1] + A[i];
            // System.out.println(totalSum[i]);
        }
        
        int min = Integer.MAX_VALUE;
        for (int i = 0; i < A.length - 1; i++) {
            int difference = totalSum[i] - (totalSum[A.length -1] - totalSum[i]);
            // System.out.println(difference + "@@#");
            if (difference < 0) {
                difference *= -1;
            }
            if (difference < min) {
                min = difference;
            }
        }
        return min;
    }
}
```
