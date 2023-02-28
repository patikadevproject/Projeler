# Kolay seviye projeler
1. fibonnacci
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

2. Üçgen Çizme
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

3. Daire Çizme
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

4. Algoritma
```
static string Algoritma(string word)
{
    string[] arr = word.Split(",");
    return arr[0].Remove(Convert.ToInt16(arr[1]),1);
}

``` 

5. Karakter Tersten Yazdırma
```
static string reverse(string sentence)
{
    string newsentence = "";
    for(int i = sentence.Length-1; i>=0;i--){
        newsentence+=sentence[i];
    }
    return newsentence;
}

``` 

# Orta seviye projeler

1. Alan Hesaplama

```
static double sekil_hesapla(string type)
{
    Console.WriteLine("Lütfen boyut seçiniz: \n Çevre (1) \n Alan  (2) \n Hacim (3)");
    int islem = Convert.ToInt32(Console.ReadLine());
    switch (type)
    {
        case "Daire":
            Console.WriteLine("Lütfen yarıçap uzunluğu giriniz:");
            int r = Convert.ToInt32(Console.ReadLine());
            switch (islem)
            {
                case 1:
                    return 2 * Math.PI * r;
                case 2:
                    return Math.PI * Math.Pow(r, 2);
                case 3:
                    return (4 * Math.PI * Math.Pow(r, 3)) / 3;
                default: Console.WriteLine("Geçerli bir işlem seçiniz"); break;
            }
            break;
        case "Dörtgen":
            Console.WriteLine("Lütfen kısa kenarın uzunluğu giriniz:");
            int a = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Lütfen uzun kenarın uzunluğu giriniz:");
            int b = Convert.ToInt32(Console.ReadLine());
            switch (islem)
            {
                case 1:
                    return 2 * (a + b);
                case 2:
                    return a * b;
                case 3:
                    Console.WriteLine("Yükseklik giriniz:");
                    int c = Convert.ToInt32(Console.ReadLine());
                    return a * b * c;
                default: Console.WriteLine("Geçerli bir işlem seçiniz"); break;
            }
            break;
        case "Kare":
            Console.WriteLine("Lütfen kenarın uzunluğu giriniz:");
            int k1 = Convert.ToInt32(Console.ReadLine());
            switch (islem)
            {
                case 1:
                    return 4 * k1;
                case 2:
                    return k1 * k1;
                case 3:
                    return k1 * k1 * k1;
                default: Console.WriteLine("Geçerli bir işlem seçiniz"); break;
            }
            break;

        case "Üçgen":
            Console.WriteLine("Lütfen birinci kenar uzunluğunu giriniz:");
            int u1 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Lütfen ikinci kenar uzunluğunu giriniz:");
            int u2 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Lütfen üçüncü kenar uzunluğunu giriniz:");
            int u3 = Convert.ToInt32(Console.ReadLine());
            Console.WriteLine("Lütfen üçüncü kenara ait yüksekliği giriniz:");
            int uh = Convert.ToInt32(Console.ReadLine());
            switch (islem)
            {
                case 1:
                    return u1 + u2 + u3;
                case 2:
                    return (u3 * uh) / 2;
                case 3:
                    Console.WriteLine("Yükseklik giriniz:");
                    int h = Convert.ToInt32(Console.ReadLine());
                    return (u3 * uh * h) / 2;
                default: Console.WriteLine("Lütfen geçerli bir şekil giriniz"); break;
            }
            break;
        default: Console.WriteLine("lütfen geçerli bir şekil giriniz"); break;
    }
    return 0;
}

``` 

2. İkililerin toplamı

```
static void ikililer(int[] sayıListesi)
{
    if (sayıListesi.Length % 2 == 0)
        for (int i = 0; i < sayıListesi.Length; i += 2)
                Console.Write(sayıListesi[i] == sayıListesi[i + 1]? Math.Pow(sayıListesi[i] + sayıListesi[i + 1],2)+" ":sayıListesi[i] + sayıListesi[i + 1]+" ");
    else
        Console.WriteLine("\a Hatalı tuşlama! Lütfen çift sayı giriniz.");
}
```
3. Mutlak Kare Alma

```
static string mutlakkare(int[] sayıListesi)
{
    int toplamfarklar = 0;
    double mutlakkareler = 0;
    for (int i = 0; i < sayıListesi.Length; i++)
    {
        if (sayıListesi[i] <= 67)
            toplamfarklar += 67 - sayıListesi[i];
        else
            mutlakkareler += Math.Pow((sayıListesi[i] - 67), 2);
    }
    return toplamfarklar + " " + mutlakkareler;
}
```
3. Mutlak Kare Alma

```
static string mutlakkare(int[] sayıListesi)
{
    int toplamfarklar = 0;
    double mutlakkareler = 0;
    for (int i = 0; i < sayıListesi.Length; i++)
    {
        if (sayıListesi[i] <= 67)
            toplamfarklar += 67 - sayıListesi[i];
        else
            mutlakkareler += Math.Pow((sayıListesi[i] - 67), 2);
    }
    return toplamfarklar + " " + mutlakkareler;
}
```
3. Mutlak Kare Alma

```
static string mutlakkare(int[] sayıListesi)
{
    int toplamfarklar = 0;
    double mutlakkareler = 0;
    for (int i = 0; i < sayıListesi.Length; i++)
    {
        if (sayıListesi[i] <= 67)
            toplamfarklar += 67 - sayıListesi[i];
        else
            mutlakkareler += Math.Pow((sayıListesi[i] - 67), 2);
    }
    return toplamfarklar + " " + mutlakkareler;
}
```

4. Karakter Değiştirme

```
static void change_letters(string input)
{
    string[] str = input.Split();
    foreach (var item in str)
    {
        char[] letters = item.ToCharArray();
        char tasiyici = letters[0];
        letters[0] = letters[letters.Length - 1];
        letters[letters.Length - 1] = tasiyici;
        string s = "";
        foreach (var c in letters)
            s += c.ToString();
        Console.Write(s + " ");
    }
}
```

5. Sessiz Harf

```
static void sessiz_harf(string input)
{
    string[] kelimeler = input.Split(' ');
    string sessizler = "bcdfghjklmnpqrstvwxyz";
    foreach (string item in kelimeler)
    {
        bool varmi = false;
        for (int i = 0; i < item.Length - 1; i++)
        {
            if (sessizler.Contains(item[i]) && sessizler.Contains(item[i + 1]))
            {
                varmi = true;
                break;
            }
        }
        Console.Write(varmi + " ");
    }
}
```
