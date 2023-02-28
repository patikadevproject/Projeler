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

# Üçgen Çizme
```
static void ucgen(int derinlik)
{
    for (int i = 1; i <= derinlik; i++)
    {
        for (int j = 1; j <= derinlik - i; j++)
            Console.Write(" ");
        for (int j = 1; j <= 2 * i - 1; j++)
            Console.Write("*");
        Console.WriteLine();
    }
}

```

# Daire Çizme
```
static void daire(double r)
{
    for (int y = -(int)r; y <= (int)r; y++)
    {
        for (int x = -(int)r; x <= (int)r; x++)
            Console.Write(x * x + y * y <= r * r ? "*" : " ");
        Console.WriteLine();
    }
}

```

# Algoritma
```
static string Algoritma(string word)
{
    string[] arr = word.Split(",");
    return arr[0].Remove(Convert.ToInt16(arr[1]),1);
}

``` 
