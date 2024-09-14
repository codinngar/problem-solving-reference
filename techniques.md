# Techniques for problem solving

<br><br>

## Table of contents
- [Frequency Array](#frequency-array)
- [Prefix Sum](#prefix-sum)
- [Partial Sum](#partial-sum)

<br><br>

## Frequency Array
> Use this technique when you want to know how many times a number has been repeated or to check if the number exists or not.
```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    // n = Size of the array
    // mx = Minimum number in constrains
    // fa = Frequency array
    int n,mx=-1e9;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
        if(arr[i]>mx) mx=arr[i];
    }
    int fa[mx+1]{0};
    for (int i=0;i<n;i++) fa[arr[i]]++;
    return 0;
}
```

<br><br>

## Prefix Sum
> Use this technique when you want to get the sum of a range quickly instead of looping for the whole array.
```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    // n = Size of the array
    int n;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++) cin>>arr[i];
    for(int i=1;i<n;i++) arr[i]+=arr[i-1];
    return 0;
}
```

<br><br>

## Partial Sum
> Use this technique when you want to add a number from start index to end index for an array of zeros.
```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    // n = Size of the array
    // l = Start index
    // r = End index
    // k = The number to be added to the range
    int n,l,r,k;
    cin>>n>>l>>r>>k;
    int arr[n+9]{0};
    arr[l]+=k;
    arr[r+1]-=k;
    for(int i=1;i<n;i++) arr[i]+=arr[i-1];
    return 0;
}
```
