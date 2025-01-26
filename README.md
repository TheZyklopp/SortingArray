# SortingArray
````csharp
namespace SortingArray
{
    internal class Program
    {
        static void Main(string[] args)
        {
            string[] Namen = new string[4];
            Namen[0] = "Anna";
            Namen[1] = "Maximilian";
            Namen[2] = "Sophie";
            Namen[3] = "Paul";

            int max = 0;
            string laengsterName = "";

            foreach (string name in Namen)
            {
                Console.WriteLine(name.Length);
                int laenge = name.Length;
                if (laenge > 5)
                {
                    Console.WriteLine($"{name} hat mehr als 5 Buchstaben: {laenge}");
                }
                else if (laenge < 5)
                {
                    Console.WriteLine($"{name} hat weniger als 5 Buchstaben: {laenge}");
                }
                else
                {
                    Console.WriteLine($"{name} hat genau 5 Buchstaben.");
                }

                if (laenge > max)
                {
                    max = laenge;
                    laengsterName = name;
                }
            }
            Console.WriteLine($"der größte wert ist {max} mit dem Namen {laengsterName}");           
        }
    }
}
