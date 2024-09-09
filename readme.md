# Slot Machine Game 

## Overview

This is a simple text-based slot machine game implemented in Python. The game allows the player to deposit money, place bets on a configurable number of lines, and spin the slot machine to potentially win prizes based on the symbols that appear. The player can continue spinning as long as they have a balance remaining and choose to play.

## Features

- **Deposit Functionality**: Players can deposit money to start playing.
- **Betting System**: Players can bet on 1 to 3 lines with adjustable bet amounts (within the defined limits).
- **Slot Machine Simulation**: A slot machine with 3 rows and 3 columns. The symbols are randomly chosen based on their predefined count.
- **Winning Calculation**: Winnings are calculated based on the matching symbols in the chosen lines.
- **Interactive Gameplay**: The game runs in a loop allowing the player to spin multiple times until they choose to quit or run out of balance.

## Game Mechanics

- **Symbols**: There are four symbols, each with a different occurrence frequency and payout value:
  - `A`: 2 occurrences, payout value of 5x
  - `B`: 4 occurrences, payout value of 4x
  - `C`: 6 occurrences, payout value of 3x
  - `D`: 8 occurrences, payout value of 2x

- **Slot Machine Setup**: 
  - The slot machine consists of 3 rows and 3 columns.
  - Each column is filled with randomly selected symbols based on their availability.
  - Each spin generates a new set of symbols across the columns.

- **Betting**:
  - Players can bet on 1 to 3 lines.
  - The minimum bet per line is $1, and the maximum bet per line is $100.
  - The total bet is calculated as the bet per line multiplied by the number of lines.

- **Winning Conditions**:
  - A player wins if all symbols in a selected line match across all columns.
  - The payout is calculated based on the symbol's value multiplied by the bet amount.
  - Winnings are added to the player's balance after each spin.

## Code Structure

1. **Constants**: 
   - `MAX_LINES`, `MAX_BET`, `MIN_BET`, `ROWS`, `COLS`
   - `symbol_count` and `symbol_value` dictionaries to manage the occurrence and value of symbols.

2. **Functions**:
   - `check_winnings(columns, lines, bet, values)`: Calculates the winnings based on the outcome of the spin.
   - `get_slot_machine_spin(rows, cols, symbols)`: Generates a random set of symbols for the slot machine.
   - `print_slot_machine(columns)`: Prints the slot machine's current state to the console.
   - `deposit()`: Allows the player to deposit money.
   - `get_number_of_lines()`: Gets the number of lines the player wants to bet on.
   - `get_bet()`: Gets the bet amount per line from the player.
   - `spin(balance)`: Handles the spinning logic, checks for sufficient balance, calculates winnings, and updates the player's balance.
   - `main()`: The main loop of the game where the player can repeatedly spin until they choose to quit.

## How to Play

1. **Run the Program**: Start the game by running the Python script.
2. **Deposit Money**: Enter the amount of money you want to deposit to start playing.
3. **Place Bets**: Choose the number of lines to bet on and the amount to bet per line.
4. **Spin the Slot Machine**: Watch the slot machine spin and see if you win!
5. **Repeat or Quit**: Continue spinning as long as you have money left, or press `q` to quit the game.

## Requirements

- Python 3.x
- No external libraries are required; the game runs using Python's standard library.

## Customization

- **Adjust Symbol Frequency and Values**: Modify the `symbol_count` and `symbol_value` dictionaries to change the frequency and payouts of symbols.
- **Change Slot Machine Dimensions**: Adjust the `ROWS` and `COLS` constants to create different slot machine configurations.
- **Betting Limits**: Modify `MAX_BET` and `MIN_BET` to adjust the betting range.

## Example Gameplay

1. Deposit $100.
2. Bet $5 on 3 lines.
3. Spin the slot machine.
4. If you win, the winnings are added to your balance. If you lose, your bet is subtracted from your balance.
5. Continue playing until you decide to quit or run out of money.

## License

This code is open-source and can be used and modified freely. Attribution to the original author is appreciated if redistributed.

Enjoy playing the slot machine game! 🎰