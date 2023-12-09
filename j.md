#include<iostream>

using namespace std;

int main()
{
	int n,m;
	int cnt=0;
	cin>>n>>m;
	for(int i=n;i<m+1;i++){
		if(i%6==0&&i%7!=0){
			cnt++;
		}
	}
	cout<<cnt;
	return 0;
}