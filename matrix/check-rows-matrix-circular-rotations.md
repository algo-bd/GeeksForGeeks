## [Matrix Circular Rotation](http://www.geeksforgeeks.org/check-rows-matrix-circular-rotations/)

```c++
#include <bits/stdc++.h>
using namespace std;

#define MAX 4

bool  isPermutedMatrix(int mat[MAX][MAX], int n) {
	string s = "";
	for (int i = 0; i < MAX; i++) {
		if (i == 0) {
			s += std::to_string(mat[0][i]);
		}
		else {
			s += "-" + std::to_string(mat[0][i]);
		}
	}

	s = s + "-" + s;

	bool isPermuted = false;

	for (int row = 1; row < MAX; row++) {
		int flag = 0;
		int counter = 0;
		for (int column = 0; column < MAX; column++) {
			string c = std::to_string(mat[row][column]);

			for (unsigned int k = flag; k < s.length(); k++) {
				if (c[0] == s[k]) {
					flag = k;
					counter = counter + 1;
					break;
				}
			}
		}
		if (counter == MAX) {
			isPermuted = true;
			counter = 0;
		}
		else {
			isPermuted = false;
			return false;
		}
	}
	return isPermuted;
}


int main() {

	//freopen("input.txt", "r", stdin);
	//freopen("output.txt", "w", stdout);	

	int n = 4;
	int mat[MAX][MAX] = {
		{ 1, 2, 3, 4 },
		{ 4, 1, 3, 2 },
		{ 3, 4, 1, 2 },
		{ 2, 3, 4, 1 }
	};
	isPermutedMatrix(mat, n) ? cout << "Yes" : cout << "No";

	getchar();
	return 0;
}
```
