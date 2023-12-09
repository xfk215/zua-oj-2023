#include<iostream>
using namespace std;
int n;
int main()
{
	int n;
	cin>>n;
	cin.ignore();
	while(n--)
	{
		string s;
		getline(cin,s);
		int a[6]={0};
		for(unsigned int i=0;i<s.length();i++)
		{
			char c=tolower(s[i]);
			if(c=='a')a[0]++;
			else if(c=='e')a[1]++;
			else if(c=='i')a[2]++;
			else if(c=='o')a[3]++;
			else if(c=='u')a[4]++;
		}
		printf("a:%d\ne:%d\ni:%d\no:%d\nu:%d\n",a[0],a[1],a[2],a[3],a[4]);
		cout<<endl;
	}
}