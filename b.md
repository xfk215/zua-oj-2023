
# 绝对值排序

```c++
#include <vector>
#include <iostream>
#include <cmath>
#include <algorithm>
using namespace std;
bool c(int a, int b)
{
    return abs(a) < abs(b);
}
int main()
{
	int n;
	while (cin >> n && n)
	{
		vector<int> a(n);
		for (int i = 0; i < n; i++)
		{
			cin >> a[i];
		}
		sort(a.begin(), a.end(), c);
		for (int i = n - 1; i >= 0; i--)
		{
			cout << a[i] << " ";
		}
		cout << endl;
	}
    return 0;
}

```
