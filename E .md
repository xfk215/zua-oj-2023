
# 韩信点兵

```c++
#include<iostream>
#include<cmath>
using namespace std;
int cnt;
bool flag;
int main()
{
    int a,b,c;
     while(cin>>a>>b>>c)
     {
        flag=false;
         cnt++;
         int i=0;
         for(i=10;i<=100;i++)
         {
             if(i%3==a&&i%5==b&&i%7==c)
             {
                 flag=true;
                printf("Case %d: %d\n",cnt,i);
             }
         }
         if(!flag)printf("Case %d: No answer\n",cnt);
     }
}

```
