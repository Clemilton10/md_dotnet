# String

```c#
using System;
using System.Text;

namespace MyApp
{
	class Program
	{
		static void Main(string[] args)
		{
			// Juntando/Concatenando/Interpolando textos com outros objetos
				// 1ª Forma
				var price = 12.56;
				var texto1 = "O Preço é " + price;

				// 2ª Forma
				var texto2 = string.Format("O preço é {0} isso é {1}", price, true);

				// 3ª Forma
				var texto3 = $"O preço é {price} isso é {true}";

			// Santando linha ou escrever caracteres especiais(escape (\n)) -> arroba
			var texto4 = $@"O preço é {price}
isso é {true}";

			// Comparar texto
				// Comparando -> Case Sensitive
				var texto5 = "O Clemas é um cara legal";
				var cpc = texto5.CompareTo("Clemas");
				// not Case Sensitive
				// var cpi = texto5.CompareTo("Clemas", StringComparison.OrdinalIgnoreCase);
				var eq = texto5.Equals("o clemas é um cara legal", StringComparison.OrdinalIgnoreCase);

			// Procurando / Verificando se contém -> Case Sensitive
				var ctc = texto5.Contains("cle");
				// not Case Sensitive
				var cti = texto5.Contains("cle", StringComparison.OrdinalIgnoreCase);

			// Procurando no Início ou Final
				var inicio = texto5.StartsWith("O Clemas", StringComparison.OrdinalIgnoreCase);
				var final = texto5.EndsWith("legal", StringComparison.OrdinalIgnoreCase);

			// Buscar um caracter do array de char
				var cr = texto5[0];

			// Buscando a primeira e última ocorrência de uma string
				var pri = texto5.IndexOf("e");
				var ult = texto5.LastIndexOf("e");

			// Convertendo o texto para maiúsculo ou minúsculo
				var maius = texto5.ToUpper();
				var minus = texto5.ToLower();

			// Inserindo texto em uma posição
				var texto5b = texto5.Insert(5, " TESTE ");

			// Removendo uma parte de uma string
				var texto5c = texto5.Remove( 5, 5 );

			// Qtd de caracteres
				var lg = texto5.Length;

			// Substituir
				var texto5d = texto5.Replace("e", "x");

			// Dividir / Quebrar
				var pedacos = texto5.Split(" ");

			// Juntar
				var juntados = string.Join(" ", pedacos);

			// pedaço
				var pedaco = texto5.Substring(0, 5);

			// Limpar espaço do inicio e final
				var limpo = " Clemas tu tá de sacanagem ".Trim();

			// Concatenar textos grandes
				dynamic texto6 = new StringBuilder();
				texto6.AppendLine("Mais uma linha 1");
				texto6.Append("Novo Tipo");
				texto6.AppendLine("Mais uma linha 2");
				texto6.AppendLine("Mais uma linha 3");
				texto6.AppendLine("Mais uma linha 4");
				texto6 = texto6.ToString();

			Console.WriteLine( texto6.GetType() );
			// Console.WriteLine( texto6 );

		}
	}
}
```
