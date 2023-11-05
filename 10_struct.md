# Struct

```c#
// Quando se atribui assim, tem que preencher todas as propriedades
Product product1;
product1.Id = 1;
product1.Price = 10.99f;
product1.Name = "Produto A";
Console.WriteLine(product1.PriceInDolar(4));

var product2 = new Product();
product2.Id = 2;
Console.WriteLine(product2.PriceInDolarDefault());
struct Product
{
	// Propriedades com primeira letra maiúscula
	public int Id;
	public float Price;
	public string Name;

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
		string name = "Original"
	)
	{
		Id = id;
		Price = price;
		Name = name;
		// se for com mesmo nome(errado), tem que usar o this
	}
	public Product()
	{
		Id = 0;
		Price = 10.0f;
		Name = "Original";
		// se for com mesmo nome(errado), tem que usar o this
	}
}
```
