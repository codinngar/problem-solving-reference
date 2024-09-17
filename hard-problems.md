# Hard Problems Solutions

<br><br>

### Table of contents
- [Maximum Subarray Sum](#maximum-subarray-sum)
- [Prime Numbers](#prime-numbers)

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

<br><br>

## Prime Numbers

```c++
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n=7;
    bool p=true;
	if(n<=1) p=false;
	for(int i=2;i<=sqrt(n);i++)
	{
		if(n%i==0) p=false;
	}
    p ? cout<<n<<" is prime." : cout<<n<<" is not prime.";
}
```

