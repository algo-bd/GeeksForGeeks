## [Calculate XOR from 1 to n](http://www.geeksforgeeks.org/calculate-xor-1-n/)
```cpp
#include <bits/stdc++.h>
using namespace std;

// Function to calculate xor
int computeXOR(int n)
{
    // If n is a multiple of 4
    if (n % 4 == 0)
        return n;
 
    // If n%4 gives remainder 1
    if (n % 4 == 1)
        return 1;
 
    // If n%4 gives remainder 2
    if (n % 4 == 2)
        return n + 1;
 
    // If n%4 gives remainder 3
    return 0;
}

int main()
{
    // [Naive Approach]
    for(int j = 1; j <= 20; j++)
    {
        int n = j;
        int result = 1;

        for(int i = 2; i <= n; i++)
        {
            result ^= i;
        }

        cout << j << " = " << result << endl;
    }
    
    // [Efficient Method]
    int n = 20;
    cout <<  "XOR From 1 to " << n << " = " << computeXOR(n);
    
    return 0;
}
```

## Sample Output
```sh
1 = 1
2 = 3
3 = 0
4 = 4
5 = 1
6 = 7
7 = 0
8 = 8
9 = 1
10 = 11
11 = 0
12 = 12
13 = 1
14 = 15
15 = 0
16 = 16
17 = 1
18 = 19
19 = 0
20 = 20
XOR From 1 to 20 = 20
```
