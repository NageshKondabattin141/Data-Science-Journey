#Day 6 Time & Space Complexity  Mastery
##1. Objectives
-Time Complexity growth patterns
-Recursion Relations
-Recursion Tree Method
-Master Theorem Intuition
-Space Complexity in Recursion
-Trades-off Between Approach

##Time Complexity Basics
-Time complexity measures how the number of operations grows as input size n increases.
-It does NOT measure actual time.
-It measures growth rate.

##🔹 Common Growth Orders
###Complexity	Meaning	Example

-O(1)  ->  Constant	->   Dictionary lookup

-O(log n)	->  Logarithmic	->  Binary Search

-O(n)  ->  Linear  ->  Single loop

-O(n log n)  ->  Linearithmic  ->  Merge Sort

-O(n²)	->  Quadratic	->  Nested loops

-O(2ⁿ)  ->  Exponential  ->  Naive Fibonacci

##2. Linear Recurence

-Pattern 
 T(n)=T(n-1)+1

-Expansion
    T(n)
    = T(n-1) + 1
    = T(n-2) + 2
    = T(n-3) + 3
    ...
    = T(1) + (n-1)
    
-Conclusion
    Time = O(n)
    Depth of recursion n
    space = O(n)

##Logarithmic Recurence

-Pattern 
 T(n)=T(n/2)+1

-Expansion

    n -> n/2 -> n/4 -> ...
    
    Stops when
        n/2^k=1
        ->/2^k=n
        k=log n
        
-Conclusion
    Time = O(log n)
-Example = Binary Search

##4. Divide & Conquer – Balanced Case

-Pattern 
    T(n)= 2T(n/2)+n

-Recursion Tree Insight

    level 0  -> n
    level 1  -> n
    level 2  -> n

    Number of levels = log n
    so total = n * log n
    
-Conclusion
    Time = O(n log n)
-Example = Merge Sort

##5. Shrinking Work Case

-Pattern 

     T(n)=T(n/2)+n
     
-Recursion Tree

    level 0  ->  n
    level 1  ->  n/2
    level 2  ->  n/4

    Total = n + n/2  + n/4 + n/8 + ...
    Geometric series sum = 2n
    
-Conclusion
    Time = O(n)

##6. Exponential Growth

-Pattern

    T(n) = 2T(n-1) + 1
    
-Expands as : 
    1 + 2 + 4 + 8 +...

-Conclusion
    Time = O(2^n)
-Example =  Naive Fibonacci

##7. Master Theorem (Core Formula)

-General form:

    T(n) = aT(n/b) + f(n)

    -Step 1:
    Compute:
         n^(log_b a)

    -Step 2:
    Compare with f(n)
    
-Case 1:
    If
        f(n) = n^(log_b a)
        👉 O(n log n)

-Case 2:
    If
        f(n) < n^(log_b a)
        👉 O(n^(log_b a))
-Example:
        T(n) = 3T(n/2) + n
-Here:
        n^(log₂3) ≈ n^1.585
        
-So:
        👉 O(n^1.585)

-Case 3:
    If
        f(n) > n^(log_b a)
        👉 O(f(n))

-Example:

        T(n) = 2T(n/2) + n²

-Since  n² > n¹
        👉 O(n²)

##8. Space Complexity in Recursion

    Recursive stack depth determines space.

-Examples:
        Pattern 	Space
        T(n-1)	->   O(n)
        T(n/2)	->  O(log n)
        Memoization	 ->  O(n)
        Iterative  ->  O(1)
        
##9. Trade-Off Thinking

-Brute Force:
        O(n²)
        O(1) space

-Using Set:
        O(n)
        O(n) space

-Sorting Method:
        
        O(n log n)
        O(n) space (Python)

-👉 Optimization = trading space for time.

##10. Key Takeaways

✔ Understand growth, don’t memorize
✔ Always include cost of sorting
✔ Watch for hidden loops (count(), index())
✔ Hashing reduces time complexity
✔ Recursion depth = space complexity

##🧠 Reflection

-Today I moved from memorizing Big-O to deriving it using:

    -Recursion tree method
    -Geometric series reasoning
    -Master theorem comparison

-This improves analytical ability required for:
    
-Technical interviews
-Competitive coding

##Data structures optimization

###Algorithm design

###🚀 Foundation Status

-After this session, I can:
    ✔ Analyze recurrence relations
    ✔ Compare growth rates
    ✔ Understand divide & conquer
    ✔ Identify exponential explosion
    ✔ Think in terms of input scaling



