#include <iostream>
#include <map>
using namespace std;

int main() {
    int n;
    while (cin >> n) {
        map<int, int> count;
        int num;
        for (int i = 0; i < n; i++) {
            cin >> num;
            count[num]++;
        }
        for (auto it : count) {
            if (it.second >= (n + 1) / 2) {
                cout << it.first << endl;
                break;
            }
        }
    }
    return 0;
}