# Funções

## EXEMPLO 1

```c#
public class Employee4
{
	public string id;
	public string name;

	public Employee4()
	{
	}

	// Em casses secundárias não precisa
	// do void para não retornar nada
	public Employee4(string name, string id)
	{
		this.name = name;
		this.id = id;
	}

	// VARIAVEL PUBLICA
	public static int employeeCounter;

	public static int AddEmployee()
	{
		return ++employeeCounter;
	}
}

class MainClass : Employee4
{
	// OBS.: void -> não retorna nada
	static void Main()
	{
		Console.Write("Enter the employee's name: ");
		string name = Console.ReadLine();// INPUT
		Console.Write("Enter the employee's ID: ");
		string id = Console.ReadLine();// INPUT

		Employee4 e = new Employee4(name, id);
		Console.Write("Enter the current number of employees: ");
		string n = Console.ReadLine();// INPUT
		Employee4.employeeCounter = Int32.Parse(n);// String -> int
		Employee4.AddEmployee();

		Console.WriteLine($"Name: {e.name}");// PRINT
		Console.WriteLine($"ID:   {e.id}");// PRINT
		Console.WriteLine($"New Number of Employees: {Employee4.employeeCounter}");// PRINT
	}
}
```

## EXEMPLO 2

```c#
// Receber argumentos ao chamar o executável
class Program
{
	static void Main(string[] args)
	{
		Console.WriteLine("Length of the arguments: " + args.Length);
		foreach (var arg in args)
		{
			Console.WriteLine(arg);
		}
	}
}
👉 # MyApp.exe "Arg 1" "Arg 2" "Arg 3"
👉 # Copy.exe C:\a1.txt C:\a2.txt
```

## EXEMPLO 3

```c#
class Program
{
	// TODOS OS PARAMETROS OPCIONAIS DEVEM ESTAR NO FINAL
	static string RetornaNome(
		string nome,
		string sobrenome,
		int idade = 22,
		email="contato@empresa.com"
	)
	{
		return nome + " " + sobrenome + " tem "
		+ idade.ToString() + " anos (" + email + ")";
	}
	static void Escreva()
	{
		Console.WriteLine("C# é legal");
	}
	static void Main()
	{
		Console.WriteLine(RetornaNome("Clemas", "da Costa"));
		Escreva();
	}
}
```
