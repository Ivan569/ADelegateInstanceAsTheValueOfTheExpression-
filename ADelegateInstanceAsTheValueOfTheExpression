using System;

namespace ADelegateInstanceAsTheValueOfTheExpression
{
    // Делегат для работы с методами, 
    // имеющими целочисленный аргумент 
    // и целочисленный результат:
    delegate int MyDelegate(int number);
    // Класс с главным методом:
    class MyClass
    {
        public static void Main()
        {
            // Создание объекта:
            MyClassTwo myClassTwo = new MyClassTwo();
            // Переменные:
            sbyte k = 0;
            sbyte x = 0;
            // Вывод результата:
            Console.WriteLine(myClassTwo[x](k));
        }
    }
    // Класс с индексатором:
    class MyClassTwo
    {
        // Метод возвращает квадрат аргумента:
        private int MyMethod(int number)
        {
            return number * number;
        }
        // Метод возвращает значение аргумента:
        private int MyMethodTwo(int number)
        {
            return number;
        }
        // Индексатор результатом возвращает
        // ссылку на экземпляр делегата:
        public MyDelegate this[sbyte x]
        {
            // Аксессор для считывания значения:
            get
            {
                switch(x)
                {
                    case 0:
                        return MyMethod;
                    default:
                        return MyMethodTwo;
                }
            }
        }
    }
}
