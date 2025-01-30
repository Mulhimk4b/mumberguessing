# Random Guessing Game Flowchart

## **Overview**
This diagram represents the logic of a **random guessing game** where the computer selects a random number, and the player attempts to guess it. The game provides feedback on whether the guess is too high, too low, or correct.

## **Flowchart**

```mermaid
flowchart TD
    Start([Start Game]) -->|Generate Random Number| GenerateNumber
    GenerateNumber --> GetUserInput[/Get User Input/]
    GetUserInput -->|Check Input Validity| ValidateInput
    
    ValidateInput -->|Invalid (Not a Number)| GetUserInput
    ValidateInput -->|Valid| CheckGuess
    
    CheckGuess -->|Too High| TooHigh
    CheckGuess -->|Too Low| TooLow
    CheckGuess -->|Correct| CorrectGuess
    
    TooHigh --> GetUserInput
    TooLow --> GetUserInput
    
    CorrectGuess -->|Play Again?| PlayAgain{Play Again?}
    PlayAgain -->|Yes| GenerateNumber
    PlayAgain -->|No| End([End Game])
```

## **Explanation of the Flowchart**
1. **Start**: The game begins and a random number is generated.
2. **User Input**: The player enters a guess.
3. **Validation**:
   - If the input is **not a number**, the game prompts the player again.
   - If the input is a number, it is compared to the randomly generated number.
4. **Comparison**:
   - If the guess is **too high**, the player is notified and asked to guess again.
   - If the guess is **too low**, the player is notified and asked to guess again.
   - If the guess is **correct**, the player wins and is asked if they want to play again.
5. **Game End**:
   - If the player chooses to play again, a new random number is generated.
   - If not, the game ends.

## **How to Submit**
1. Copy this Markdown content into a new file named `Guessing.md` in your GitHub repository.
2. Commit and push the file.
3. Submit the **public GitHub link** for grading.
