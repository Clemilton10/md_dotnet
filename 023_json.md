# Json

## EXEMPLO 1

```c#
using System;
using System.Text.Json;

namespace MyApp
{
	class Program
	{

		// aqui a mágica
		public class Department{
			public int DeptId { get; set; }
			public string DepartmentName { get; set; }
		}

		static void Main(string[] args)
		{
			string jsonData = "{\"DeptId\": 101, \"DepartmentName\": \"IT\"}";
			Department deptObj = JsonSerializer.Deserialize<Department>(jsonData);
			Console.WriteLine("Department Id: {0}", deptObj.DeptId);
			Console.WriteLine("Department Name: {0}", deptObj.DepartmentName);
		}
	}
}
```

```sh
# OUTPUT
Department Id: 101
Department Name: IT
```

## EXEMPLO 2

```c#
using System;
using System.Text.Json;

namespace MyApp
{
	class Program
	{

		// aqui a mágica
		public class Pessoa
		{
			public String Nome { get; set; }
			public int Idade { get; set; }
		}
		static void Main(string[] args)
		{
			var json = @"{""Nome"":""Carlos Silva"",""Idade"":33}";
			var pessoa = JsonSerializer.Deserialize<Pessoa>(json);
			Console.WriteLine(pessoa.Nome);
			Console.WriteLine(pessoa.Idade);
		}
	}
}
```

```sh
# OUTPUT
Carlos Silva
33
```

## EXEMPLO 3

```c#
using System;
using System.Text.Json;

var json = @"{""Nome"":""Carlos Silva"",""Idade"":33, ""Telefones"": { ""celular"": ""11-99999-9999"", ""comercial"": ""11-4444-4444""}}";

var obj = JsonDocument.Parse(json);
var nome = obj.RootElement.GetProperty("Nome").GetString();
var celular = obj.RootElement.GetProperty("Telefones").GetProperty("celular").ToString();
Console.WriteLine(nome);
Console.WriteLine(celular);
```

```sh
# OUTPUT
Carlos Silva
11-99999-9999
```
