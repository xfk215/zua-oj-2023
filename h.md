
# 求最大连续子序列之和

```c++
#include<iostream>
#include<vector>
using namespace std;
int main()
{
    int n,cnt;
    int max_sum,t;
    while(cin>>n,n!=0){
        max_sum=t=0;
        vector<int> v(n);
        for(int i=0;i<n;i++){
            cin>>v[i];
            t+=v[i];
            if(t>max_sum){
                max_sum=t;
            }
            if(t<0){
                t=0;
            }
            if(v[i]<0){
                cnt++;
            }
        }
        cout<<max_sum<<endl;
    }
    return 0;
}

```
