## Versão do `.NET (dotnet)`

```sh
dotnet --version
```

## Listar Versões instaladas

```sh
dotnet --list-sdks
```

## Ajuda

```sh
dotnet --help
```

## Iniciar um projeto

Iniciando com `nome do projeto`

```sh
dotnet new sh -n NomeProjeto
dotnet new xunit -n NomeProjeto
```

Iniciando com `nome da pasta`

```sh
dotnet new sh -o NomePasta
dotnet new xunit -o NomePasta
```

## Obs.:

Sempre inicie o nome do projeto, namespace ou classes com `primeira letra 'maiúscula'`

```cs
internal class Program { ... }
```

`Constantes tudo em 'maiúsculo'`

```cs
const int Q_VEZES = 25;
```

Sempre inicie o nome de uma `variável com letra 'minúscula'`

```cs
var primeiroNome = "Clemas"
```

## Trocar versão do SDK do projeto

```sh
dotnet new globaljson --sdk-version 2.0.0 --force
```

## Baixa todos os pacotes necessários para a aplicação

```sh
dotnet restore
```

## Compilar a aplicação

```sh
dotnet build
```

## Limpa as compilações anteriores -> Limpar cache

```sh
dotnet clean
```

## Compila e executa a aplicação

```sh
dotnet run
dotnet run --project .\NomeDaPasta
dotnet run --project .\NomeDaPasta\NomeDoProjeto.csproj
```

## Sequência

```sh
dotnet clean
dotnet build
dotnet run
```

```powershell
👉 # Obs.: O comando run não executa depuração (Debug)
```

## Executar com as variáveis alteradas

```sh
dotnet run --environment=NomeAmbiente
dotnet run --environment=development
dotnet run --environment=production
```
