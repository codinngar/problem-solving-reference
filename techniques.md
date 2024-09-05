# Techniques for problem solving

<br><br>

## Frequency Array
> Use this technique when you want to know how many times a number has been repeated or to check if the number exists or not.
```cpp
#include <bits/stdc++.h>
using namespace std;

int main()
{
    int n,mx=-1e9;
    cin>>n;
    int arr[n];
    for(int i=0;i<n;i++)
    {
        cin>>arr[i];
        if(arr[i]>mx) mx=arr[i];
    }
    int frequencyArray[mx+1]{0};
	for (int i=0;i<n;i++) frequencyArray[arr[i]]++;
	return 0;
}
```

<br><br>

## Prefix Sum
> Use this technique when you want to get the sum of a range quickly instead of looping for the whole array.
```cpp
int main()
{
    int n;
    cin >> n;
    int arr[n];

	for (int i = 0; i < n; i++)
	    cin >> arr[i];

    for (int i = 1; i < n; i++)
        arr[i] += arr[i-1];

    return 0;
}

```

<br><br>

## Partial Sum
> Use this technique when you want to add a number from start index to end index for an array of zeros.
```cpp
int main()
{
    int n, q;
    cin >> n >> q;
    int arr[n+9] {0};

    for (int i = 0; i < q; i++)
    {
        int l, r, k;
        cin >> l >> r >> k;
        arr[l-1] += k;
        arr[r] -= k;
    }

    for (int i = 1; i < n; i++)
        arr[i] += arr[i-1];

    return 0;
}
```