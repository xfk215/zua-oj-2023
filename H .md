#include<iostream>
#include<algorithm>
#include<cstring>
using namespace std;
char str[100];
int main()
{
    scanf("%s",str);
    int len=strlen(str);
    for(int i=1;i<=len;i++)
    {
        if(len%i==0)
        {
            bool flag=true;
            for(int j=i;j<len;j++)
             {
                if(str[j]!=str[j%i])
                {
                    flag=false;
                    break;
                }
            }
            if(flag==true)
            {
                cout<<i<<endl;
                break;
            }
        }
    }
}