![maxresdefault](https://user-images.githubusercontent.com/98576037/165406406-151dcde0-cae2-4ffd-8e16-c1fc90505733.jpg)

# **NUMBER GUESSING GAME**

# Information

* **Number Guessing Game: It is a game of chance played between the User and the Program. If the user knows the number randomly chosen by the program, the user wins.**

# Technologies Used

* **JAVA**

# Contents

* Arrays, Random and Scanner classes from the Util library are included in the project.

* The Random class allows the program to generate random numbers.

* The Arrays class is an assignment that facilitates the user's total rights and warning when entering numbers outside of the specified number values.

* The Scanner class is a recognized class to make it easier for the user to enter values.

* Evaluates false or winning predictions with a boolean variable true and false.

* The while loop is designed to repeat number input until the user has exhausted a total of 5.

* With if conditions, it sends a warning without allowing the user to deviate from certain rules.

<br />

# Codes

```Java

        import java.util.Arrays;

        import java.util.Random;

        import java.util.Scanner;


        public class NumberGuessingGame{

            public static void main(String[] args) {

                Random rand = new Random();

                int number = rand.nextInt(100);

                int right = 0;

                int selected;

                int[] wrong = new int[5];

                boolean isWin = false;

                boolean isWrong = false;


                Scanner input = new Scanner(System.in);


```

```Java

                while(right < 5){

                    System.out.print("Please enter your guess : ");

                    selected = input.nextInt();

                    if(selected < 0 || selected > 99){

                        System.out.println("Please enter a value between 0-100 ! ");

                        if(isWrong){

                            right++;

                            System.out.println("You made too many incorrect entries. Remaining right : " + (5 - right));

                        }else{

                            isWrong = true;

                            System.out.println("Your next wrong entry will be deducted from your rights.");

                        }

                        continue;

                    }

                    if(selected == number){

                        System.out.println("Congratulations, correct guess! Your guessed number is : " + number);

                        isWin = true;

                        break;

                    }else{

                        System.out.println("You entered an wrong number ! ");

                        if(selected > number){

                            System.out.println(selected + " You guessed too high ! ");

                        }else{

                            System.out.println(selected + " You guessed too small ! ");

                        }

                        wrong[right++] = selected;

                        System.out.println("Your remaining right : " + (5 - right));

                    }
                }

```
```Java

                if(!isWin){

                    System.out.println("You Lost ! ");

                    if(!isWrong){

                        System.out.println("Your guesses : " + Arrays.toString(wrong));

                    }
                }

            }
        }

```

```bash

    Please enter your guess : 55
    You entered an wrong number !
    55 You guessed too small !
    Your remaining right : 4
    Please enter your guess : 75
    You entered an wrong number !
    75 You guessed too high !
    Your remaining right : 3
    Please enter your guess : 68
    You entered an wrong number !
    68 You guessed too high !
    Your remaining right : 2
    Please enter your guess : 62
    You entered an wrong number !
    62 You guessed too high !
    Your remaining right : 1
    Please enter your guess : 59
    You entered an wrong number !
    59 You guessed too high !
    Your remaining right : 0
    You Lost !
    Your guesses : [55, 75, 68, 62, 59]

```

<br />

# LINK

* Click here https://github.com/Fogo9/NumberGuessingGame.git to access the Github page for this project.

<br />

# LICENSE

* This software is licensed By Tuncay Demir under the MIT license.

<br />

>[Patika.dev](https://app.patika.dev/fogomurphy)

<br/>

| Name |  Email |
| ---- |  ----- |
| Tuncay | tuncaydemir682@gmail.com |
