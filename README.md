![image](https://github.com/nikolay60109002/homework/assets/159818007/616b1596-1d26-4c4b-a0e4-f8c865259582)
using System;

class Program
{
    static void Main()
    {
        Commands();
        string fromUser = ReadInput("Введите команду: ");
        switch (fromUser)
        {
            case "1":
                var array1 = new string[] { "Hello", "2", "world", ":-)" };
                PrintArray(array1);
                break;
            case "2":
                var array2 = new string[] { "1234", "1567", "-2", "computer science" };
                PrintArray(array2);
                break;
            case "3":
                var array3 = new string[] { "Russia", "Denmark", "Kazan" };
                PrintArray(array3);
                break;
            default:
                Console.WriteLine($"{fromUser} - Такой команды нет");
                break;
        }
    }
    static void Commands()
    {
        Console.WriteLine();
        Console.WriteLine("СПИСОК КОМАНД:");
        Console.WriteLine("1 – использовать массив: [\"Hello\", \"2\", \"world\", \":-)\"]");
        Console.WriteLine("2 – использовать массив: [\"1234\", \"1567\", \"-2\", \"computer science\"]");
        Console.WriteLine("3 – использовать массив: [\"Russia\", \"Denmark\", \"Kazan\"]");
        Console.WriteLine();
    }
    static string ReadInput(string msg)
    {
        Console.Write(msg);
        return Console.ReadLine();
    }
    static void PrintArray(string[] array)
    {
        Console.Write("[ ");
        Console.WriteLine(string.Join(", ", array));
        Console.Write("] ");
    }
}
