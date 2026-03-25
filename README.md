# Primeiro-Projeto-

📐 Cálculo de Área de Triângulos com POO

Este projeto é uma aplicação de console desenvolvida em **C#** que tem como objetivo calcular e comparar as áreas de dois triângulos distintos. O cálculo é baseado na **Fórmula de Heron**, que permite encontrar a área de um triângulo conhecendo apenas as medidas de seus três lados.

 🚀 Funcionalidades
* Entrada de dados via console para os lados de dois triângulos ($x$ e $y$).
* Cálculo automático do semiperímetro e da área.
* Comparação lógica para determinar qual dos dois triângulos possui a maior área.
* Exibição dos resultados com formatação de precisão numérica.

Código Abaixo:


using System;
using System.Globalization;

namespace Course
{

    class Triangulo
    {
        public double a;
        public double b;
        public double c;
    }

    class Program
    {
        static void Main(string[] args)
        {
            Triangulo x, y;
            x = new Triangulo();
            y = new Triangulo();

            Console.WriteLine("Entre com as medidas do triangulo X: ");
            x.a = double.Parse(Console.ReadLine(), CultureInfo.InvariantCulture);
            x.b = double.Parse(Console.ReadLine(), CultureInfo.InvariantCulture);
            x.c = double.Parse(Console.ReadLine(), CultureInfo.InvariantCulture);

            Console.WriteLine("Entre com as medidas do triangulo Y: ");
            y.a = double.Parse(Console.ReadLine(), CultureInfo.InvariantCulture);
            y.b = double.Parse(Console.ReadLine(), CultureInfo.InvariantCulture);
            y.c = double.Parse(Console.ReadLine(), CultureInfo.InvariantCulture);

            double p = (x.a + x.b + x.c) / 2.0;
            double areaX = Math.Sqrt(p * (p - x.a) * (p - x.b) * (p - x.c));

            p = (y.a + y.b + y.c) / 2.0;
            double areaY = Math.Sqrt(p * (p - y.a) * (p - y.b) * (p - y.c));

            Console.WriteLine("Área de X = " + areaX.ToString("F4", CultureInfo.InvariantCulture));
            Console.WriteLine("Área de Y = " + areaY.ToString("F4", CultureInfo.InvariantCulture));

            if (areaX > areaY)
            {
                Console.WriteLine("Maior área: X");
            }
            else
            {
                Console.WriteLine("Maior área: Y");
            }
        }
    }
}
