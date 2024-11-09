# Codsoft-Task-4
import random

# Function to get the computer's choice
def get_computer_choice():
    choices = ['rock', 'paper', 'scissors']
    return random.choice(choices)

# Function to determine the winner
def determine_winner(player_choice, computer_choice):
    if player_choice == computer_choice:
        return "It's a tie!"
    
    if (player_choice == 'rock' and computer_choice == 'scissors') or \
       (player_choice == 'paper' and computer_choice == 'rock') or \
       (player_choice == 'scissors' and computer_choice == 'paper'):
        return "You win!"
    
    return "You lose!"

# Main function to run the game
def play_game():
    print("Welcome to Rock, Paper, Scissors!")
    
    # Game loop
    while True:
        # Get player's choice
        player_choice = input("\nEnter your choice (rock, paper, scissors). To quit, type 'exit': ").lower()

        if player_choice == 'exit':
            print("Thanks for playing! Goodbye.")
            break
        
        # Check if player's input is valid
        if player_choice not in ['rock', 'paper', 'scissors']:
            print("Invalid input. Please choose either rock, paper, or scissors.")
            continue
        
        # Get the computer's choice
        computer_choice = get_computer_choice()
        print(f"Computer's choice: {computer_choice}")
        
        # Determine the winner
        result = determine_winner(player_choice, computer_choice)
        print(result)

# Run the game
if __name__ == "__main__":
    play_game()
