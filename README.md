# IFQ555
QueenslandCompetitionApp

The following real-world problem has been solved as a small programming exercise.

Queensland State hosts the Queensland Idol competition each summer during the state fair. The talent competition takes place over a three-day period during which contestants are eliminated following rounds of performances until the year’s ultimate winner is chosen.

This program named QueenslandCompetitionApp performs/allows the following:

Displays the number of tickets for adults, for children and for seniors and displays a statement that shows a statistic of visitors attending.
If the number of adult tickets is smaller than or equal to the total of children's and senior tickets, the app displays “The competition is becoming a festival for everyone!”.
If the number of children's tickets is greater than or equal to senior tickets, the app should display “The competition is attracting more and more young people!”.
In other cases, the app displays “The competition should have more space for kids!”.

The app is developed using simple logic.
The code can be tested using test data covering multiple cases.
The program is free from any compilations/execution errors.

namespace QueenslandCompetitionApp

{
    class Program

    {

        static void Main(string[] args)

        {
            //TASK1
            WriteLine("**************************");
            WriteLine("*The stars shine in Queensland*");
            WriteLine("**************************");


            //TASK2
            Console.WriteLine("Please enter amount of adults tickets sold & press enter");
            int adultTicket = int.Parse(Console.ReadLine());
            int adultTotal = adultTicket * 20;
            Console.WriteLine("Amount of adult tickets sold is $");
            Console.WriteLine(adultTicket * 20);
            Console.ReadLine();

            Console.WriteLine("Please enter amount of child tickets sold & press enter");
            int childTicket = int.Parse(Console.ReadLine());
            int childTotal = childTicket * 10;
            Console.WriteLine("Amount of child tickets sold is $");
            Console.WriteLine(childTicket * 10);
            Console.ReadLine();

            Console.WriteLine("Please enter amount of senior tickets sold & press enter");
            int seniorTicket = int.Parse(Console.ReadLine());
            int seniorTotal = seniorTicket * 6;
            Console.WriteLine("Amount of senior tickets sold is $");
            Console.WriteLine(seniorTicket * 6);
            Console.ReadLine();

            double revenue;
            revenue = adultTotal + childTotal + seniorTotal;
            Console.WriteLine("Calculating total revenue from competition tickets", revenue);
            Console.WriteLine(revenue.ToString("C2"));
            Console.ReadLine();

            //TASK3
            Console.WriteLine("Number of tickets sold is adult: {0}, children: {1} and senior: {2}", adultTicket, childTicket, seniorTicket);
            Console.ReadLine();
            int totalTickets;
            Console.WriteLine("Statistics of visitors attending");
            Console.WriteLine(totalTickets = adultTicket + childTicket + seniorTicket);
            Console.ReadLine();


            if ((adultTicket <= childTicket) && adultTicket <= seniorTicket)

                Console.WriteLine("The competition is becoming a festival for everyone!");

            else if ((adultTicket > childTicket) && adultTicket > seniorTicket)

                Console.WriteLine("The competition should have more space for kids!");

            if (childTicket >= seniorTicket)

                Console.WriteLine("The competition is attracting more and more young people");

            else if (childTicket < seniorTicket)

                Console.WriteLine("The competition should have more space for kids!");


        }

    }

}
