## [Diagonal Sum of Square Matrix](http://www.geeksforgeeks.org/sum-diagonals-spiral-odd-order-square-matrix/)
```c++
#include <iostream>

using namespace std;

int spiralDiaSum(int n) {
	if (n == 1)
		return 1;
	else return (4 * n* n - 6 * n + 6) + spiralDiaSum(n - 2);
}

int main() {
	int n = 7;
	cout << spiralDiaSum(n);
	getchar();
	return 0;
}
```
