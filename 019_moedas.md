# Moedas

```c#
// when in doubt go with decimal
decimal valor = 10.25m;

// pt-BR
decimal vl = 1780.25m;
var br = CultureInfo.CreateSpecificCulture("pt-BR");
Console.WriteLine( vl.ToString(br) );
//-> 1780,25
Console.WriteLine( string.Format("{0:G}") );
Console.WriteLine( vl.ToString("G",br) );
//-> 1780,25
Console.WriteLine( string.Format("{0:F}") );
Console.WriteLine( vl.ToString("F",br) );
//-> 1780,25
Console.WriteLine( string.Format("{0:C}") );
Console.WriteLine( vl.ToString("C",br) );
//-> R$ 1.780,25
Console.WriteLine( string.Format("{0:N}") );
Console.WriteLine( vl.ToString("N",br) );
//-> 1.780,25
Console.WriteLine( string.Format("{0:E04}") );
Console.WriteLine( vl.ToString("E04",br) );
//-> 1,7803E+003
Console.WriteLine( string.Format("{0:P}") );
Console.WriteLine( vl.ToString("P",br) );
//-> 178.025,00%

// MATH ROUND
var vl = 10.25m;
Type tp = vl.GetType();
//-> System.Decimal
// TO UP or DOWN
var vl2 = Math.Round(vl);//arredondar
// TO UP
var vl3 = Math.Ceiling(vl);//telhado
// TO DOWN
var vl4 = Math.Floor(vl);//chão
```
