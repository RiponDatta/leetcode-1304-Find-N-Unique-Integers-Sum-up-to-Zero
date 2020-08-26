# leetcode 1304 - Find N Unique Integers Sum up to Zero

## C#
```C#
public int[] SumZero(int n)
{
    var arr = new int[n];
    int j = 0;
    int x = 1;

    for(int i = 0; i < n/2; i++)
    {
        arr[j++] = x;
        arr[j++] = -1 * x;
        x++;
    }
    if (n % 2 == 1) arr[j] = 0;
    return arr;
}
```
