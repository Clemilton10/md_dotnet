# Enum

```c#
// Quando se atribui assim, tem que preencher todas as propriedades
Product product1;
product1.Id = 1;
product1.Price = 10.99f;
product1.Name = "Produto A";
product1.Category = Product.ECategory.HomeAppliances;
Console.WriteLine(product1.PriceInDolar(4));

var product2 = new Product();
product2.Id = 2;
Console.WriteLine(product2.PriceInDolarDefault());
Console.WriteLine(product2.Category);
Console.WriteLine((int)product2.Category);
struct Product
{
	// Propriedades com primeira letra maiúscula
	public int Id;
	public float Price;
	public string Name;

	public ECategory Category;

	// Parâmetros com a primeira letra minúscula
	public float PriceInDolar(float dolar)
	{
		Console.WriteLine(Price);
		Console.WriteLine(dolar);
		return Price * dolar;
	}
	public float PriceInDolarDefault(float dolar = 5)
	{
		Console.WriteLine(Price);
		Console.WriteLine(dolar);
		return Price * dolar;
	}
	// construct
	public Product(
		int id = 0,
		float price = 10.0f,
		string name = "Original",
		ECategory category = ECategory.Eletronics
	)
	{
		Id = id;
		Price = price;
		Name = name;
		Category = category;
	}
	public Product()
	{
		Id = 0;
		Price = 10.0f;
		Name = "Original";
		Category = ECategory.Eletronics;
	}

	public enum ECategory
	{
		Eletronics = 1,
		Games = 2,
		HomeAppliances = 3
	}
}
```
