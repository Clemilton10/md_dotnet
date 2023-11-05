# Try / Catch / Finally

## EXEMPLO 1

```c#
var arr = new int[3];
try
{
	for(var i = 0; i < 10; i++)
	{
		Console.WriteLine(arr[i]);
	}
}
catch(IndexOutOfRangeException er)
{
	Console.WriteLine(er.GetType().FullName);
	Console.WriteLine(er.Message);
	Console.WriteLine("O índice não foi encontrado na lista");
}
catch(Exception er)
{
	Console.WriteLine(er.GetType().FullName);
	Console.WriteLine(er.Message);
	Console.WriteLine("Ops!");
}
finally
{
	Console.WriteLine("Fim!");
	//Obs.: Usado para fechar arquivos, conexões, etc
}
```

## EXEMPLO 2

```c#
static void Main(string[] args)
{
	try
	{
		string s = "";
		Salvar(s);
	}
	catch(Exception er)
	{
		Console.WriteLine(er.GetType().FullName);
		Console.WriteLine(er.Message);
		Console.WriteLine("Ops!");
	}
	finally
	{
		Console.WriteLine("Fim!");
		//Obs.: Usado para fechar arquivos, conexões, etc
	}
}
static void Salvar(string texto)
{
	if(string.IsNullOrEmpty(texto))
	{
		throw new Exception("O texto não pode ser nulo ou vazio");
	}
}
```

## EXEMPLO 3

```c#
static void Main(string[] args)
{
	try
	{
		string s = "";
		Salvar(s);
	}
	catch(Exception er)
	{
		Console.WriteLine(er.GetType().FullName);
		Console.WriteLine(er.Message);
		Console.WriteLine("Ops!");
	}
	finally
	{
		Console.WriteLine("Fim!");
		//Obs.: Usado para fechar arquivos, conexões, etc
	}
}
static void Salvar(string texto)
{
	if(string.IsNullOrEmpty(texto))
	{
		if(texto == null)
		{
			throw new ArgumentNullException(paramName: nameof(texto), message: "O texto não pode ser nulo");
		}
		if(texto == String.Empty)
		{
			throw new ArgumentException(paramName: nameof(texto), message: "O texto não pode ser vazio");
		}
	}
}
```

## EXEMPLO 4

```c#
static void Main(string[] args)
{
	try
	{
		string s = "";
		Salvar(s);
	}
	catch(MinhaException er)
	{
		Console.WriteLine(er.fc);
		Console.WriteLine(er.GetType().FullName);
		Console.WriteLine(er.Message);
	}
	catch(Exception er)
	{
		Console.WriteLine(er.GetType().FullName);
		Console.WriteLine(er.Message);
		Console.WriteLine("Ops!");
	}
	finally
	{
		Console.WriteLine("Fim!");
		//Obs.: Usado para fechar arquivos, conexões, etc
	}
}
static void Salvar(string texto)
{
	if(string.IsNullOrEmpty(texto))
	{
		MinhaException er = new MinhaException(message: "Este texto não pode ser nulo ou vazio!", fc: "Salvar:");
		throw er;
	}
}
public class MinhaException : Exception
{
	public MinhaException(string message = "", string fc = ""): base(message)
	{
		this.fc = fc;
	}
	public string fc { get; set; }
}
```
