#include<stdio.h>
int isComplete(int n);
int main()
{
	int n,n1,n2,count=0;
	scanf("%d %d",&n1,&n2);
	for(n=n1;n<=n2;n++)//完数个数 
	{
		if(isComplete(n)==1)
		count++;
	}
	printf("%d",count);
	return 0;
}
int isComplete(int n)//int可以不加 
{
	int sum=1;//细节处理：1是任何一个数的因子
	for(int i=2;i<n;i++)
	{
		if(n%i==0)
	    sum+=i;	
	}
	if(sum==n)
	return 1;
	else
	return 0; 
}
