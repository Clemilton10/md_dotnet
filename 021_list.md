# List

```c#
List<int> idades = new List<int>();
idades.Add(38);
idades.Add(43);
idades.Add(51);
List<int> idades2 = new List<int>();
idades2.AddRange(idades);//Cloning old array in new array
idades2[0] = 1;
foreach(var idade in idades)
{
	Console.WriteLine(idade);
}
foreach(var idade in idades2)
{
	Console.WriteLine(idade);
}
```

## Principais propriedades

```c#
Capacity # representa o número de elementos que a lista pode suportar sem que precise ser redimensionada. A partir desse número, novos elementos farão com que o compilador aloque mais memória para a lista.
Count # retorna (apenas leitura) a quantidade de itens que atualmente existe na lista.
```

## Principais métodos

```c#
# A seguir serão citados alguns dos principais métodos da classe List, mas é fundamental que o leitor visite a documentação oficial para conferir a lista completa de métodos, incluindo métodos de extensão.
Add(T item) # adiciona o parâmetro de tipo T (definido na declaração) no final da lista.
AddRange(IEnumerable<T> collection) # adiciona todos os itens da coleção que foi passada como parâmetro à lista.
Clear() # como o nome sugere, esse método limpa a lista, removendo todos os elementos.
Contains(T item) # retorna um valor booleano indicando se o item pesquisado existe na lista.
Exists(Predicate<T> match) # retorna um booleano indicando se existe na lista um item que atenda às condições definidas no predicado.
Find(Predicate<T> match) # verifica se existe um ou mais itens que atendam à condição definida em match e caso exista, retorna a primeira ocorrência.
FindAll(Predicate<T> match) # funciona semelhante ao Find, mas retorna uma lista com todos os itens que atendam à condição.
ForEach(Action<T> action) # executa a ação definida para todos os elementos da lista.
Insert(int index, T item) # funciona semelhante ao Add, mas insere o item em uma posição definida por index.
InsertRange(int index, IEnumerable<T> collection) # funciona semelhante ao AddRange, mas insere a nova lista na posição definida por index.
Remove(T item) # remove o item da lista e retorna um booleano indicando o sucesso da operação. Caso o item não seja encontrado, também retorna false.
Sort() # ordena a lista utilizando o comparador padrão do tipo de item contido na lista. Este método também pode receber como parâmetro objetos que definem a forma como a comparação entre os itens deve ser feita.
ToArray() # retorna um vetor do tipo contido na lista.
```
