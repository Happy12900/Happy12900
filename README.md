import random

def guessing_game():
    number = random.randint(1, 20)
    attempts = 3

    print("Welcome to the Guessing Game!")
    print("I'm thinking of a number between 1 and 20.")

    for attempt in range(1, attempts + 1):
        guess = int(input(f"Attempt {attempt}/{attempts}. Enter your guess: "))
        
        if guess < number:
            print("Your guess is too low.")
        elif guess > number:
            print("Your guess is too high.")
        else:
            print(f"Congratulations! You guessed the number ({number}) correctly!")
            return
    
    print(f"Sorry, you ran out of attempts. The number was {number}.")

