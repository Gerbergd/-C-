# Язык C#
Программа по инициализации переменной:

	 string myName;
	 myName = "Jane";

	 Console.WriteLine(myName);
	 
	 Console.ReadKey();

Использование строкового литерала:
    
    Console.WriteLine(MyName);

    Console.WriteLine("Привет, мир");
    Console.WriteLine("Мне 27 лет");
    Console.WriteLine("My name is Jane");

    Console.ReadKey();

Использование символьного литерала:

	const string MyName = "Jane";

	Console.WriteLine(MyName);

	Console.WriteLine("\t Привет Мир");
	Console.WriteLine("\t Мне 27 лет");
	Console.WriteLine("\t My name is \n {0}", MyName);
	Console.WriteLine("\u0040");
	Console.WriteLine("\x23")
	Console.ReadKey();

Использование логических литералов:

	Console.WriteLine(true);
    Console.WriteLine(false);
    
    Console.ReadKey();

Изучение типов переменных:

	string MyName = "Jane";
	byte MyAge = 27;
	bool HaveIApet  = true;
	double MyShoeSize = 37.5;

	Console.WriteLine("My name is " + MyName);
	Console.WriteLine("MyAge " + MyAge);
	Console.WriteLine("Do I have a pet? " + HaveIApet);
	Console.WriteLine("My shoe size is " + MyShoeSize);

Как определять минимальное и максимальное значения любого типа (на примере целочисленного типа):
	
	Console.WriteLine("IntMax {0}", int.MaxValue);
	Console.WriteLine("IntMin {0}", int.MinValue);

Перечисления (enum):

	//const byte Monday = 1;
    //const byte Tuesday = 2;
    //const byte Wednesday = 3;
    //const byte Thursday = 4;
    //const byte Friday = 5;
    //const byte Saterday = 6;
    //const byte Sunday = 7;
    // Такой вариант записи не эффективен, воспользуемся перечислением
    enum Semaphore : short
    {
		Red = 100,
        Yellow = 200,
        Green = 300
    }