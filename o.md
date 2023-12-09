
# 小H分糖果

```c++
#include<iostream>
#include<vector>
using namespace std;

int Lx(vector<int> v){
	int n=v.size();
	vector<int> dp(n,1);
	for(int i=1;i<n;i++){
		if(v[i]>v[i-1]){
			dp[i]=dp[i-1]+1;
		}
	}
	
	for(int i=n-2;i>=0;i--){
		if(v[i]>v[i+1]){
			dp[i]=dp[i+1]+1;
		}
	}
	int sum=0;
	for(auto val:dp){
		sum+=val;
	}
	return sum;
}

int main()
{
	int n;
	cin>>n;
	vector<int> v(n);
	for(int i=0;i<n;i++){
		cin>>v[i];
	}
	int res=Lx(v);
	cout<<res<<endl;
	return 0;
}

```
