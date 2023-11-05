# Contagem regressiva

```c#
using System;
using System.Threading;

namespace ContagemRegressiva
{
    class Program
    {
        static void Main(string[] args)
        {
            Menu();
        }
        static string Input(string df)
        {
            string vl = Console.ReadLine() ?? df;
            vl = String.IsNullOrEmpty(vl) ? df : vl;
            return vl;
        }
        static void Menu()
        {
            try
            {
                Console.Clear();
                Console.WriteLine("S-Segundos => 10s = 10 Segundos");
                Console.WriteLine("M-Minutos => 1m = 1 Minuto");
                Console.WriteLine("0-Sair");
                Console.WriteLine("Quanto tempo deseja contar?");

                string data = Input("0");

                if(data == "0")
                {
                    System.Environment.Exit(0);
                }else
                {
                    data = data.ToLower();
                    char type = char.Parse( data.Substring( data.Length - 1, 1 ) );
                    int time = int.Parse( data.Substring(0, data.Length - 1) );
                    //Console.WriteLine(data);
                    //Console.WriteLine(type);
                    //Console.WriteLine(time);
                    Console.Clear();
                    Console.WriteLine("0-Não");
                    Console.WriteLine("1-Sim");
                    Console.WriteLine("A contagem é regressiva?");
                    int rg = int.Parse( Input("0") );

                    int multiplier = 1;

                    if(type == 'm') multiplier = 60;

                    PreStart(time * multiplier, rg);
                }
            }catch(Exception er)
            {
                Console.Clear();
                Console.WriteLine("Menu:");
                Console.WriteLine(er.Message);
            }
        }
        static void PreStart(int time, int rg)
        {
            try
            {
                Console.Clear();
                Console.WriteLine("Ready...");
                Thread.Sleep(1000);
                Console.WriteLine("Set...");
                Thread.Sleep(1000);
                Console.WriteLine("Go...");
                Thread.Sleep(1000);
                Start(time, rg);
            }catch(Exception er)
            {
                Console.Clear();
                Console.WriteLine("PreStart:");
                Console.WriteLine(er.Message);
            }
        }
        static void Start(int time = 10, int rg = 0)
        {
            try
            {
                if(rg == 0)
                {
                    /*
                    int currentTime = 0;
                    while(currentTime != time)
                    {
                        currentTime++;
                        Console.Clear();
                        Console.WriteLine(currentTime);
                        Thread.Sleep(1000);
                    }
                    */
                    for(int i = 0; i < time; i++)
                    {
                        Console.Clear();
                        Console.WriteLine(i + 1);
                        Thread.Sleep(1000);
                    }
                }else
                {
                    for(int i = time; i > 0; i--)
                    {
                        Console.Clear();
                        Console.WriteLine(i);
                        Thread.Sleep(1000);
                    }
                }
                Console.Clear();
                Console.WriteLine("Fim");
            }catch(Exception er)
            {
                Console.Clear();
                Console.WriteLine("Start:");
                Console.WriteLine(er.Message);
            }
        }
    }
}
```
