import random
print("Python 🐍 Slot Machine 🎰",
      "\n", "************************")

# FUNCTION
def spin_row():
    symbols = ['🍒', '🍉', '🍋', '🔔', '⭐️'] # LIST WITH STRINGS


# LIST COMPREHENSION:
    return [random.choice(symbols)for _ in range(3)]

# FUNCTION
def print_row(row):
    print("------------")
    print(" | ".join(row)) 
    print("------------")

# FUNCTION
def get_payout(row, bet):# PASSING 2 ARGUMENTS
    if row[0] == row[1] == row[2]:
        if row[0] == '🍒':
            return bet * 5
        elif row[0] == '🍉':
            return bet * 7
        elif row[0] == '🍋':
            return bet * 10
        elif row[0] == '🔔':
            return bet * 15
        elif row[0] == '⭐️':
            return bet * 20
    return 0


# FUNCTION
def main():
    balance = 100  # VARIABLE IS BALANCE


    print("Welcome to Python Slots!",
          "\n", "Symbols: 🍒 🍉 🍋 🔔 ⭐️",
          "\n", "*************************")

    while balance > 0:
        print(f"Current balance: ${balance}") # FSTRING

        bet = input("Place your bet amount: ") # VARIABLE IS BET
        if not bet.isdigit():
            print("\033[38;5;221m", "Please enter a valid number!", "\033[0m")
            continue #WILL SKIP THE CONTINUE ITERATION OF THE LOOP AND WILL START FROM THE BEGINNING

        bet = int(bet) # TYPECASTING

        if bet > balance:
            print("\033[1;31m", "Insufficient funds ☹️", "\033[0m")
            continue

        if bet <= 0:
            print("\033[38;5;225m", "Bet must be greater than 0", "\033[0m")
            continue

        balance -= bet

        row = spin_row() # CALL SPIN_ROW FUNCTION TO RETURN A LIST
        print("Spinning....\n")
        print_row(row)

        payout = get_payout(row, bet)

        if payout > 0:
            print(f"You won ${payout}!!! 🤩")
        else:
            print("Sorry you lost this round!! 😭")

        balance += payout

        play_again = input("Do you want to spin again? (Y/N):").upper()

        if play_again != 'Y':
            break
    print(f"Game Over! Your final balance is ${balance}")

if __name__ == '__main__':
    main()

