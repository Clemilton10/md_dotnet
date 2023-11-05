# Type

```c#
using System;

namespace MyApp
{
	class Program
	{
		static void Main(string[] args)
		{
			// Buscando o hash
			Guid id = Guid.NewGuid();

			// Buscando o tipo
			Type tp = id.GetType();

			// Escrevendo
			Console.WriteLine(id);
			Console.WriteLine(tp);

			// Testando se é igual
			if( tp == typeof(System.Guid) )
			{
				Console.WriteLine(typeof(Guid));
			}
		}
	}
}
```
