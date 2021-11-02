# Random number guesser Portfolio
## Aufgabenstellung
Ich habe einen C# Programm gemacht, wo der Computer eine Geheimzahl zwischen 1 und 100 speichert und der Benutzer/in musst die Geheimzahl raten
##### Ziele
1. Ich mache einen Random Number Guesser
2. Ich probiere verschidene Methoden in C# zu benutzen
3. Ich lerne mehr über C# 

### Inhalt 1  
##### Bild
![bild](https://snipboard.io/nVrLOl.jpg)
### Inhalt 2
##### Youtube Link

[![description](http://img.youtube.com/vi/iriSuKcU61Y/0.jpg)](http://www.youtube.com/watch?v=iriSuKcU61Y)

### Inhalt 3
##### Code

```csharp
{
        static void Main(string[] args)
        {
            Random r = new Random();
            bool done = true;
            int Highscore = 0; 

            while (done == true )
            {
                
                int truenum = r.Next(1, 100);
                int f = 0;
                int tries = 0;
                
                Console.WriteLine("I've picked my number. Guess it or Die!");


                while (truenum != f)
                {
                    try
                    {
                        f = Convert.ToInt32(Console.ReadLine());
                        if (f < 1 || f > 100)
                        {
                            Console.ForegroundColor = ConsoleColor.Red;
                            Console.WriteLine("Please enter a number between 1 and 100");
                            Console.ForegroundColor = ConsoleColor.White;
                            tries--;
                        }
                        else if (f < truenum)

                        {
                            Console.ForegroundColor = ConsoleColor.Yellow;
                            Console.WriteLine("Number too low! go higher!");
                            Console.ForegroundColor = ConsoleColor.White;
                        }
                        else if (f > truenum)
                        {
                            Console.ForegroundColor = ConsoleColor.Yellow;
                            Console.WriteLine("Number too high! go lower!");
                            Console.ForegroundColor = ConsoleColor.White;
                        }
                        else { }
                        
                    }
                    catch
                    {
                        Console.ForegroundColor = ConsoleColor.Red;
                        Console.WriteLine("Guess must be a whole number!");
                        Console.ForegroundColor = ConsoleColor.White;
                        tries--;
                    }
                    tries++;
                }

                if(Highscore == 0) // Highscore
                {
                    Highscore = tries;
                }
                else if(Highscore != 0 && tries < Highscore)
                {
                    Highscore = tries;
                }

                Console.ForegroundColor = ConsoleColor.Green;
                Console.WriteLine("you got it! you get to live another day... took you " + tries + " tries");
                Console.WriteLine("your best result was "+Highscore+" tries!");
                Console.WriteLine("Do you want to try again? [y/n]");
                Console.ForegroundColor = ConsoleColor.White;
                bool dilemna = true;


                do
                {
                    string retry = Console.ReadLine();
                    if (retry == "y")
                    {
                        Console.WriteLine("Here we go again..");
                        dilemna = false;
                    }
                    else if (retry == "n")
                    {
                        done = false;
                        dilemna = false;
                    }
                    else
                    {
                        Console.ForegroundColor = ConsoleColor.Red;
                        Console.WriteLine("Please answer with y or n.");
                        Console.ForegroundColor = ConsoleColor.White;
                    }
                } while (dilemna == true);
            } 

                
        }
    }
```

## Reflektion und Verifikation
#### Was sind gut gelaufen?
- Die "Try Catch" Method ist an der ersten Implementierung sehr gut gelaufen. 
#### Was sind schlecht gelaufen?
- Wegen meiner Konzentration sind einige Methode schlecht gelaufen z.B. die Loops
- Die Wiederholung-Modus hat immer Problem bekommen, weil ich immer am Anfang des Loops ein ";" hinzufügt.
#### Was kann ich Verbessern
1. Ich sollte in der Zukunft mehr Konzentration haben und mehrmals den Code durchlesen und prüfe, ob alles funktionieren kann.
2. Ich sollte nicht mehr am Anfang eines Loops ein ";" schreiben.
# Verifikation
### Habe ich meine Ziele erreicht?
- Ziel 1: Das Programm funktioniert und alle Anforderungen für das Programm läuft!  
- Ziel 2: Wegen dieses Projekt habe ich viele Methoden benutzt und gelernt, z. B. While Loop/Do-While Loop /Try, Throw and Catch/If Else
- Ziel 3: Wegen dieses Projekt habe ich viel mehr über C# gelernt

