using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Threading.Tasks;

namespace Odd_Even_Sum
{
    class Program
    {
        static void Main(string[] args)
        {
            int n = int.Parse(Console.ReadLine());

            int oddSum = 0;
            int evenSum = 0;

            for (int i = 1; i <= n; i++)
            {
                int m = int.Parse(Console.ReadLine());

                int level = i % 2;

                if (level == 1)
                {
                    oddSum += m;
                }
                else
                {
                    evenSum += m;
                }
            }

            int totalSum = Math.Abs(oddSum - evenSum);

            Console.WriteLine(totalSum == 0 
                ? $"Yes sum = {oddSum}"
                : $"No diff = {totalSum}");
        }
    }
}
