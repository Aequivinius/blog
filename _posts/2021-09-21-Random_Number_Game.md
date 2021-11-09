---
layout: post
title: Random_Number_Game
---

# **How do i use while loop in an example like Random_Number_Guesser?**
### Welcome to Random_Number_Guesser
My goal was to program a first game with C# where the user guesses a randomly generated number.

There are 2 aims that i want to achieve with this because i had problems with them too:
1. The aim that you should have achieved after this page is to understand and realize the **"while loop"**.
2. You should be able to use **"while loop"** after this page by yourself and also use it in your own code.

I'll give you a little instructions on how to use the **"while loop"** on a short Game but you can use it for the code that you need but there are 3 important things you need to know about the while loop:

1. **bool**
2. **while**
3. **if and else** 

## Task of the Game
This is the used code for the programm to work.
What it basically does is:
1. Generating a random number.
2. Letting you guess by entering a number.
3. Compares the 2 numbers with each other and gives you 2 an output of 3 texts these are:

| 1. "Entered number to small." | 2. "Entered number to big."| 3. "Entered number equals the random number." |
| --- | --- | --- |
4. It subtracts 1 Attempt from your Attempts for every number you entered.
5. It tells you if the number you entered is equal to the random number and tells you the number of attempts that you had left.
6. It stops the whole programm when you reach the end of the given attempts.

And for all of these the while loop is essential for the programm to even work.

**The whole code that I've written is right under here for ilustration:**
Try to understand what it does and if you don't you can go ahead and read further into this.
```csharp
bool whileCont = true;

while (whileCont == true)
    {
      try
      {
        Console.ForegroundColor = ConsoleColor.Black;
        Console.WriteLine("Guess the number:");
        int guess = Convert.ToInt32(Console.ReadLine());

        if (ranNummer > guess)
        {
          attempts = attempts - 1;

          Console.ForegroundColor = ConsoleColor.Red;
          Console.WriteLine("Number to small please try again!");
          if (attempts == 0)
          {
            whileCont = false;
          }
       }
        else
       {
          if (ranNummer < guess)
          {
            attempts = attempts - 1;

            Console.ForegroundColor = ConsoleColor.Red;
            Console.WriteLine("Number to big please try again!");
            }
             else
            {
                if (ranNummer == guess)
                {
                    attempts = attempts - 1;
                    Console.ForegroundColor = ConsoleColor.Green;
                    Console.WriteLine("Well done!");
                    Console.WriteLine(FiggleFonts.Big.Render("Congrats  you  had  " + attempts + Attempts  left!"));
                    whileCont = false;
                }
            }
        }
    }
```

## Using While Loop

![Screenshot](https://i.imgur.com/nE30psj.png)

#### Step 1 *(Important for while loop)*
For using the loop you gotta make a bool first it doesn't matter for now what a bool exactly is but it does matter how you name him, because it should be a name that tells you exactly for what programm you need that bool for example i called mine *"whileCont"* and it stands for *"while controlling"* but feel free to use another one that fits better for your code.
My bool is **"whileCont = true""** and I am also working with an **"int attempts"** so you are using *"if"* and *"else"* as well.
#### Step 2 *(Important for while loop)*
Give the int attempts the number of attempts you want to have like **"int attempts = 10"**.
Now you do **"while (whileCont == true)"**.
#### Step 3
Make **"{"** write the **"try"** to find any invalid numbers or letters in that codeblock and at the end when you finished all the code that is in the loop you can make a **"}"** to close everything up and add the **"catch"**.
#### Step 4
Now you can write your **"if"** and **"else"** and programm what it should do if you aren't knowing any example there is one pictured above.
#### Step 5 *(Important for while loop)*
You do **"if (attempts == 0)"** then open a clamp and write in there what it should do if the attempts reached the end of the given attempts and equal 0 now.
I made it that if it reaches 0 that it says **"whileCont = false"** then the Programm ends.

## Finished Result
![Screenshot 1](https://i.imgur.com/gb4zCt0.png)
If you start the debugging on the programm by pressing the green arrow in Microsoft Visual Studio the programm should work and you should be able to guess your number.
If it is equal to the random generated number the console will tell you that it is correct by automatically giving you the number of the guesses you had left and a little congratulations text if it isn't it will tell you with the text that you have programmed if it's bigger or smaller than the guessed number and will ask you again and again and again until you are left with 0 guesses then programm ends.

Now you can play the Game
![Screenshot 2](https://i.imgur.com/8afAQ9U.png)
## Reflexion
I had Problems with the **"while loop"** and  **"if else"** so I lost an extreme amount of time there but at the end I think I learned quite much out of that.
## Verifikation
I reached all my aims that I've set for myself and even got more features than the task was  about.
