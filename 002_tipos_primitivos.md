## Tipos primitivos

```c#
byte    # 0 -> 255
sbyte   # -127 -> 127 // s=signed

short   # Números pequenos -> 16bt
int     # Números médios -> 32bt // padrão
long    # Números longos -> 64bt
ushort  # Números pequenos // u=unsigned -> não aceita número negativo
uint    # Números médios
ulong   # Números longos

float   # 32bt -> float salario = 2.500f;
double  # 64bt -> double salario = 25.500; // padrão
decimal # 128bt -> decimal salario = 25.500m;

bool    # 8bt -> bool pagamentoRecebido = true;
char    # 16bt -> char letra = 'A'; // apenas um caracter unicode -> aspa simples
string  # string nome = "Clemas"; // uma lista de char -> aspa dupla
var     # assume o primeiro item informado // tem que passar um valor inicial
object  # pode declarar sem passar valor

void    # vazio

null    # int? idade = null;
```

## alias

```c#
System.String ➜ String ➜ string
System.Int32  ➜ Int32  ➜ int
```

## Valores padrão

```c#
int     # 0
float   # 0
decimal # 0
bool    # false
char    # \0
string  # ""
```

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
			Console.WriteLine((int)cl.EstadoCivil);
		}
	}
}
```
