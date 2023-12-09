#include<stdio.h>
#define maxn 1010
int main(void)
{
    int n,i,j;
    int a[maxn],b[maxn];
    while(scanf("%d",&n)==1&&n)
    {
        int k;
        printf("Game %d:\n",++k);
        for(i=0;i<n;i++)
        {
            scanf("%d",&a[i]);
        }
        while(1)
        {
            int A=0,B=0,count=0;
            for(i=0;i<n;i++)
            {
                scanf("%d",&b[i]);
                if(a[i]==b[i]) A++;
                if(b[i]==0) count++;
            }
            if(count==n) break; 
            for(j=0;j<=9;j++)
            {
                int a1=0,a2=0;
                for(i=0;i<n;i++)
                {
                    if(a[i]==j) a1++;
                    if(b[i]==j) a2++;
                }
                if(a1<a2) B=B+a1;        
                else B=B+a2;          
            }
            printf("(%d,%d)\n",A,B-A); 
        }
    }
} 