# Hard Problems Solutions

<br><br>

### Table of contents
- [Maximum Subarray Sum](#maximum-subarray-sum)

<br><br>

## Maximum Subarray Sum
```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++) cin>>arr[i];
    int maxSub=arr[0];
    int curSum=0;
    for(int i=0;i<n;i++)
    {
    	if(curSum<0) curSum=0;
    	curSum+=arr[i];
    	maxSub=max(maxSub,curSum);
    }
    cout<<maxSub;
    return 0;
}
```