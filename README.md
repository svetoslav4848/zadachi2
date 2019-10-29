# zadachi2
zadacha1

using System;

namespace zadacha20
{
    class Program
    {
        static void Main(string[] args)
        {
            int dayOfReservation = int.Parse(Console.ReadLine());
            int monthOfReservation = int.Parse(Console.ReadLine());
            int dayOfAccommodation = int.Parse(Console.ReadLine());
            int monthOfAccommodation = int.Parse(Console.ReadLine());
            int dayOfLeave = int.Parse(Console.ReadLine());
            int monthOfLeave = int.Parse(Console.ReadLine());
            int costPerDay = 30;
            int days =   dayOfLeave - dayOfAccommodation;
           

            if (monthOfReservation < monthOfAccommodation)
            {
                costPerDay = 25 - (25  * 20 / 100);
            }
            else if (dayOfReservation <= dayOfAccommodation - 10 )
            {
                costPerDay = 25;
            }
            double totalPrise = costPerDay * days;


            Console.WriteLine("Your stay from {0}/{1} to {2}/{3} will cost {4}", dayOfAccommodation , monthOfAccommodation ,dayOfLeave, monthOfLeave, totalPrise);

        }
    }
}



zadacha2




using System;

namespace zadacha5_ot_shkolata
{
    class Program
    {
        static void Main(string[] args)
        {
            string sushi = Console.ReadLine();
            string restaurant = Console.ReadLine();
            int servings = int.Parse(Console.ReadLine());
            char delivery = char.Parse(Console.ReadLine());
            string sushiZone = "Sushi Zone";
            string sushiTime = "Sushi Time";
            string sushiBar = "Sushi Bar";
            string asianPub = "Asian Pub";
            string sashimi = "sashimi";
            string maki = "maki";
            string uramaki = "uramaki";
            string temaki = "temaki";


            if (restaurant != "Sushi Zone" && restaurant != "Sushi Time"
                && restaurant != "Sushi Bar" && restaurant != "Asian Pub")
            {
                Console.WriteLine(" {0} is invalid restaurant!", restaurant);
            }
            else
            {
                double prise = 0;
                if (sushi == "sashimi")
                {
                    if (restaurant == sushiZone)
                    {
                        prise = 4.99;
                    }
                    else if (restaurant == sushiBar)
                    {
                        prise = 5.25;
                    }
                    else if (restaurant == sushiTime)
                    {
                        prise = 5.49;
                    }
                    else if (restaurant == asianPub)
                    {
                        prise = 4.50;
                    }
                }
                else if (sushi == "maki")
                {
                    if (restaurant == sushiZone)
                    {
                        prise = 5.29;
                    }
                    else if (restaurant == sushiBar)
                    {
                        prise = 5.55;
                    }
                    else if (restaurant == sushiTime)
                    {
                        prise = 4.69;
                    }
                    else if (restaurant == asianPub)
                    {
                        prise = 4.80;
                    }
                }
                else if (sushi == "uramaki")
                {
                    if (restaurant == sushiZone)
                    {
                        prise = 5.99;
                    }
                    else if (restaurant == sushiBar)
                    {
                        prise = 6.25;
                    }
                    else if (restaurant == sushiTime)
                    {
                        prise = 4.49;
                    }
                    else if (restaurant == asianPub)
                    {
                        prise = 5.50;
                    }
                }
                else if (sushi == "temaki")
                {
                    if (restaurant == sushiZone)
                    {
                        prise = 4.29;
                    }
                    else if (restaurant == sushiBar)
                    {
                        prise = 4.75;
                    }
                    else if (restaurant == sushiTime)
                    {
                        prise = 5.19;
                    }
                    else if (restaurant == asianPub)
                    {
                        prise = 5.50;
                    }
                }
                double totalPrise = 0;               
                if (delivery == 'Y')
                {                   
                    totalPrise = (prise * servings) + ((prise * servings * 20) / 100);
                }
                else if(delivery == 'N')
                {                 
                    totalPrise = prise * servings;
                }
                Console.WriteLine("Total price: {0} lv.",totalPrise);
            }
        }
    }
}

//tuk malko prerabotih tazi zadacha koqto reshavahme 





zadacha3



using System;

namespace Check_for_a_Play_Card
{
    class Program
    {
        static void Main(string[] args)
        {
            string card = Console.ReadLine();

            if( card == "J" || card =="Q" || card =="K" || card =="A" || card == "2" || card == "3" || card == "4" || card == "5" || card == "6" || card == "7" || card == "8" || card == "9")
            {
                Console.WriteLine("yes");
            }
            else
            {
                Console.WriteLine("No");
            }
        }
    }
}
