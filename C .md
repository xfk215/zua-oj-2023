
# 3n+1问题

```c++
#include <iostream>
using namespace std;
int main()
{
	ll n;
	cin>>n;
	while(n>1)
	{
	    if(n%2==0)
	    {
	        n/=2;
	        cnt++;
	    }
	    else
	    {
	        n=(3*n+1)/2;
	        cnt+=2;
	    }
	}
	cout<<cnt<<endl;    
}

```