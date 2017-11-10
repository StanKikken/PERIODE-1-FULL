using System;
using System.Collections.Generic;
using System.Linq;
using System.Text;
using System.Text.RegularExpressions;
using System.Threading.Tasks;

namespace periode_1
{
    class Program
    {
        static int correct = 0;
        static void Main(string[] args)
        {
            int Nummer1;
            int Nummer2;
            int Teller;
            int Aantal;

            double Keuze;
            double Bedrag1;
            double bedrag2;

            string Input;

            //FUNCTIE TEXTFILES
            string ReadFile(string src)
            {
                System.IO.StreamReader reader = new System.IO.StreamReader(Environment.CurrentDirectory + "/" + src);

                string line, re = "";
                while ((line = reader.ReadLine()) != null)
                {
                    re += line + "\n";
                }
                return Regex.Unescape(re);
            }
            //logo
            typewriter(ReadFile("TextFile27.txt"));
            Console.ReadLine();

            do
            {
                //OPTIE KIEZEN
                Console.Clear();
                Console.WriteLine(ReadFile("TextFile28.txt"));
                Console.WriteLine("Optie 1: Valuta omrekenen.");
                Console.WriteLine("Optie 2: Random number generator.");
                Console.WriteLine("Optie 3: Dagen op aarde checker.");
                Console.WriteLine("Optie 4: Alfabetisch sorteren ");
                Console.WriteLine("Optie 5: Lijst");
                Console.WriteLine("");
                Console.WriteLine("Geef de keuze hieronder op en druk op de enter toets");
                Console.WriteLine("");
                Keuze = Convert.ToDouble(Console.ReadLine());

                do
                {


                    do
                    {


                        if (Keuze == 1)
                        {
                            Console.Clear();
                            typewriter(ReadFile("TextFile1.txt"));
                            Input = Console.ReadLine().ToUpper();
                            if (Input == "EURO")
                            {
                                Console.Clear();
                                typewriter(ReadFile("TextFile2.txt"));
                                Input = Console.ReadLine().ToUpper();
                                if (Input == "DOLLAR")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile3.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in euro in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 1.16;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Euro = " + bedrag2.ToString() + " Amerikaanse Dollar");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }
                                }
                                if (Input == "YEN")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile4.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in euro in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 131.87;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Euro = " + bedrag2.ToString() + " Japanse Yen");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }
                                }
                                if (Input == "POND")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile5.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in euro in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.88;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Euro = " + bedrag2.ToString() + " Britse Pond");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }
                                }
                                if (Input == "YUAN")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile6.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in euro in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 7.69;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Euro = " + bedrag2.ToString() + " Chinese Yuan");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }

                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }
                                }
                            }

