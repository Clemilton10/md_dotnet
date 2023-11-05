# Guid

```c#
using System;

namespace MyApp
{
	class Program
	{
		static void Main(string[] args)
		{
			// Gerando uma ID tipo hash
			Guid id = Guid.NewGuid();

			// Alterando para String
			string sid = id.ToString();

			// Usando apenas um pedaço do hash
			string pid = id.ToString().Substring(0, 8);

			// Passando um hash manualmente
			// Tem que ser um hash válido
			var manual_id = new Guid("4f3f27d4-bc89-43b6-b781-a83c0050b6fd");

			// Gerar hash zerada
			var oid = new Guid();

			// Buscando o tipo
			Type tp = id.GetType();

			// Escrevendo
			Console.WriteLine(id);
			Console.WriteLine(tp);
			Console.WriteLine(oid);

			// Verificando se o tipo é um expecífico
			if( tp == typeof(System.Guid) )
			{
				Console.WriteLine(typeof(Guid));
			}
		}
	}
}
```
