#include<iostream>
#include<vector>
using namespace std;

int main()
{
	int t,cnt;
	cin>>t;
	for(int i=0;i<t;i++){
		int n;
		cin>>n;
		vector<vector<int>> v(n,vector<int>(2));
		cin>>v[0][0]>>v[0][1];
		cnt=1;
		for(int j=1;j<n;j++){
			cin>>v[j][0]>>v[j][1];
			if(v[j][0]<v[j-1][1]){
				cnt++;
			}
		}
		cout<<cnt*5<<endl;
	}
	return 0;
}