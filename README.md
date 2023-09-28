using System;

class Program
{
    static void Main(string[] args)
    {
        // Запросить у пользователя данные для регистрации
        Console.WriteLine("Добро пожаловать! Введите ваше имя:");
        string имя = Console.ReadLine();

        Console.WriteLine("Введите вашу электронную почту:");
        string почта = Console.ReadLine();

        Console.WriteLine("Введите пароль:");
        string пароль = Console.ReadLine();

        // Создать нового пользователя
        User новыйПользователь = new User(имя, почта, пароль);

        // Вывести информацию о новом пользователе
        Console.WriteLine();
        Console.WriteLine("Регистрация успешно завершена. Ваши данные:");
        Console.WriteLine("Имя: " + новыйПользователь.Имя);
        Console.WriteLine("Электронная почта: " + новыйПользователь.Почта);

        // Ожидание ввода, прежде чем закрыть консольное приложение
        Console.ReadLine();
    }
}

class User
{
    public string Имя { get; }
    public string Почта { get; }
    private string Пароль { get; }

    public User(string имя, string почта, string пароль)
    {
        Имя = имя;
        Почта = почта;
        Пароль = пароль;
    }
}
