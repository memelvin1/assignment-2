# assignment-2
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace ConsoleApp12
{
   
    class Program
    {

        static void Main(string[] args)
        {
            string reply = string.Empty;
            string userInput = string.Empty;


            try
            {
                int choice;
                do
                {

                    Console.WriteLine("1.Enter Triangle Dimensions:");
                    Console.WriteLine("2.exit:");
                    Console.WriteLine("Enter your choice:");
                    userInput = Console.ReadLine();
                }
                while ((int.TryParse(userInput, out choice) && userInput != "1" && userInput != "2"));

                if (userInput == "1")
                    
                {

                    do
                    {
                        int a;
                        int b;
                        int d;
                        Console.WriteLine("Enter the first side of triangle:");
                       string side1 = Console.ReadLine();
                         Console.WriteLine("Enter the second side of triangle:");
                        string side2 = Console.ReadLine();
                        Console.WriteLine("Enter the third side of triangle:");
                        string side3 = Console.ReadLine();

                        if (!(int.TryParse(side1, out a))
                            || (!(int.TryParse(side2, out b))) || (!(int.TryParse(side3, out d))))
                        {
                            Console.WriteLine("invalid");
                        }

                        //  if (!(Convert.ToInt32(Console.ReadLine()))
                        //  int a = Convert.ToInt32(Console.ReadLine());

                        else
                        {
                            TriangleSolver.Analyze(a, b, d);
                        }
                        Console.WriteLine("do you want to enter more?");
                        reply = Console.ReadLine();
                    }
                    while (reply.ToUpper() == "Y" );
                }
                else if (userInput == "2")
                {

                   System.Environment.Exit(0);
                }
            }
            catch (Exception e)
            {
                Console.WriteLine(e.Message);
            }
        }
    }
}
