<h1>Nested loops</h1>

<h2>Description</h2>
This is a example of a coding assignment I completed in Cis 199 that displays nested loops to output asterisks
<br />




<p align="center">
 <br/>
<img src="blob:https://imgur.com/a97ba100-032f-49a3-a16c-d4bb6c2577db" alt="]"/>
Code:
using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Lab7
{
    class Program
    {
        static void Main(string[] args)
        {

            int numStars; // declaring numStars variable
            numStars = 0; //numStars is equal to 0 

            do // using do loop
            {

                Console.WriteLine("Please enter number of stars: "); //displaying message for user to input number of stars
                string number; //declaring number as string
                number = Console.ReadLine(); //taking number input from user

                if (int.TryParse(number, out numStars)) //using tryparse to convert string to parse
                {
                    ShowSquareOfStars (numStars); //implementing ShowSquareofStars method to display square asterisk
                }

            }
            while (numStars < 0); // run lopp while numStars is less than 0
            Console.ReadLine(); // reads the line and stops the code from ending until user hits key to exit

        }
        public static void ShowSquareOfStars(int numStars) //declaring void method
        {

            for (int i = 0; i < numStars; i++) // loop is less than numStars
            {

                for (int x = 0; x < numStars; x++) //loop is less than numStars
                {
                    Console.Write("*"); // displays the asterisk

                }
                Console.Write("\n"); //Creating a new line and puts the * in  a row instead of one straight line


            }


        }
    }
}
