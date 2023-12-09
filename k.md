#include <iostream>
#include <vector>
#include <algorithm>

using namespace std;

struct p
{
	int vote;
	int index;
};

bool c(p a, p b)
{
	return a.vote > b.vote;
}

int main()
{
	int n, k;
	cin >> n >> k;
	
	vector<p> v(n);
	
	for (int i = 0; i < n; i++)
	{
		int x;
		cin >> x;
		v.push_back({x,i+1});
	}
	
	sort(v.begin(), v.end(), c);
	for(int i=0;i<k;i++){
		cout<<v[i].index<<" ";
	}
	
	return 0;
}