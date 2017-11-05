### [Print numbers from 1 to 100 without using loop](http://www.geeksforgeeks.org/how-will-you-print-numbers-from-1-to-200-without-using-loop/)

### Javascript
```js
function printNos(n) {
    if(n > 0){
        printNos(n-1);
        console.log(n);
    }
}
printNos(100);
```

### C++
```cpp
#include <stdio.h>

/* Prints numbers from 1 to n */
void printNos(unsigned int n)
{
    if(n > 0)
    {
        printNos(n-1);
        printf("%d ",  n);
    }
    return;
}

/* Driver program to test printNos */
int main()
{
    printNos(100);
    getchar();
    return 0;
}
```
