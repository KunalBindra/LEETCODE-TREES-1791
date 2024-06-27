# LEETCODE-TREES-1791
Your `findCenter` method in the `Solution` class aims to find the center of a star graph given its edges. A star graph is a graph where one central node is connected to all other nodes. The method works by examining the first two edges of the graph. Here's a step-by-step explanation of how your code works:

1. **Extract the Nodes**: You extract the nodes of the first two edges. 
   - `a` and `b` are the nodes of the first edge.
   - `c` and `d` are the nodes of the second edge.

2. **Determine the Center Node**: You then check if `a` is equal to either `c` or `d`. If so, `a` is the center node. Otherwise, `b` is the center node.

Here is your code for clarity:

```java
class Solution {
    public int findCenter(int[][] edges) {
        int a = edges[0][0], b = edges[0][1];
        int c = edges[1][0], d = edges[1][1];
        return a == c || a == d ? a : b;
    }
}
```

To confirm that your code is correct and runs without issues, you can run it with some test cases. Here is an example of how to test it:

```java
public class Main {
    public static void main(String[] args) {
        Solution solution = new Solution();
        
        // Example 1
        int[][] edges1 = {{1, 2}, {2, 3}, {4, 2}};
        System.out.println(solution.findCenter(edges1)); // Output: 2
        
        // Example 2
        int[][] edges2 = {{1, 3}, {2, 3}, {3, 4}};
        System.out.println(solution.findCenter(edges2)); // Output: 3
    }
}
```

You can place this `Main` class in the same file or a separate file to run the tests. The output should be the central node of the star graph for each set of edges.
