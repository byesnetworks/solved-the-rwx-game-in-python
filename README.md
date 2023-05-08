Download Link: https://assignmentchef.com/product/solved-the-rwx-game-in-python
<br>
The RWX game is a game where the idea is to guess the same random string that the program has generated.

For each game, the program should generate a random three character target string (using the characters in string digits ensuring that each character in the target string is unique – e.g. “1 12” is not a valid target string because “1” is repeated). The user then tries to guess the target, and receives a hint after each incorrect guess indicating how close their guess is to the target string.

<ul>

 <li>A “W” indicates that all of the characters in the guess are wrong.</li>

 <li>One or more “X”s indicates that they have a correct character, but in an incorrect position</li>

 <li>One or more “R”s indicates they have a correct character in the right position</li>

</ul>

The characters in the hint are presented in alphabetic order. The following table gives an example of the game’s output for a user guess. Assume the target string is “123”.




* This hint would never be displayed in the game, because the game ends after a correct guess, before this hint would be presented.

Scoring for the game depends on the number of guesses required for the user to guess the target string. If the user guesses the right answer on their first guess, they receive 10,000 points. Each subsequent guess reduces the possible score by of its current value. For example, if the user guesses the right answer on their second guess, the user would receive 9,000 points (10% of 10,000). On their third guess, the user would receive 8,100

(10% of 9,000), and so on.

The game ends either when either:

<ul>

 <li>The user guesses the target string, in which case they are told the number of guesses it took them to guess the target string and the number of points they were awarded (displayed to two decimal places);</li>

 <li>or when the possible number of points drops below 1,000, in which case they are told that the game is over, the number of guesses they have made, and the correct answer.</li>

</ul>

When the game completes, the user will be offered the opportunity to start a new game. If the user chooses to start a new game, the target string, the number of guesses, and the points must all be reset.

Notes

You must implement and use a function named get hint (guess, target) that takes the current guess and target string as parameters. It will return the hint that gets displayed to the user after an incorrect guess. The structure of the rest of your assignment is left to you, though it is suggested that other functions would be useful.

Your program should perform input validation. If the user enters anything other than three digits when asked to guess, they should be informed of the error and asked to input the guess again. You might find str.is digit () useful. When asked to play again, the user should be repeatedly asked until they enter “Y” or “y” (indicating they do want to play again) or “N” or “n” (indicating the program should exit).