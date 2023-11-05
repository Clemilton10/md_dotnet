# NameSpace

FormasGeometricas.cs

```c#
namespace FormasGeometricas
{
	// Classe base para todas as formas
	public abstract class Forma
	{
		public abstract double CalcularArea();
	}

	// Namespace para as formas 2D
	namespace Formas2D
	{
		// Classe para círculos
		public class Circulo : Forma
		{
			public double Raio { get; set; }

			public Circulo(double raio)
			{
				Raio = raio;
			}

			public override double CalcularArea()
			{
				return Math.PI * Raio * Raio;
			}
		}

		// Classe para retângulos
		public class Retangulo : Forma
		{
			public double Largura { get; set; }
			public double Altura { get; set; }

			public Retangulo(double largura, double altura)
			{
				Largura = largura;
				Altura = altura;
			}

			public override double CalcularArea()
			{
				return Largura * Altura;
			}
		}
	}
}
```

Program.cs

```c#
using System; // importações
using FormasGeometricas;

namespace MyApp // disco virtual
{
	class Program // classe programa
	{
		static void Main(String[] args) // função principal
		{
			// Exemplo de uso das classes em namespaces
			var circulo = new FormasGeometricas.Formas2D.Circulo(5);
			var retangulo = new FormasGeometricas.Formas2D.Retangulo(4, 6);
			Console.WriteLine("Área do círculo: " + circulo.CalcularArea());
			Console.WriteLine("Área do retângulo: " + retangulo.CalcularArea());
		}
	}
}
```
