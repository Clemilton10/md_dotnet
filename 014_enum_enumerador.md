# Enum -> Enumerador

```c#
namespace MeuApp
{
	enum EEstadoCivil
	{
		Solteiro = 1,
		Casado = 2,
		Divorciado = 3,
		Viuvo = 4
	}
	struct Cliente
	{
		public string Nome;
		public EEstadoCivil EstadoCivil;
		public Cliente(string nome, EEstadoCivil estadoCivil)
		{
			Nome = nome;
			EstadoCivil = estadoCivil;
		}
	}
	class MainClass
	{
		static void Main()
		{
			var cl = new Cliente("José Ambrósio", EEstadoCivil.Casado);
			Console.WriteLine(cl.Nome);
			Console.WriteLine(cl.EstadoCivil);
			Console.WriteLine( (int)cl.EstadoCivil );
		}
	}
}
```
