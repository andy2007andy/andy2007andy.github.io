```c
#include<bits/stdc++.h>
#include<cstdio>
#include<iostream>
using namespace std;
int a[100500],d[100500];
int n,q,m;
int build(int s,int t,int p){
	if(s==t){
		d[p]=a[s];
		return d[p];
	}
	int m=s+((t-s)>>1);
	return d[p]=build(s,m,p*2)+build(m+1,t,p*2+1);
}
int main(){
	scanf("%d %d %d",&n,&q,&m);
	for(int i=1;i<=n;i++){
		scanf("%d",&a[i]);
	}
	build(1,n,1);
	for(int i=1;i<=q;i++){
		int temp,x,y,k;
		scanf("%d %d %d",&temp,&x,&y);
		if(temp==1){
			scanf("%d",&k);
		}
		else if(temp==2){
			scanf("%d",&k);
		}
		else{
		}
	}
	return 0;
}
```
