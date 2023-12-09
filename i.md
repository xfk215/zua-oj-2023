
# 闹铃何时会响？

```c++
#include<iostream>

using namespace std;

int main()
{
    int ct,tt;
    int t;
    cin>>ct>>tt; 
    t=tt-ct;
    if(t<0){
        t=24+t;
    }
    cout<<t;
    return 0;
}

```
