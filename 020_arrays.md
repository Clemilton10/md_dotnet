# Arrays

```c#
// EMPTY ARRAY WITHOUT COUNT ITEMS
var myArray = new int[]{45,56};
int[] myArray = new int[]{45,56};

// EMPTY ARRAY WITH COUNT ITEMS
var myArray = new int[2];
int[] myArray = new int[2];

// FILLED ARRAY
var myArray = new int[2]{45,56};
int[] myArray = new int[2]{45,56};
myArray[0] = 88;
for(var i = 0; i < myArray.Length; i++)
{
	Console.WriteLine(myArray[i]);
}

// ARRAY WITH REFERENCE
var refArray = myArray;

// NEW ARRAY
var a1 = new[] { "Ally", "Bishop", "Billy" };
var a2 = new string[3];
a1.CopyTo(a2, 0);//creating new array in zero position
a1[0] = "Philip";
foreach (var item in a1)
{
	Console.WriteLine(item);
}
foreach (var item in a2)
{
	Console.WriteLine(item);
}

var a1 = new[] { "Ally", "Bishop", "Billy" };
var a2 = new string[8];
a1.CopyTo(a2, 2);//create new array at a specific position
a1[0] = "Philip";
for(var i = 0; i < a2.Length; i++)
{
	Console.WriteLine($"{i} - {a2[i]}");
}
//-> 0 -
//-> 1 -
//-> 2 - Ally
//-> 3 - Bishop
//-> 4 - Billy
//-> 5 -
//-> 6 -
//-> 7 -

// DYNAMIC
static void Main(string[] args)
{
	Console.Clear();
	var funcionarios = new Funcionario[2];
	funcionarios[0] = new Funcionario(){ Id = 88, Name = "Clemas" };//--OBS
	foreach(var funcionario in funcionarios)
	{
		Console.WriteLine(funcionario.Id);
		Console.WriteLine(funcionario.Name);
		Console.WriteLine("----------------------");
	}
}
public struct Funcionario
{
	public int Id { get; set; }
	public string Name { get; set; }
}
```
