Number Guessing Game in C

Overview
    This is a robust, command-line implementation of the classic Number Guessing Game,
    written in C. It features two distinct game modes—Survival and Timer—each with four difficulty
    levels, and includes custom input validation for reliable operation.
FeaturesTwo Game Modes:
    Survival Mode:
        Guess the number within a fixed, limited number of attempts.Timer Mode: Race to guess the number
        before the time limit expires.Four Difficulty Settings: Increasing challenge based on the random
        number range and resource limits:
        | Difficulty | Range | Survival Attempts | Timer Limit (Seconds)|
        | Easy       | 1 - 40| 10                | 240                  |
        | Medium     |1 - 400| 8                 | 180                  |
        | Hard       |1- 4000| 6                 | 120                  |
        | Impossible |1-32767| 4                 | 60                   |
    Robust Input Validation: 
        Custom input functions (Check_input_int, Check_input_yn) prevent common issues
        like buffer overflow, non-numeric input, and incorrect character input (y/n), ensuring the game remains
        stable.
Installation and SetupPrerequisites
    You need a C compiler (such as GCC or Clang) installed on your operating system to compile and run the source code.CompilationSave the provided source code as
    main.c.Open your terminal or command prompt.Navigate to the directory where you saved the file.Compile
    the code using a command similar to this:Bashgcc -o guess_game main.c
    (This creates an executable file named guess_game.)Running the GameExecute the compiled program from your terminal:Bash./guess_game
     How to PlayThe game starts with the main menu, allowing you to choose your mode:    
        [1] Survival Mode.
        [2] Timer Mode.
        [3] Exit.
    Survival Mode Gameplay
        In this mode, you must guess the secret number using only the provided attempts.
        If your guess is wrong, the game will indicate if the actual number is HIGHER or LOW than your entry.
        Your score is calculated based on remaining attempts: 
        [Attempts Left] / [Starting Attempts].
    Timer Mode Gameplay
        In this mode, you must guess the secret number before the countdown reaches zero.
        If your guess is wrong, the game will indicate if the actual number is HIGH or LOW than your entry.
        If you win, the total Time Taken to guess the number is displayed.If you exceed the time limit, you lose.
Code StructureThe program is organized into functional units:
    Function NamePurposemain()
        Initializes the random seed (srand(time(NULL))) and manages the main menu and game loop flow.
    Survival_Mode()
        Presents the difficulty menu and sets up the random number and attempt count for Survival Mode games.
    Timer_Mode()
        Presents the difficulty menu and sets up the random number and time limit for Timer Mode games.
    Check_rand_numb()
        Core game logic for Survival Mode. 
        Handles user input, compares the guess to the random number, and manages the attempt counter.
    Check_rand_numb_timer()
        Core game logic for Timer Mode. 
        Handles user input, uses time() and difftime() to track elapsed time, and determines if the player ran out of time.
    Check_input_int()Validation: 
        Ensures the user enters a positive integer, handling non-numeric input and buffer overflow.
    Check_input_yn()Validation: 
        Ensures the user enters only 'y' or 'n' (case-insensitive), handling extraneous characters and buffer overflow.
Contribution & LicenseThis project is open-source. 
    Feel free to fork the repository, suggest improvements, or submit pull requests.
    LicenseThis project is licensed under the [MIT License] - see the LICENSE file for details.
Contact
  AmeerAbdullahM
