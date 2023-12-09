#include<iostream>
#include<cmath>
typedef long long ll;
int cnt;
using namespace std;
int main()
{
     double res=0;
	int n,m;
	while(cin>>n>>m,n!=0&&m!=0)
	{
	    res=0;
	    cnt++;
	    for(ll i=n;i<=m;i++)
    	{
	         res+=(1.0)/(i*i);
    	}
	printf("Case %d: %.5lf\n",cnt,res);
	}
}