# Primeiro-Projeto-

📐 Cálculo de Área de Triângulos com POO

Este projeto é uma aplicação de console desenvolvida em **C#** que tem como objetivo calcular e comparar as áreas de dois triângulos distintos. O cálculo é baseado na **Fórmula de Heron**, que permite encontrar a área de um triângulo conhecendo apenas as medidas de seus três lados.

 🚀 Funcionalidades
* Entrada de dados via console para os lados de dois triângulos ($x$ e $y$).
* Cálculo automático do semiperímetro e da área.
* Comparação lógica para determinar qual dos dois triângulos possui a maior área.
* Exibição dos resultados com formatação de precisão numérica.

* using Console_triangulo;
using System;
using System.Globalization;
namespace Course
{

    class Program
    {
        static void Main(string[] args)
        {
            triangulo x, y;
            x = new triangulo();
            y = new triangulo();

            Console.WriteLine("Entre com a medida do triangulo x: ");
            x.a = double.Parse(Console.ReadLine());
            x.b = double.Parse(Console.ReadLine());
            x.c = double.Parse(Console.ReadLine());

            Console.WriteLine("Entre com a medida do triangulo y: ");
            y.a = double.Parse(Console.ReadLine());
            y.b = double.Parse(Console.ReadLine());
            y.c = double.Parse(Console.ReadLine());

            double p = (x.a + x.b + x.c) / 2.0;
            double areax = Math.Sqrt(p * (p - x.a) * (p - x.b) * (p - x.c));
            p = (y.a + y.b + y.c) / 2.0;
            double areay = Math.Sqrt(p * (p - y.a) * (p - y.b) * (p - y.c));
            Console.WriteLine("Area de x = " + areax.ToString("F4"));
            if (areax > areay)
            {
                Console.WriteLine("Maior area: Y");
            }
        }
    }
}



