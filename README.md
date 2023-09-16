namespace ConsoleApp2
{
    internal class Program
    {
        static string normalphonenumber(string phonenumber)
        {
           
            if (phonenumber.StartsWith("+98"))
            {
                phonenumber = phonenumber.Replace("+98", "0");
            }
            return phonenumber;
        }
        static string ID(string Name, string lastname)
        {
            return Name + " " + lastname;
        }

        static void Main(string[] args)
        {
            Console.WriteLine("enter your name:");
            string Name = Console.ReadLine();
            Console.WriteLine("enter your last name:");
            string lastname = Console.ReadLine();
            Console.WriteLine("enter your fathername:");
            string Fathername = Console.ReadLine();
           
            Console.WriteLine("enter your phonenumber:");
            string phonenumber = Console.ReadLine();
            if (phonenumber.Length == 10)
            {
                Console.WriteLine(phonenumber = "0" + phonenumber);
            }
            else
            {
                Console.WriteLine(normalphonenumber(phonenumber));

            }

            Console.WriteLine("enter your birthyear:");
            string birthyear = Console.ReadLine();
            string birthday = birthyear;
            int year = 1402;
            int age = year - Convert.ToInt32(birthday);
            Console.WriteLine("your age is:" + age);


            Console.WriteLine("what is your gender?(male or female)");
            string gender = Console.ReadLine();


            Console.WriteLine(ID(Name, lastname));
            Console.WriteLine($"my name is:{Name} {lastname} my fathername is:{Fathername} i am {age} years old");
            Console.WriteLine("please choose?(1:detail,2:summary)");
            int choose = int.Parse(Console.ReadLine());

            if (choose == 1)
            {
                Console.WriteLine($"my name is:{Name} {lastname} my fathername is:{Fathername} i am {age} years old");
            }
            else
            {
                Console.WriteLine($"my name is:{Name} {lastname}");
            }


            bool isEligibleForService = gender == "male" && age >= 18 && age <= 50;
            if(isEligibleForService )
            {
                Console.WriteLine("isEligibleForService is true");
            }
            else
            {
                Console.WriteLine("isEligibleForService is False");
            }
        }
    }
}
