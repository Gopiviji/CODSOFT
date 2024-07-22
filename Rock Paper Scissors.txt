import random  

print("\nLet's play Rock-Paper-Scissors!") 
choices = ["rock", "paper", "scissors"]  

while True:  
    user_choice = input("Choose Rock, Paper, or Scissors (or type 'quit' to exit): ").strip().lower()  

    if user_choice == "quit" or user_choice == "exit":  
        print("Thanks for playing! Goodbye!")  
        break  

    if user_choice in choices:  
        computer_choice = random.choice(choices)  

        print(f"Your choice: {user_choice.capitalize()}")
        print(f"Computer's choice: {computer_choice.capitalize()}")

        if user_choice == computer_choice:
            print("It's a tie!")
        elif (
            (user_choice == "rock" and computer_choice == "scissors") or
            (user_choice == "paper" and computer_choice == "rock") or
            (user_choice == "scissors" and computer_choice == "paper")
        ):
            print("You win!")
        else:
            print("Computer wins!")
    else:
        print("Invalid choice. Please choose Rock, Paper, or Scissors or type 'quit' to exit.")