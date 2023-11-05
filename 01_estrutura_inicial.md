# Estrutura inicial

```c#
using System;
namespace MyApp
{
	class Program
	{
		static void Main(String[] args)
		{
			var texto = "testando";
			Console.WriteLine(texto);
		}
	}
}
```

```c#
/*
Hoje em dia o dotnet executa sem:
- using System;
- namespace MyApp
- class Program
- static void Main(String[] args)
*/
int valor = 0;
do
{
	valor++;
	Console.WriteLine(valor);
} while (valor < 5);
outroMetodo();

static void outroMetodo()
{
	Console.WriteLine("Outro Método");
}
```
