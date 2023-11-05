# Values Types

```c#
// Cópia independente
int x = 25;
int y = x; // y é uma cópia
Console.WriteLine(x);//25
Console.WriteLine(y);//25
x = 32; // afeta apenas o x
Console.WriteLine(x);//32
Console.WriteLine(y);//25
```

# References Type

```c#
// Referência ao mesmo objeto
string[] arr = new string[2];
arr[0] = "Item Antes";
arr[1] = "Item Antes2";
string[] arr2 = arr;
print(arr);
print(arr2);
arr2[0] = "Alterei";// Quando altera um, altera o outro
print(arr);
print(arr2);

static void print(string[] list)
{
	foreach (string str in list)
	{
		Console.WriteLine(str);
	}
	Console.WriteLine("");
}
```

# Clone idependente

```c#
// Cópia independente
string[] arr = new string[2];
arr[0] = "Item Antes";
arr[1] = "Item Antes2";
string[] arr2 = (string[])arr.Clone();
print(arr);
print(arr2);
arr2[0] = "Alterei";// Quando altera um, não altera o outro
print(arr);
print(arr2);

static void print(string[] list)
{
	foreach (string str in list)
	{
		Console.WriteLine(str);
	}
	// ou
		for (int i = 0; i < list.Length; i++)
	{
		Console.WriteLine(list[i]);
	}
	Console.WriteLine("");
}
```
