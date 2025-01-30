flowchart TD
    Start([Start Game]) -->|Generate Random Number| GenerateNumber
    GenerateNumber --> GetUserInput[/Get User Input/]
    
    GetUserInput --> ValidateInput{Is Input a Number?}
    ValidateInput -- No --> GetUserInput
    ValidateInput -- Yes --> CheckGuess

    CheckGuess -->|Too High| TooHigh
    CheckGuess -->|Too Low| TooLow
    CheckGuess -->|Correct| CorrectGuess

    TooHigh --> GetUserInput
    TooLow --> GetUserInput

    CorrectGuess --> PlayAgain{Play Again?}
    PlayAgain -- Yes --> GenerateNumber
    PlayAgain -- No --> End([End Game])
