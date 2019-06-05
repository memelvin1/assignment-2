# assignment-2

              public static string Analyze(int a, int b, int c)
        {
           
            string values = string.Empty;
            string reply = string.Empty;
            string Sides = string.Empty;

           
            
           if (((a + b > c) && (a + c > b) &&(b + c > a))
                && a>0 && b>0 && c>0)
            {

                Console.WriteLine("given dimensions form a triangle");

                if (a == b && b == c) 
                {
                    Console.WriteLine(" Equilatoral Triangle");
                   
                }
                else if (a == b || b == c || a == c)
                {
                    Console.WriteLine("These sides form an isosceles Triangle");
                }
                else
                {

                    Console.WriteLine("These sides form a  scalene Triangle");
                }

            }
            else
            {
                Console.WriteLine("do not form a triangle");
            }
            



            return values;
        }

    }

}
