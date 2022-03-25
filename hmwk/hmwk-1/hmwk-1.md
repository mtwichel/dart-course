# Homework 1 - Guessing Game

This small project will help you practice using variables and conditionals.

## Description
You will build a simple guessing game:
1. The program will think of a number between two numbers that should be configurable in the program. 
2. The user will guess a number.
3. The program will tell the user they guessed correctly.
    - If they guessed right, the program congradulates the user and exits.
    - If they guessed wrong, the program will tell them if the guess was too high or too low. It then prompts the user to guess again.

## Example Output

```bash
$ dart guessing_game.dart

Welcome to my guessing game!

Guess a number between 1 and 10.
> 5

Too low! Guess again.
> 8

Too high! Guess again.
> 7

Correct! Great job!
exit
```

## Extra Challenge
Here are a few ideas to modifiy the game for an extra programming challenge:
1. Start the game by asking the range of numbers to guess from instead of putting it in the program.
2. Make it a two player game by making one player choose the number and the other player guesses. You'll have to find a way to make sure the guesser doesn't see the first players inputed number.
3. This guessing game is similar to the game Wordle. Try changing the game so you:
    - Have a limited number of guesses
    - Guess 5 digit words instead of numbers
    - Let the game tell you how many letters you got right and/or if they're in the right location