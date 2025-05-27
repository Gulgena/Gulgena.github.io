```mermaid
#  Random Guessing Game Flowchart                                                                                                                                 
flowchart TD                                                                                                                 
    Start([Start])
    Init["Generate random number (e.g., 1-100)"]
    GetGuess[/Prompt user for a guess/]
    Validate{"Is input a valid number?"}
    ErrorMsg["Show error message"]
    Compare{"Is guess equal to target?"}
    TooLow["Display 'Too low'"]
    TooHigh["Display 'Too high'"]
    Congrats["Display 'Correct! You guessed it!'"]
    End([End])

    Start --> Init --> GetGuess --> Validate
    Validate -- No --> ErrorMsg --> GetGuess
    Validate -- Yes --> Compare
    Compare -- Yes --> Congrats --> End
    Compare -- No --> Direction{"Guess > or < target?"}
    Direction -- "Too High" --> TooHigh --> GetGuess
    Direction -- "Too Low" --> TooLow --> GetGuess


```markdown
##  Description of Each Step

1. **Start** – Beginning of the program.
2. **Generate Random Number** – Computer selects a number between 1 and 100.
3. **Ask for User Guess** – User is asked to enter a number.
4. **Validate Input** – Check if the input is a number:
   - If not, show error message and ask again.
5. **Compare Guess to Target**:
   - If correct: show "Correct!" and end the game.
   - If not:
     - If guess > target, show "Too High".
     - If guess < target, show "Too Low".
6. **Repeat** – Keep asking until the guess is correct.
7. **End** – Program finishes when the correct number is guessed.
