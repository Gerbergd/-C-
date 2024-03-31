# Язык C#
#### Программа по инициализации переменной:

	 string myName;
	 myName = "Jane";

	 Console.WriteLine(myName);
	 
	 Console.ReadKey();

#### Использование строкового литерала:
    
    Console.WriteLine(MyName);

    Console.WriteLine("Привет, мир");
    Console.WriteLine("Мне 27 лет");
    Console.WriteLine("My name is Jane");

    Console.ReadKey();

#### Использование символьного литерала:

	const string MyName = "Jane";

	Console.WriteLine(MyName);

	Console.WriteLine("\t Привет Мир");
	Console.WriteLine("\t Мне 27 лет");
	Console.WriteLine("\t My name is \n {0}", MyName);
	Console.WriteLine("\u0040");
	Console.WriteLine("\x23")
	Console.ReadKey();

#### Использование логических литералов:

	Console.WriteLine(true);
    Console.WriteLine(false);
    
    Console.ReadKey();

#### Изучение типов переменных:

	string MyName = "Jane";
	byte MyAge = 27;
	bool HaveIApet  = true;
	double MyShoeSize = 37.5;

	Console.WriteLine("My name is " + MyName);
	Console.WriteLine("MyAge " + MyAge);
	Console.WriteLine("Do I have a pet? " + HaveIApet);
	Console.WriteLine("My shoe size is " + MyShoeSize);

#### Как определять минимальное и максимальное значения любого типа (на примере целочисленного типа):
	
	Console.WriteLine("IntMax {0}", int.MaxValue);
	Console.WriteLine("IntMin {0}", int.MinValue);

#### Перечисления (enum):

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
#### Методы преобразования типов переменных:
            
            int olddata = 6;
            long data = (long)olddata;

            int olddata = 5;
            string data = olddata.tostring();

            console.writeline("enter your age: ");
            int age = convert.toint32(console.readline());
            console.writeline("your age is {0}", age);
            console.readkey();

            // parse - методы, который при наличии ошибки он возвращает
            // эту ошибку и не производит дальнейших операций.
            // tryparse - метод, возвращающий булевое значение в
            // зависимости от того, было ли преобразование удачным.
            console.write("enter your age: ");
            int age = int.parse(console.readline());
            console.writeline("your age is {0} ", age);
            console.readkey();

            console.write("enter your age: ");
            int age;
            bool iscorrect = int.tryparse(console.readline(), out age);
            console.writeline("your age is {0} ", age);
            console.readkey();

            console.write("enter your age: ");
            byte age = (byte)int.parse(console.readline());
            console.writeline("age is {0} ", age);
            console.readkey();

            // checked - служебное слово помогающее проверить,
            // возможно ли преобразование без потерим данных

            console.write("enter your name: ");
            string name = console.readline();
            console.write("enter your age: ");
            byte age = checked((byte)int.parse(console.readline()));
            console.writeline("your name is {0} and age is {1} ", name, age);
            console.writeline("what is your favorite day a week?");
            dayofweek day = (dayofweek)int.parse(console.readline());
            console.writeline($"your favorite day is {day}");
            console.readkey();

            var name = Console.ReadLine();

            var age = checked((byte)int.Parse(Console.ReadLine()));
            Console.WriteLine("Your name is {0} and age is {1} ", name, age);

            Console.Write("What is your favorite day of week? ");

            var day = (DayOfWeek)int.Parse(Console.ReadLine());
            Console.WriteLine("Your favorite day is {0}", day);

#### Использование условных операций (if, else if, else):
            
            var a = 6;
            var b = 7;

            if (a == b && b > 1)
            {
                Console.WriteLine("Условие истинно");
            }

            else if (b > 10 || b == 7)
            {
                Console.WriteLine("Значение b = {0} больше 10 или равно 7", b);
            }
            else
            {
                Console.WriteLine("Значение b = {0}", b);
            }

#### Использование сокращённой записи условной операции if/else:
            
            var a = 6;
            var b = 7;

            var c = a != b ? a + b : b;

            // a != b - условие, после ? пишется ответ если условие истинно,
            // после : пишется ответ если условие ложно.
            Console.WriteLine(c);

#### Окрашивание фона букв и цвет контура букв:

            Console.WriteLine("Напишите свой любимый цвет на английском с маленькой буквы");

            var color = Console.ReadLine();

            if (color == "red")
            {
                Console.BackgroundColor = ConsoleColor.Red;
                Console.ForegroundColor = ConsoleColor.Black;

                Console.WriteLine("Your color is red!");
            }

            else if (color == "green")
            {
                Console.BackgroundColor = ConsoleColor.Green;
                Console.ForegroundColor = ConsoleColor.Black;

                Console.WriteLine("Your color is green!");
            }
            else
            {
                Console.BackgroundColor = ConsoleColor.Cyan;
                Console.ForegroundColor = ConsoleColor.Black;

                Console.WriteLine("Your color is cyan!");
            }

