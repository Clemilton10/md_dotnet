# Métodos

```c#
// not return
outroMetodo();

// not age
string name = returnName("Clemas", "Costa");
Console.WriteLine(name);

// with age
string nameB = returnName("Clemas", "Costa", 44);
Console.WriteLine(nameB);

static void outroMetodo()
{
	Console.WriteLine("Outro Método");
}


static string returnName(
	string name,
	string lastname,
	int? age = null // default value
	// default values ​​have to be at the end of the parameters
)
{
	return $"{name} {lastname} {age.ToString()}";
}
```
