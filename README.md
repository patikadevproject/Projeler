# fibonnacci
```
static double fibonacci(double n)
{
    int a = 1, b = 1, c;
    double toplam = 0;
    for (int i = 1; i <= n; i++)
    {
        c = a + b;
        a = b;
        b = c;
        toplam += c;
    }
    return toplam / n;
}
```
