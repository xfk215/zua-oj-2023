
# Let the Balloon Rise

```c++
#include <iostream>
#include <map>
using namespace std;

int main() {
    int n;
    while (cin >>n) {
        if(n==0){
            break;
        }
        map<string, int> count;
        string color;
        for (int j = 0; j < n; j++) {
            cin >> color;
            count[color]++;
        }
        int maxCount = 0;
        string mColor;
        for (auto it : count) {
            if (it.second > maxCount) {
                maxCount = it.second;
                mColor = it.first;
            }
        }
        cout << mColor << endl;
    }
    return 0;
}

```
