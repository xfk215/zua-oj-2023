#include <iostream>
#include <cstdio>
#include <cstdlib>
#include <cstring>
char s[20],buff[100];
int cnt;
using namespace std;
int main()
{
    scanf("%s",s);
	
	for(int abc=100;abc<=999;abc++)
	{
	 for(int de=10;de<=99;de++)
	 {
	     int mid1=abc*(de%10);
	     int mid2=abc*(de/10);
	     int res=abc*de;
	     sprintf(buff,"%d%d%d%d%d",abc,de,mid1,mid2,res);
	     int flag=1;
	     for(int i=0;i<strlen(buff);i++)
	      {
	          if(strchr(s,buff[i])==NULL)
	          {
	              flag=0;
	              break;
	          }
	      }
	      if(flag) 
	      {
	          printf("<%d>\n%5d\nX%4d\n-----\n%5d\n%4d\n-----\n%5d\n\n",++cnt,abc,de,mid1,mid2,res);
	      }
	 }
	}
	 printf("The number of solutions=%d",cnt);
}