# Enum

```c#
// Quando se atribui assim, tem que preencher todas as propriedades
Product product1;
product1.Id = 1;
product1.Price = 10.99f;
product1.Name = "Produto A";
product1.Category = 3;
product1.ECategoryy = Product.ECategory.Eletronics;
Console.WriteLine(product1.PriceInDolar(4));

var product2 = new Product();
product2.setECategory(3);
Console.WriteLine(product2.PriceInDolarDefault());
Console.WriteLine(product2.Category);
Console.WriteLine(product2.ECategoryy);//objeto
Console.WriteLine(product2.ECategoryy.ToString());//string
Console.WriteLine((int)product2.ECategoryy);//inteiro
struct Product
{
	// Propriedades com primeira letra maiúscula
	public int Id;
	public float Price;
	public string Name;

	public int Category;
	public ECategory ECategoryy;

	// Parâmetros com a primeira letra minúscula
	public float PriceInDolar(float dolar)
	{
		return Price * dolar;
	}
	public float PriceInDolarDefault(float dolar = 5)
	{
		return Price * dolar;
	}
	// construct
	public Product(
		int id = 0,
		float price = 10.0f,
		string name = "Original",
		int category = (int)ECategory.Eletronics
	)
	{
		Id = id;
		Price = price;
		Name = name;
		Category = category;
		ECategoryy = (ECategory)Enum.ToObject(typeof(ECategory), Category);
	}
	public void setECategory(int category)
	{
		Category = category;
		ECategoryy = (ECategory)Enum.ToObject(typeof(ECategory), Category);
	}
	public Product()
	{
		Id = 0;
		Price = 10.0f;
		Name = "Original";
		Category = (int)ECategory.Eletronics;
		ECategoryy = (ECategory)Enum.ToObject(typeof(ECategory), Category);
	}

	public enum ECategory
	{
		Eletronics = 1,
		Games = 2,
		HomeAppliances = 3
	}
}
```
