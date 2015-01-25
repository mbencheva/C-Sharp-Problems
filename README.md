# C-Sharp-Problems
//
using System;

class OddOrEven
{
    static void Main()
    {
        int numberSets = int.Parse(Console.ReadLine());
        int numbersPerSet = int.Parse(Console.ReadLine());
        string oddOrEven = Console.ReadLine();
        int[] mas = new int[numberSets];
        for (int i = 0; i < numberSets; i++)
        {
            int count = 0;
            for (int j = 0; j < numbersPerSet; j++)
            {
                int number = int.Parse(Console.ReadLine());
                if (oddOrEven == "odd")
                {
                    if (number % 2 != 0)
                    {
                        count++;
                    }
                    mas[i] = count;

                }
                if (oddOrEven == "even")
                {
                    if (number % 2 == 0)
                    {
                        count++;
                    }
                    mas[i] = count;

                }
            }
        }
        int a = 0;
        int max = 0;
        int numberS = 0;
        string display = "";
        if (mas[0] == mas[mas.Length - 1] && mas[mas.Length - 1] ==0)
        {
            Console.WriteLine("No");
        }

        else
        {

            for (int i = 0; i < mas.Length; i++)
            {
                if (mas[i] > a)
                {
                    max = mas[i];
                    a = mas[i];
                    numberS = i + 1;
                    
                }
            }
            display = GetDispaly(numberS);
            Console.WriteLine("{0} set has the most {1} numbers: {2}", display, oddOrEven, max);
        }


    }
    static string GetDispaly(int numberS)
    {
        switch (numberS)
        {
            case 1:
                return "First";
            case 2:
                return "Second";
            case 3:
                return "Third";
            case 4:
                return "Fourth";
            case 5:
                return "Fifth";
            case 6:
                return "Sixth";
            case 7:
                return "Seventh";
            case 8:
                return "Eighth";
            case 9:
                return "Ninth";
            default:
                return "Tenth";

        }

    }
