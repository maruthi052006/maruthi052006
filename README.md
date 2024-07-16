

def guess_number_game():
    print("Welcome to the Number Guessing Game!")
    print("I'm thinking of a number between 1 and 100.")

    # Generate a random number between 1 and 100
    secret_number = random.randint(1, 100)
    attempts = 0

    while True:
        try:
            guess = int(input("Enter your guess (between 1 and 100): "))
            attempts += 1
            
            if guess < 1 or guess > 100:
                print("Please enter a number between 1 and 100.")
                continue
            
            if guess < secret_number:
                print("Too low! Try guessing higher.")
            elif guess > secret_number:
                print("Too high! Try guessing lower.")
            else:
                print(f"Congratulations! You guessed the number {secret_number} in {attempts} attempts!")
                break
        
        except ValueError:
            print("Invalid input! Please enter a valid number.")

if __name__ == "__main__":
    guess_number_game()
