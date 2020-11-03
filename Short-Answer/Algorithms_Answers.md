#### Please add your answers to the ***Analysis of  Algorithms*** exercises here.

## Exercise I

a) The posed question involves an upper limit of n^3, but each step of the iteration increases a by n^2. Therefore, it will take n steps to complete, meaning this is O(n) time complexity

b) First we iterate on the range of n, an O(n) operation. In the inner loop we double the value of j until it reaches n, which indicates logarithmic speed, giving us a combined O(n * log(n)) time complexity.

c) Assuming only non-negative numbers of bunnies, this algorithm makes a single recursive call to itself, and reduces the remaining bunnies by 1 doing so. This is analogous to counting down to 0, giving us O(n) time

## Exercise II

Considering that f is a stable value, we can do better than to start from the bottom up until the egg breaks. What if no level breaks? What if all levels break? We may be motivated to check the endpoints first. Furthermore, if the egg breaks at some level, we know it will break at f + 1, f + 2, etc. If it doesn't break, it also won't break at f - 1, f - 2, etc. So, after checking the endpoints, we can cut into the middle of the building floors to see if it will break there. If it does break, we want to check the floors beneath us to find the lowest floor possible. If it doesn't break, we'll check the floors above too. Repeat with the remaining floors. In this way, we reduce the number of floors to check in half every step of the way. We stop when the floor above or below the previous floor has a different outcome (breaks/doesn't break), then f is the floor above (because below/above will determine if it breaks). Since we reduce the floors in half every time, this solution is O(log(n)), where n is the number of floors.
