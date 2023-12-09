
# 今年暑假不AC

```c++
#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

int main() {
    while (true) {
        int n;
        cin >> n;
        if (n == 0) {
            break;
        }
        vector<pair<int, int>> gala;
        for (int i = 0; i < n; i++) {
            int st, et;
            cin >> st >> et;
            gala.push_back(make_pair(st, et));
        }
        sort(gala.begin(), gala.end(), [](const pair<int, int>& p1, const pair<int, int>& p2) {
            return p1.second < p2.second;
        });
        int count = 0;
        int et = 0;
        for (const pair<int, int>& p : gala) {
            int st = p.first;
            if (st >= et) { 
                count++;
                et = p.second;
            } 
        }
        cout << count << endl;
    }
    return 0;
}

```
