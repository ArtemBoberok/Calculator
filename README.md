# Calculator
#include <iostream>
#include <math.h>
using namespace std;

class Calculator
{
    float a, b;
public:

    void result()
    {
        cout << "Введите первое число: ";
        cin >> a;
        cout << "Введите второе число: ";
        cin >> b;
    }

    float add()
    {
        return a + b;
    }

    float sub()
    {
        return a - b;
    }

    float mul()
    {
        return a * b;
    }

    float div()
    {
        if (b == 0)
        {
            cout << "Деление на 0" <<
                endl;
            return INFINITY;
        }
        else
        {
            return a / b;
        }
    }
};

int main()
{
    setlocale(0, "ru");
    int ch;
    Calculator c;
    cout << "\tКалькулятор" <<
        "\nВведите 1 для сложения 2 чисел" <<
        "\nВведите 2 для вычитания 2 чисел" <<
        "\nВведите 3 для умножения 2 чисел" <<
        "\nВведите 4 для деления 2 чисел" <<
        "\nВведите 0 для выхода\n";

    do
    {
        cout << "\nВыберите действие: ";
        cin >> ch;
        switch (ch)
        {
        case 1:
            c.result();
            cout << "Результат: " <<
                c.add() << endl;
            break;
        case 2:
            c.result();
            cout << "Результат: " <<
                c.sub() << endl;
            break;
        case 3:
            c.result();
            cout << "Результат: " <<
                c.mul() << endl;
            break;
        case 4:
            c.result();
            cout << "Результат: " <<
                c.div() << endl;
            break;
        }
    } while (ch >= 1 && ch <= 4);
    return 0;
}
