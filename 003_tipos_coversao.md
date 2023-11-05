## Coversão implícita

```c#
float valor = 25.8f;
int outro = 25;
valor = outro;
```

## Conversão explícita

```c#
int inteiro = 100;
uint inteiroSemSinal = (uint)inteiro;
```

## Conversão de String para inteiro

```c#
int inteiro = int.Parse("100");
```

## Converter outros tipos

```c#
int inteiro = Convert.ToInt32("100");

// double -> string
double salario = 100.59;
string salario = salario.ToString(salario);

// inteiro string -> int
int inteiro = int.Parse("150");//só converte um inteiro de uma string

double x, y, z;
int i, j, k, l;
bool b;

x = 10.0;
y = 3.0;
z = x / y;

// double -> int -> 1ª forma
i = (int) z;

// double -> int -> 2ª forma
k = Convert.ToInt32(z);

// double -> int -> 3ª forma
Int32.TryParse("-105", out int l);

// double -> int arredondado
j = (int) Math.Round(z);

// int -> bool
b = Convert.ToBoolean(255);// qualquer número maior que zero será true

// FORMAS ERRADAS
int v = Int32.Parse('');
int v = Int32.Parse("-105.5");
int m = Int32.Parse("abc");

// TENTANDO ANTES DE FAZER
const string s = "abc";
if ( Int32.TryParse(s, out int n) )
{
	Console.WriteLine(n);
}else
{
	Console.WriteLine($"Não deu pra converter '{s}' em inteiro.");
}
```

## Buscar o tipo da variável

```c#
var vl = 10.25m;
Type tp = vl.GetType();
```
