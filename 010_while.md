# Loop `WHILE`

## Checka antes de executar

```sh
👉 # Obs.: if condicao == true -> executa
```

## Imprime começando de zero

```c#
int v1 = 0;
while (v1 < 3)
{
	Console.WriteLine(v1);
	v1++;
}
```

```sh
# OUTPUT
0
1
2
```

## Imprime comaçando de 1

```c#
int v2 = 0;
while (v2 < 3)
{
	v2++;
	Console.WriteLine(v2);
}
```

```sh
# OUTPUT
1
2
3
```

## Infinito

```c#
while (true)
{
	...
}
```

## Executa depois chega para fazer o próximo

```sh
👉 # Obs.: executa -> if condicao == true -> próximo
```

```c#
int v3 = 0;
do
{
	Console.WriteLine(v3);
	v3++;
}while (v3 < 5);
```

```sh
# OUTPUT
1
2
3
```