                            //DOLLAR
                            if (Input == "DOLLAR")
                            {
                                Console.Clear();
                                typewriter(ReadFile("TextFile7.txt"));
                                Input = Console.ReadLine().ToUpper();
                                if (Input == "EURO")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile8.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Dollar in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.86;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Dollar = " + bedrag2.ToString() + " Europese Euro");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "YEN")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile9.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Dollar in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 113.90;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Dollar = " + bedrag2.ToString() + " Japanse Yen");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "POND")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile10.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Dollar in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.76;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Dollar = " + bedrag2.ToString() + " Britse Pond");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "YUAN")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile11.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Dollar in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 6.64;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Dollar = " + bedrag2.ToString() + " Chinese Yuan");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }
                            }

                            //YEN
                            if (Input == "YEN")
                            {
                                Console.Clear();
                                typewriter(ReadFile("TextFile12.txt"));
                                Input = Console.ReadLine().ToUpper();
                                if (Input == "EURO")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile13.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Yen in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.0076;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Yen = " + bedrag2.ToString() + " Europese Euro");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "DOLLAR")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile14.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Yen in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.0088;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Yen = " + bedrag2.ToString() + " amerikaanse dollar");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "POND")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile15.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Yen in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.0067;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Yen = " + bedrag2.ToString() + " Britse Pond");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "YUAN")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile16.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Yen in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.058;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Yen = " + bedrag2.ToString() + " Chinese Yuan");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }
                            }

                            //POND
                            if (Input == "POND")
                            {
                                Console.Clear();
                                typewriter(ReadFile("TextFile17.txt"));
                                Input = Console.ReadLine().ToUpper();
                                if (Input == "EURO")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile18.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Pond in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 1.14;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Pond = " + bedrag2.ToString() + " Europese Euro");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "DOLLAR")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile19.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Pond in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 1.32;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Pond = " + bedrag2.ToString() + " amerikaanse dollar");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "YEN")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile20.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Pond in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 149.92;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Pond = " + bedrag2.ToString() + " Japanse yen");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "YUAN")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile21.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Pond in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 8.74;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Pond = " + bedrag2.ToString() + " Chinese Yuan");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }
                            }

                            //YUAN
                            if (Input == "YUAN")
                            {
                                Console.Clear();
                                typewriter(ReadFile("TextFile22.txt"));
                                Input = Console.ReadLine().ToUpper();
                                if (Input == "EURO")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile23.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Yuan in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.13;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Yuan = " + bedrag2.ToString() + " Europese Euro");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "DOLLAR")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile24.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Yuan in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.15;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Yuan = " + bedrag2.ToString() + " amerikaanse dollar");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "YEN")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile25.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Yuan in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 17.15;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Yuan = " + bedrag2.ToString() + " Japanse yen");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }

                                if (Input == "POND")
                                {
                                    Console.Clear();
                                    typewriter(ReadFile("TextFile26.txt"));
                                    Input = Console.ReadLine().ToUpper();
                                    if (Input == "JA")
                                    {
                                        correct = 1;
                                        Console.WriteLine("");
                                        Console.WriteLine("Geef hier het bedrag in Yuan in.");
                                        Console.WriteLine("");
                                        Bedrag1 = Convert.ToDouble(Console.ReadLine());

                                        bedrag2 = Bedrag1 * 0.11;
                                        Math.Round(bedrag2, 2);
                                        Console.WriteLine("");
                                        Console.WriteLine(Bedrag1.ToString() + " Yuan = " + bedrag2.ToString() + " Britse Pond");
                                        Console.ReadLine();

                                        Console.Clear();
                                        Console.WriteLine("Is dit het laatste bedrag wat u wilt omrekenen?");
                                        Console.WriteLine("Typ hieronder Ja of Nee en druk op de enter toets.");
                                        Input = Console.ReadLine().ToUpper();
                                        if (Input == "JA")
                                        {
                                            Console.Clear();
                                            credits();
                                        }
                                        if (Input == "NEE")
                                        {
                                            correct = 2;
                                        }
                                    }
                                    if (Input == "NEE")
                                    {
                                        correct = 0;
                                    }

                                }
                            }
                        }
                        //KEUZE 2
                        if (Keuze == 2)
                        {
                            Console.WriteLine("Geef hier de laagste waarde op");
                            Console.WriteLine("");
                            Nummer1 = Convert.ToInt16(Console.ReadLine());
                            Console.WriteLine("Geef hier de hoogste waarde op");
                            Console.WriteLine("");
                            Nummer2 = Convert.ToInt16(Console.ReadLine());
                            Console.WriteLine("");

                            Random rnd = new Random();
                            int Value = rnd.Next(Nummer1, Nummer2);
                            Console.WriteLine(Value);
                            Console.ReadLine();

                            Console.Clear();
                            Console.ReadLine();
                        }
                        //KEUZE 3
                        if (Keuze == 3)
                        {
                            Console.Clear();
                            Console.WriteLine("Voer het aub zo in (DD/MM/JJJJ)");
                            string myBirthday = Console.ReadLine();
                            DateTime mB = DateTime.Parse(myBirthday);
                            TimeSpan myAge = DateTime.Now.Subtract(mB);

                            Console.WriteLine("U Bent " + myAge.TotalDays + " Dagen Oud!");
                            Console.ReadLine();
                        }
                        else
                        {
                            correct = 3;
                        }

                        //KEUZE 4
                        if(Keuze == 4)
                        {
                            Console.Clear();
                            Console.WriteLine("Geef hier aan hoeveel woorden je wilt sorteren: ");
                            Aantal = Convert.ToInt32(Console.ReadLine());

                            String[] arraywoorden = new String[Aantal];

                            for (Teller = 0; Teller < Aantal; Teller++)
                            {
                                Console.WriteLine("Woord" + (Teller + 1).ToString() + ": ");
                                arraywoorden[Teller] = Console.ReadLine();
                            }
                            Console.WriteLine("");
                            Array.Sort(arraywoorden);
                            for(Teller = 0; Teller < Aantal; Teller++)
                            {
                                Console.WriteLine(arraywoorden[Teller]);
                            }
                            
                            Console.ReadLine();
                        }

                        //KEUZE 5
                        if(Keuze == 5)
                        {
                            List<int> list = new List<int>();
                            list.AddRange(new int[] { 1, 2, 3, 4, 5, 6, 7, 8, 9, 10 });
                            list.Clear();
                            list.Add(3);
                            list.Add(7);
                            list.Add(5);
                            list.Add(2);
                            Console.WriteLine("Count : " + list.Count);
                            foreach(int getal in list)
                            {
                                Console.WriteLine(getal.ToString());
                            }
                            Console.ReadLine();
                        }




                    } while (correct == 0);
                } while (correct == 2);
            } while (correct == 3);
        }

        

        //CREDITS
        public static void credits()
        {
            Console.Clear();
            Console.SetCursorPosition(10, 20);
            Console.WriteLine("Gemaakt door Stan Kikken");
            Console.ReadLine();
        }

        //Typewriter
        public static void typewriter(string tex)
        {
            foreach (char c in tex)
            {
                Console.Write(c);
                System.Threading.Thread.Sleep(5);
            }
        }
    }

}
