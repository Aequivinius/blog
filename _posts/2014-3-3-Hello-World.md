---
layout: post
title: Number Riddle
---

### **Aufgabenstellung**
Ich habe mithilfe der Programmiersprache "C#" ein kleines Progamm geschrieben, wo man das spiel "Number Riddle" spielen kann.
In dem spiel geht es darum, dass der Computer eine Zahl zwischen 1 und 100 nimmt und der Nutzer muss diese Zahl herausfinden.


### **Ziele**
- Meine Skills mit `while`-Schleifen verbessern


### **Was habe ich jetzt genau gemacht?**
Damit bestimmte Funktionen des Programmes funktionieren müssen, müssen sie in einer Schleife geschrieben werden, d. h. der Inhalt der Schleife wird die ganze Zeit wiederholt oder bis im code eine Regel gesetzt wurde, wann das Programm die Schleife verlassen soll. Hier ein Beispiel von meinem Code:

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
          
 ```
Es wurde zuerst ein `bool` mit dem Namen _found_ erstellt. Der Wert wurde auf `false` gesetzt.
Danach haben wir hier mithilfe von `while` eine Schleife erstellt. Alles was innerhalb der ersten und der zweiten geschweiften Klammer ist, wird immer wieder wiederholt. Nun um die Schleife zu verlassen können, muss der Wert der `while` schleife nicht mehr stimmen. In unserem Fall ist der Wert des `bool`'s und der Schleife auf `false` gesetzt d. h. wir treten direkt in die schleife ein und führen den code aus. Zu unterst sehen wir den code `found = true;` der sorgt dafür das unser Programm aus der Schleife geht. Warum? Weil der wert von _found_ auf `true` gesetzt wurde und das Programm immer schaut, was der Wert der whilfe schleife ist. Und da sich ja der Wert geändert hat verlässt das Programm die Schleife!

### **Reflektion**
Im grossen und ganzen hatte ich Mega Spass and diesem Projekt! Meine Hilfe holte ich mir aus den verschiedensten SubReddits, Stack Overflow und von einem Freund ^^. Für das nächste mal sollte ich mehr mit einem PAP arbeiten! Ich habe am anfang des Projekts direkt mit dem realisieren des Projekts angefangen und diese falsche Vorgehensweise hat mir sehr viel Zeit gekostet!

### **Verifikation**
Mein Ziel war es meine Skills mit der `while` Schleife zu verbessern, und das ist mir wirklich gelungen! Als wir das Projekt zum ersten mal behandelt haben bekam ich einen kurzen Schock als ich von den Mitschülern hörte das man eine oder mehr `while` Schleifen bräuchte, doch mit Hilfe vom Internet und meines Freundes bin ich jetzt viel Versierter was einer `while` schleife angeht!