#### Использование switch-конструкции:

            Console.WriteLine("Напишите свой любимый цвет на английском с маленькой буквы");

            var color = Console.ReadLine();

            switch (color)
            {
                case "red":
                    Console.BackgroundColor = ConsoleColor.Red;
                    Console.ForegroundColor = ConsoleColor.Black;

                    Console.WriteLine("Your color is red!");
                    break;

                case "green":
                    Console.BackgroundColor = ConsoleColor.Green;
                    Console.ForegroundColor = ConsoleColor.Black;

                    Console.WriteLine("Your color is green!");
                    break;

                default:
                    Console.BackgroundColor = ConsoleColor.Cyan;
                    Console.ForegroundColor = ConsoleColor.Black;

                    Console.WriteLine("Your color is cyan!");
                    break;
            }
            //Блок *default* — это если значение не соответствует ни одному из условий.
            //Он является правилом хорошего тона, но его можно опустить.
            //Оператор *break* показывает, где кончилась последовательность действий для заданного условия.
            //Он обязателен, но можно также использовать вместо него другие операторы перехода: goto case, return или throw.
            //* return — это выход из метода, применять его будем позже.
            //* goto case — позволяет перейти к другому условию внутри блока switch.
            //* throw применяется для выбора ошибок, и мы рассмотрим его в других модулях.

#### Использование циклов и команды continue:
            do
            {
                Console.WriteLine("Напишите свой любимый цвет на английском с маленькой буквы");
                var color = Console.ReadLine();

                switch (color)
                {
                    case "red":
                        Console.BackgroundColor = ConsoleColor.Red;
                        Console.ForegroundColor = ConsoleColor.Black;

                        Console.WriteLine("Your color is red!");
                        break;

                    case "green":
                        Console.BackgroundColor = ConsoleColor.Green;
                        Console.ForegroundColor = ConsoleColor.Black;

                        Console.WriteLine("Your color is green!");
                        break;

                    case "cyan":
                        Console.BackgroundColor = ConsoleColor.Cyan;
                        Console.ForegroundColor = ConsoleColor.Black;

                        Console.WriteLine("Your color is green!");
                        break;

                    case "yellow":
                        Console.BackgroundColor = ConsoleColor.Yellow;
                        Console.ForegroundColor = ConsoleColor.Red;

                        Console.WriteLine("Your color is yellow!");
                        break;

                    default:
                        continue;
                }
            } while (true);

#### Пример инициализации массива с циклом foreach:
        string[] favoriteColor = new string[3];
            for (int i = 0; i < favoriteColor.Length; i++)
            {
                Console.WriteLine("Введите любимый цвет номер {0}", i + 1);
                favoriteColor[i] = Console.ReadLine();
            }
         foreach (var color in favoriteColor)
         {
            switch (color)
            {
                case "red":
                    Console.BackgroundColor = ConsoleColor.Red;
                    Console.ForegroundColor = ConsoleColor.Black;

                    Console.WriteLine("Your color is red!");
                    break;

                case "green":
                    Console.BackgroundColor = ConsoleColor.Green;
                    Console.ForegroundColor = ConsoleColor.Black;

                    Console.WriteLine("Your color is green!");
                    break;

                case "cyan":
                    Console.BackgroundColor = ConsoleColor.Cyan;
                    Console.ForegroundColor = ConsoleColor.Black;

                    Console.WriteLine("Your color is green!");
                    break;

                case "yellow":
                    Console.BackgroundColor = ConsoleColor.Yellow;
                    Console.ForegroundColor = ConsoleColor.Red;

                    Console.WriteLine("Your color is yellow!");
                    break;

                default:
                    continue;
                }
            }

#### Разновидности инициализаций переменных в массивах и использование свойства length - свойство массива, которое вернёт кол-во элементов массива:
            //Размерность массива 
            var arr = new int[] { 1, 2, 3, 4 };
            var l = arr.Length;

            //Разные виды инициализации массива
            int[] arr1 = new int[4] { 1, 2, 3, 5 };
            int[] arr2 = new int[] { 1, 2, 3, 5 };
            int[] arr3 = new[] { 1, 2, 3, 5 };
            int[] arr4 = { 1, 2, 3, 5 };

#### Использование строки как массива:
                Console.Write("Введите свё имя: ");
                var name = Console.ReadLine();

                Console.WriteLine("Ваше имя по буквам");
                foreach (var ch in name)
                {
                    Console.Write(ch + " ");
                }
                Console.WriteLine("\n Последняя буква вашего имени: " + name[name.Length - 1]);

#### Запись имени в обратном порядке:
            Console.Write("Введите свё имя: ");
            var name = Console.ReadLine();

            Console.WriteLine("Ваше имя в обратном порядке: ");
            for(int i = name.Length-1;  i >= 0; i--)
            {
                Console.Write(name[i] + " ");
            }