---
layout: post
title: Number Riddle
---

### **Aufgabenstellung**
Ich habe mithilfe der Programmiersprache "C#" ein kleines Progamm geschrieben, wo man das spiel "Number Riddle" spielen kann.
In dem spiel geht es darum, dass der Computer eine Zahl zwischen 1 und 100 nimmt und der Nutzer muss diese Zahl herausfinden.


### **Ziele**
- Meine Skills mit While-Schleifen verbessern


### **Was habe ich jetzt genau gemacht?**
Damit bestimmte Funktionen des Programmes funktionieren müssen sie in einer Schleife geschrieben werden, dh. der inhalt der schleife wird dei ganze zeit wiederholt oder bis im code eine Regel gesetzt wurde wann das Programm die Schleife verlassen soll. Hier ein Beispiel von meinem Code:

```csharp
bool found = false;

            while (found == false)
            {
                string userinput = Console.ReadLine();
                attempts++;
                if (int.TryParse(userinput, out int test))
                {
                    int usernumber = int.Parse(userinput);
                    if (usernumber == rand_num)
                    {
                        Console.Clear();
                        Console.ForegroundColor = ConsoleColor.Green;
                        Console.WriteLine($"{rand_num} was the right number! GG!");
                        Console.ForegroundColor = ConsoleColor.White;
                        Console.WriteLine($"It took you {attempts} attempts to find out the right number!");
                        found = true;
                    }
                    else
                    {

                        if (usernumber < rand_num)
                        {
                            Console.ForegroundColor = ConsoleColor.Red;
                            Console.WriteLine("Your number is too small!");
                            Console.ForegroundColor = ConsoleColor.White;
                            attempts++;
                        }
                        else if (usernumber > rand_num)
                        {
                            Console.ForegroundColor = ConsoleColor.Red;
                            Console.WriteLine("Your number is too big!");
                            Console.ForegroundColor = ConsoleColor.White;
                            attempts++;
                        }
                    }
                }
                else
                {
                    Console.ForegroundColor = ConsoleColor.Red;
                    Console.WriteLine("An Error occured! Make sure to type in a number!");
                    Console.ForegroundColor = ConsoleColor.White;
                    attempts++;
                }
 ```


### **Reflektion & Verifikation**
