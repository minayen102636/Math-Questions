using System;

namespace _1053010506作業6
{
    class Program
    {
        public static int ReverseInteger(int number)
        {
            int result = 0;
            int reminder;
            int negative = 0;

            if (number < 0)
            {
                number = -number;
                negative = 1;
            }


            while (number % 10 >= 0 && number > 0)
            {
                reminder = number % 10;
                result = result * 10 + reminder;
                number = (int)number / 10;
            }

            if (negative == 1)
            {
                result = -result;
            }


            return result;
        }


        public static int Question2(int[] array)
        {
            int max = array[0];
            int second = array[0];

            for (int i = 0; i < array.Length; i++)
            {
                if (max < array[i])
                {
                    second = max;
                    max = array[i];
                }

                else if (array[i] > second && array[i] < max)
                {
                    second = array[i];
                }
            }
            return second;
        }


        public static void Question3()
        {
            int[] array = { 15, 12, 17, 1 };

            for (int i = 0; i < 4; i++)
            {
                int number = 0 + array[i];
                Console.WriteLine(array[i]);

                if ((number % 2 == 0) || (number % 3 == 0) || (number % 5 == 0))
                {
                    Console.WriteLine("true");
                }

                else
                {
                    Console.WriteLine("false");
                }

            }

        }

        public static int Question4(int[] array)
        {
            int n = array.Length;
            int allsum = (n + 0) * (n + 1) / 2; //在沒有遺漏數字下的總和
            int sum = 0; //有遺漏數字下的總和
            int missing = 0;
            for (int i = 0; i < array.Length; i++)
            {
                sum = sum + array[i];
                missing = allsum - sum;
            }
            return missing;
        }

        public static int Question5(int[] array)
        {
            int n = array.Length;
            int count = 0; //計數器
            int currentcount = 1; //即時計數器

            for (int i = 0; i < n; i++)
            {
                if (i < n - 1 && array[i] == array[i + 1]) //前一個束子和現在數字相同
                {
                    currentcount++; //即時計數器加一
                }
                else
                {
                    if (currentcount > count) //即時計數器是否是最大的
                    {
                        count = currentcount;
                    }
                    currentcount = 1;
                }

            }
            return count;
        }



        public static void Main()
        {
            // Question1
            Console.WriteLine("123 to " + ReverseInteger(123));
            Console.WriteLine("-123 to " + ReverseInteger(-123));

            //Question2
            int[] array1 = { 1, 2, 3, 4, 5, 6, 7 };
            int[] array2 = { 9, 3, 6, 12, 5, 7 };
            Console.WriteLine(Question2(array1));
            Console.WriteLine(Question2(array2));

            Question3();

            //Question4
            int[] array3 = { 1, 3, 2, 5, 0 };
            int[] array4 = { 8, 6, 4, 1, 3, 2, 5, 0 };
            Console.WriteLine(Question4(array3));
            Console.WriteLine(Question4(array4));

            //Question5
            int[] array5 = { 1, 1, 1, 1, 0, 0, 1, 1, 1 };
            int[] array6 = { 1, 1, 0, 0, 1, 1, 1, 1, 1, 1 };
            Console.WriteLine(Question5(array5));
            Console.WriteLine(Question5(array6));

        }
    }
}
