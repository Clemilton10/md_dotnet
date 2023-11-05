# Memória

```sh
Heap  # Value Type     ➜ armazena os dados
Stack # Reference Type ➜ armazena as referências para os dados
```

### `GERA OUTRO OBJETO`

### EXEMPLO 1

```c#
int v2 = 1;
int v1 = v2; // gera uma cópia, as duas são independentes
v1 = 2;
Console.WriteLine(v1);// 2
Console.WriteLine(v2);// 1
```

```sh
# OUTPUT
2
1
```

### EXEMPLO 2

```c#
var a1 = new[] { "Ally", "Bishop", "Billy" };
var a2 = new string[4];
a1.CopyTo(a2, 1);
a1[0] = "Philip";
foreach (var item in a1)
{
	Console.WriteLine(item);
}
foreach (var item in a2)
{
	Console.WriteLine(item);
}
```

```sh
# OUTPUT
Philip
Bishop
Billy

Ally
Bishop
Billy
```

### `NAO GERA OUTRO OBJETO`

```c#
var a1 = new string[2];
a1[0] = "Item 1";
var a2 = a1; // Não cria cópia, usa a referência, ou seja a mesma
a1[0] = "Item alterado";
Console.WriteLine(a1[0]);// Item alterado
Console.WriteLine(a2[0]);// Item alterado
```

```sh
# OUTPUT
Item alterado
Item alterado
```

```sh
👉 Built-in, Structs, Enums -> Value Type

👉 Garbage Collector -> não acessa o Stack -> remove o que não for usado na memória
```
