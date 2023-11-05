# Struct -> Estutura

## EXEMPLO 1

```c#
namespace MeuApp
{
	struct Product
	{
		public int Id;
		public float Price;
		public string Title;

		public float PriceInDolar(float dolar)
		{
			return Price * dolar;
		}
	}
	class MainClass
	{
		static void Main()
		{
			var pd = new Product();
			pd.Id = 1;
			pd.Title = "Mouse Gamer";
			pd.Price = 197.23f;
			Console.WriteLine(pd.Id);
			Console.WriteLine(pd.Title);
			Console.WriteLine(pd.Price);
		}
	}
}
```

## EXEMPLO 2

```c#
namespace MeuApp
{
	struct Product
	{
		public int Id;
		public float Price;
		public string Title;

		public Product(int id, string title, float price)
		{
			Id = id;
			Title = title;
			Price = price;
		}
	}
	class MainClass
	{
		static void Main()
		{
			var pd = new Product(1, "Mouse Gamer", 197.23f);
			Console.WriteLine(pd.Id);
			Console.WriteLine(pd.Title);
			Console.WriteLine(pd.Price);
		}
	}
}
```
