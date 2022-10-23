using System;
using System.Collections.Generic;
using System.Linq;

namespace SetsAndDictionaaries
{
    class Program
    {
        static void Main(string[] args)
        {
            var continents = new Dictionary<string, Dictionary<string, List<string>>>();
            var countries = new Dictionary<string, List<string>>();
            var N = int.Parse(Console.ReadLine());
            for (int i = 0; i < N; i++)
            {
                var input = Console.ReadLine().Split(" ", StringSplitOptions.RemoveEmptyEntries);
                var continent = input[0];
                var country = input[1];
                var city = input[2];

                if (!continents.ContainsKey(continent))
                {
                    if (!countries.ContainsKey(country))
                    {
                        countries[country] = new List<string>();
                        
                    }
                    continents[continent] = new Dictionary<string, List<string>>();
                    continents[continent].Add(country, countries[country]);
                    
                }
                if (!continents[continent].ContainsKey(country))
                {
                    continents[continent][country] = new List<string>();
                }
                continents[continent][country].Add(city);
                
            }
            foreach (var (continent, c) in continents)
            {
                Console.WriteLine($"{continent}:");
                foreach (var (country, cities) in c)
                {
                    Console.WriteLine($"{country} -> {string.Join(", ", cities)}");
                   
                }
               
            }
        }
    }
}
