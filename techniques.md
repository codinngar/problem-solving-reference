# Techniques for problem solving

<br><br>

## Frequency Array
> Use this technique when you want to know how many times a number has been repeated or to check if the number exists or not.
```cpp
int arr[] = {4, 8, 2, 7, 9, 0, 2};
int counter[10]; // max value in the array + 1
int main()
{
	for (int i = 0; i < sizeof(arr) / sizeof(arr[0]); i++)
	{
		int x = arr[i];   // 0 1 2 3 4 5 6 7 8 9
		counter[x]++;     // 1 0 2 0 1 0 0 1 1 1
	}
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