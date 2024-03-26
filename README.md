# Язык C#
Программа по инициализации переменной:
using System;

class MainClass {
  public static void Main (string[] args) {

	 string myName;
	 myName = "Jane";

	 Console.WriteLine(myName);
	 
	 Console.ReadKey();
  }
}

Использование строкового литерала:
static void Main(string[] args)
{
    const string MyName = "Jane";
    
    Console.WriteLine(MyName);

    Console.WriteLine("Привет, мир");
    Console.WriteLine("Мне 27 лет");
    Console.WriteLine("My name is Jane");

    Console.ReadKey();
}
