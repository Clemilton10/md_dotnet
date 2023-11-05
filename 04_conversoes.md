# Coversões

```c#
using System; // importações

namespace MyApp // disco virtual
{
	class Program // classe programa
	{
		static void Main(String[] args) // função principal
		{
			int inteiro = 100;
			float real = 25.5f;
			// o float poderia receber o inteiro
			// real = inteiro;

			// recebendo apenas um inteiro arredondado para baixo
			inteiro = (int)real;
			Console.WriteLine($"O inteiro que recebeu o real: {inteiro}");

			real = (float)inteiro;

			//somando
			real += 0.5f;
			Console.WriteLine($"O real que recebeu o inteiro e somei: {real}");

			int inteiroB = 100;
			float realB = 25.5f;

			//convertendo para inteiro arredondado para baixo
			realB = (int)realB;

			//convertendo em string
			string realBStr = realB.ToString();

			// convertendo para inteiro novamente
			inteiroB = int.Parse(realBStr);
			Console.WriteLine($"Real para int, para string, para inteiro: {inteiroB}");

			int inteiroC = 100;
			float realC = 25.5f;

			// Convertendo para inteiro arredondando
			inteiroC = Convert.ToInt32(realC);

			Console.WriteLine($"Real para int diretamente: {inteiroC}");
			Console.WriteLine($"Convertendo para Boolean: {Convert.ToBoolean(1)}");
			Console.WriteLine($"Convertendo para Boolean: {Convert.ToBoolean(realC)}");
			Console.WriteLine($"Convertendo para Boolean: {Convert.ToBoolean('true')}");

		}
	}
}
```
