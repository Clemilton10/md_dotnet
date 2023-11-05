# Data

```c#
// Data Padrão
var dateDefault = new DateTime();
Console.WriteLine($"{dateDefault}");
//-> 01/01/0001 00:00:00

// Agora
var dateNow = DateTime.Now;
Console.WriteLine($"{dateNow}");
//-> 30/08/2022 17:38:44

// passar data
var datePassed = new DateTime(2022, 04, 11, 14, 0, 0);
var y = datePassed.Year;
var m = datePassed.Month;
var d = datePassed.Day;
var h = datePassed.Hour;
var i = datePassed.Minute;
var s = datePassed.Second;
var w = datePassed.DayOfWeek;
var iw = (int) datePassed.DayOfWeek;
var dy = datePassed.DayOfYear;
Console.WriteLine($"{d}/{m}/{y} {h}:{i}:{s} {w} {iw} {dy}");
//-> 11/4/2022 14:0:0 Monday 1 101

var dateNow = DateTime.Now;
var dateNowFormated = String.Format(
	  "{0:"
	+ "d dd ddd dddd\n"
	+ "M MM MMM MMMM\n"
	+ "y yy yyy yyyy\n"
	+ "m mm mmm mmmm\n"
	+ "h hh hhh hhhh\n"
	+ "H HH HHH HHHH\n"
	+ "dd/MM/yyyy HH:mm:ss:ff zz}",
	dateNow
);
Console.WriteLine(dateNowFormated);
//-> 30 30 ter. terça-feira
//-> 8 08 ago. agosto
//-> 22 22 2022 2022
//-> 56 56 56 56
//-> 5 05 05 05
//-> 17 17 17 17
//-> 30/08/2022 17:56:04:70 -03
Obs.: f->Fração de segundo / z->Timezone

var dateNow = DateTime.Now;
var dateNowFormated = String.Format("{0:t}",dateNow);
//-> 18:25 -> hora curta
var dateNowFormated = String.Format("{0:T}",dateNow);
//-> 18:28:17 -> hora longa
var dateNowFormated = String.Format("{0:d}",dateNow);
//-> 30/08/2022 -> data curta
var dateNowFormated = String.Format("{0:D}",dateNow);
//-> terça-feira, 30 de agosto de 2022 -> data longa
var dateNowFormated = String.Format("{0:g}",dateNow);
//-> 30/08/2022 18:33
var dateNowFormated = String.Format("{0:G}",dateNow);
//-> 30/08/2022 18:33:15
var dateNowFormated = String.Format("{0:f}",dateNow);
//-> terça-feira, 30 de agosto de 2022 18:33
var dateNowFormated = String.Format("{0:F}",dateNow);
//-> terça-feira, 30 de agosto de 2022 18:33:15
var dateNowFormated = String.Format("{0:y}",dateNow);
//-> agosto de 2022
var dateNowFormated = String.Format("{0:r}",dateNow);
//-> Tue, 30 Aug 2022 18:46:16 GMT
var dateNowFormated = String.Format("{0:s}",dateNow);
//-> 2022-08-30T18:47:53
var dateNowFormated = String.Format("{0:u}",dateNow);
//-> 2022-08-30 18:49:03Z
var dateNowFormated = String.Format("{0:U}",dateNow);
//-> terça-feira, 30 de agosto de 2022 21:49:03

// GLOBAL DATETIME WITHOUT TIMEZONE
var dt = DateTime.UtcNow;
// adapting to a local datetime
var lcdt = dt.ToLocalTime();

// TIMEZONES
var dt = DateTime.UtcNow;
var tzAuckland = TimeZoneInfo.FindSystemTimeZoneById("Pacific/Auckland");
var tzBrasilia = TimeZoneInfo.FindSystemTimeZoneById("America/Sao_Paulo");
var tzBahia = TimeZoneInfo.FindSystemTimeZoneById("America/Bahia");
var dta = TimeZoneInfo.ConvertTimeFromUtc(dt, tzAuckland);
var sdta = String.Format("{0:U}",dta);
Console.WriteLine(sdta);

// GET ALL TIMEZONES
var dt = DateTime.UtcNow;
var timezones = TimeZoneInfo.GetSystemTimeZones();
foreach( var timezone in timezones)
{
	Console.WriteLine(timezone.Id);
	Console.WriteLine(timezone);
	var dtx = TimeZoneInfo.ConvertTimeFromUtc(dt, timezone);
	var sdtx = String.Format("{0:U}",dtx);
	Console.WriteLine(sdtx);
	Console.WriteLine("-----------------------------------");
}

// QT DAYS IN MONTH
Console.WriteLine(DateTime.DaysInMonth(2022,2));
//-> 28

// ADD OR SUBTRACT X DAYS
var dateNow = DateTime.Now;
var dateAfter = dateNow.AddDays(10);
//.AddMonths
//.AddYears
//.AddHours
//.AddMinutes
//.AddSeconds
//.AddDays(-10)

// NULL DATE
DateTime? dt = null;

// COMPARING ONLY THE DATES
var dt = DateTime.Now;
if(dt.Date == DateTime.Now.Date)
{
	Console.WriteLine("É igual");
}
// other comparators: <, <=, >, >=, !=, etc

using System.Globalization;
var dt = DateTime.Now;
var pt = new CultureInfo("pt-PT");
var br = new CultureInfo("pt-BR");
var en = new CultureInfo("en-US");
var de = new CultureInfo("de-DE");
var sdt = dt.ToString("d ddd dddd - M MM MMM MMMM - y yy yyy yyyy - dd/MM/yyyy HH:mm:ss:ff zz", de);
//-> 30 Di Dienstag - 8 08 Aug. August - 22 22 2022 2022 - 30.08.2022 20:26:23:58 -03
var ct = CultureInfo.CurrentCulture;
//-> pt-PT

// VERIFING IF IT'S WEEKEND
static void Main(string[] args)
{
	Console.Clear();
	var dt = DateTime.Now;
	Console.WriteLine( IsWeekend(dt.DayOfWeek) );
}
static bool IsWeekend(DayOfWeek today)
{
	return today == DayOfWeek.Saturday || today == DayOfWeek.Sunday;
}

// HORARIO DE VERAO
var dt = DateTime.Now.IsDaylightSavingTime();

var ts = new TimeSpan(1);
//-> 00:00:00.0000001
var hr = new TimeSpan(5, 12, 8);
//-> 05:12:08
var ms = new TimeSpan(5, 12, 8, 61);//dia,hora,minuto,segundos,milisegundos
//-> 5.12:09:01
Console.WriteLine(ms.Days);
//-> 5
Console.WriteLine(ms - hr);
//-> 5.06:56:53
var dt = DateTime.Now;
var dta = dt.Add( new TimeSpan(0, 12, 0, 0) );
var sdta = String.Format("{0:U}",dta);
//-> quarta-feira, 31 de agosto de 2022 12:34:22
```
