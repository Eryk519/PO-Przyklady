# PO-Przyklady

#1
   static void Main(string[] args)
        {
            int[] uczestnicy = { 19, 34, 23, 54, 31 };
            Console.WriteLine(uczestnicy[0]);
            Console.WriteLine(uczestnicy[1]);
            Console.WriteLine(uczestnicy[2]);
            Console.WriteLine(uczestnicy[3]);
            Console.WriteLine(uczestnicy[4]);
            Console.ReadKey();
        }
        
      #2
      
         static void Main(string[] args)
        {
            int[] uczestnicy = { 19, 34, 23, 54, 31 };
            for (int i = 0; i < 5; i++)
                Console.WriteLine(uczestnicy[i]);
            Console.ReadKey();
        }
        
        #3
        
           static void Main(string[] args)
        {
            int[] uczestnicy = { 19, 34, 23, 54, 31 };
            int i = 0;
            do
            {
                Console.WriteLine(uczestnicy[i]);
                i++;
            } while (i < 5);
            Console.ReadKey();
        }
    }
    #4
         static void Main(string[] args)
        {
            Console.WriteLine("Ile chcesz wpisać imion?");
            int rozmiar = Convert.ToInt32(Console.ReadLine());
            string[] imiona = new string[rozmiar];
            for (int i = 0; i < imiona.Length; i++)
            {
                Console.WriteLine("Podaj {0} imię", i + 1);
                imiona[i] = Console.ReadLine();
            }
            for (int i = 0; i < imiona.Length; i++)
            {
                Console.Write(imiona[i] + ", ");
            }
            Console.ReadKey();
        }
        #5
           static void Main(string[] args)
        {
            int[] uczestnicy = new int[] { 19, 34, 23, 54, 31 };
            int[] odwrotnie = new int[uczestnicy.Length];
            // Wpisywanie elementów do tablicy odwrotnie
            for (int i = uczestnicy.Length - 1; i >= 0; i--)
                odwrotnie[uczestnicy.Length - i - 1] = uczestnicy[i];
            // Wyświetlenie elementów tablicy odwrotnie
            for (int i = 0; i < odwrotnie.Length; i++)
                Console.WriteLine(odwrotnie[i]);
            Console.ReadKey();
        }
        #6
            static void Main(string[] args)
        {
            int[] uczestnicy = { 19, 34, 23, 54, 31 };
            int suma = 0;
            double srednia;
            Console.Write("Wiek uczestników: ");
            for (int i = 0; i < uczestnicy.Length; i++)
            {
                Console.Write("{0}, ", uczestnicy[i]);
                suma += uczestnicy[i];
            }
            srednia = (double)suma / uczestnicy.Length;
            Console.WriteLine();
            Console.WriteLine("Średnia: {0}", srednia);
            Console.ReadKey();
        }
        #7
        static void Main(string[] args)
        {
            int[] uczestnicy = { 19, 34, 70, 54, 31 };
            int max = uczestnicy[0]; 
            for (int i = 1; i < uczestnicy.Length; i++)
            {
                if (uczestnicy[i] > max)
                {
                    max = uczestnicy[i];
                }
            }
            Console.WriteLine("Najstarszy uczestnik ma {0} lat(a)", max);
            Console.ReadKey();
        }
    }
    #8
         static void Main(string[] args)
        {
            int[,] tablica2d = { { 1, 2 }, { 3, 4 }, { 5, 6 }, { 7, 8 } };
            for (int a = 0; a < 4; a++)
            {
                for (int b = 0; b < 2; b++)
                {
                    Console.Write("{0,3}", tablica2d[a, b]);
                }
                Console.WriteLine();
            }
            Console.WriteLine("Rozmiar: " + tablica2d.Length);
            Console.ReadKey();
        }
       #9
         static void Main(string[] args)
        {
            int[][] tab =
            {
                new int[] {1,2},
                new int[] {3,4,5,6},
                new int[] {7,8,9}
            };
            Console.WriteLine(tab[0].Length); // wypisze 2
            Console.WriteLine(tab[1].Length); // wypisze 4
            Console.WriteLine(tab[2].Length); // wypisze 3
            Console.ReadKey();
        }
        #10
             static void Main(string[] args)
        {
            int[][][] tab =
            {
                new int[][]
                {
                    new int[] {1,2},    
                    new int[] {3,4,5}
                }
            };
            Console.Write(tab[0][1][2]); // wypisze 5
            Console.ReadKey();
        }
        #11
         static void Main(string[] args)
        {
            int[][,] tab =
            {
                new int[,] { {1,2}, {3,4} },
                new int[,] { {5,6,7}, {8,9,10} }
             };
            Console.WriteLine(tab[1][0, 2]); // wypisze 7
            Console.ReadKey();
        }
        #12
                static void Main(string[] args)
        {
            int[][] tab =
            {
                new int[] {1,2},
                new int[] {3,4,5,6},
                new int[] {7,8,9}
            };
            foreach (int[] podtablica in tab)
            {
                foreach (int x in podtablica)
                {
                    Console.Write("{0,2}", x);
                }
                Console.WriteLine();
            }
            Console.ReadKey();
        }
        #13
                static void Main(string[] args)
        {
            string[][] zespoly = {
                        new string[] { "Adam", "Karol" },
                        new string[] { "Ola", "Ela", "Jan" } };
            for (int i = 0; i < zespoly.Length; i++)
            {
                for (int j = 0; j < zespoly[i].Length; j++)
                {
                    Console.Write("{0,-10}", zespoly[i][j]);
                }
                Console.WriteLine();
            }
            Console.ReadKey();
        }
        #14
             static void Main(string[] args)
        {
            int[] a = { 11, 22, 33, 44, 55, 66, 77, 88, 99 };
            int[] b = new int[10];
            Array.Copy(a, 2, b, 3, 5);
            foreach (int x in b)
            {
                Console.Write("{0}, ", x);
            }
            Console.ReadKey();
        }
        #15
           static void Main(string[] args)
        {
            int[] tab = { 1, 2, 3, 4, 5, 6, 7, 8, 9 };
            Array.Reverse(tab);
            foreach (int x in tab)
                Console.Write("{0,2}", x);
            Console.ReadKey();
        }
        #16
             static void Main(string[] args)
        {
            int[] tab = { 4, 2, 6, 23, 1, 3, 7, 0 };
            Array.Sort(tab); 
            for (int i = 0; i < tab.Length; i++)
                Console.WriteLine(tab[i]);
            Console.ReadKey();
        }
        #17
            static void Main(string[] args)
        {
            // elementy tablicy 0 1 2 3 4
            string[] imiona = { "Ala", "Ola", "Ela", "Tola", "Ela" };
            Console.WriteLine(Array.IndexOf(imiona, "Ela")); // wypisze 2
            Console.WriteLine(Array.IndexOf(imiona, "Iza")); // wypisze -1
            Console.ReadKey();
        }
        #18
             static void Main(string[] args)
        {
            string tekst = "Ala ma kota";
            int liczbaZnakow = 0;
            foreach (char litera in tekst)
                if (litera == 'a') liczbaZnakow++;
            Console.WriteLine("Litera a wystąpiła {0} razy", liczbaZnakow);
            Console.ReadKey();
        }
        #19
           static void Main(string[] args)
        {
            string tekst = "Ala ma kota";
            foreach (char litera in tekst)
                Console.WriteLine(litera);
            Console.ReadKey();
        }
        #20
          static void Main(string[] args)
        {
            string tekst = "Ala ma kota";
            string fragment;
            fragment = tekst.Substring(4, 7);
            Console.WriteLine(fragment); // wypisze "ma kot"
            Console.ReadKey();
        }
        #21
           static void Main(string[] args)
        {
            string tekst = "Ala ma kota";
            string nowyTekst;
            nowyTekst = tekst.Insert(7, "kanarka i ");
            Console.WriteLine(nowyTekst);
            Console.ReadKey();
        }
        #22
        
        
