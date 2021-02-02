#include <cmath>
#include <cstdio>
#include <vector>
#include <iostream>
#include <algorithm>
#include <cstdlib>
#include <bits/stdc++.h>
using namespace std;
using ll=long long;
ll fact(ll n)
{
    if(n==0||n==1)
    {
        return 1;
    }
    return n*fact(n-1);
}

ll g(ll n)
{
    ll i,j,k=0,sum,sum1;
    for(i=1;i!=0;i++)
    {
        sum=0,sum1=0;
        k=i;
        while(k>0)
        {
            sum=sum+fact(k%10);
            //cout<<fact(k%10)<<endl;
            k=k/10;
        }
        k=sum;
        while(k>0)
        {
            sum1=sum1+k%10;
            k=k/10;
        }
        if(sum1==n)
        {
            //cout<<i<<endl;
             return i;
        }
    }
    return 0;
}
