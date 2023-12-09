
# aabb

```c++
#include<iostream>
#include<cmath>
using namespace std;
int main()
{
    for(int i=1;i<=9;i++){
        for(int j=0;j<=9;j++){
        int num=1100*i+11*j;
        int res=sqrt(num);
        if(res*res==num)
        {
            cout<<num<<endl;
        }
        }
    }
}

```
