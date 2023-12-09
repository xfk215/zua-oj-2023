
# 竖式问题

```c++
#include<iostream>
#include<cstring>
#include<algorithm>
using namespace std;
char buff[100],s[100];
int main()
{
    scanf("%s",s);
    int cnt=0;
    for(int abc=100;abc<=999;abc++)
        for(int de=10;de<=99;de++){
         bool flag=false;
         int res=abc*de;
         int num1=abc*(de%10);
         int num2=abc*(de/10);
         sprintf(buff,"%d%d%d%d%d",abc,de,num1,num2,res);
         for(int i=0;i<strlen(buff);i++)
         {
             if(strchr(s,buff[i])==NULL)
             {
                flag=true;
                break;
             }
         }
         if(!flag)
         {
              cnt++;
                 printf("<%d>\n",cnt);
                 printf("%5d\n",abc);
                 printf("X%4d\n",de);
                 printf("-----\n");
                 printf("%5d\n",num1);
                 printf("%4d\n",num2);
                 printf("-----\n");
                 printf("%5d\n",res);
                cout<<endl;
         }   
     }
 
     printf("The number of solutions=%d\n",cnt);
}

```
