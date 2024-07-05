
Algorithm for Tic-Tac-Toe Game
1.Start

2.Create a class Xand that extends JFrame and implements ActionListener.
  Define a JButton array of size 9 to represent the Tic-Tac-Toe grid.
  Initialize a boolean variable isX to true to track the current player's turn (true for X, false for O).
   Constructor (Xand):

3. Set the title of the frame to "Tic-Tac-Toe".
 Set the size of the frame to 400x400 pixels.
 Set the default close operation to EXIT_ON_CLOSE.
 Set the layout of the frame to GridLayout with 3 rows and 3 columns.
 Initialize each button in the buttons array:
 Set the font to Arial, plain, and size 60.
 Set focus painted to false.
 Add the current instance as the action listener for each button.
 Add the button to the frame.
 Make the frame visible.
 Action Handling (actionPerformed method):

4. Determine which button was clicked.
 If the button's text is empty:
 Set the button's text to "X" if isX is true, otherwise set it to "O".
 Disable the button.
 Toggle the value of isX.
 Call checkForWinner to determine if there is a winner or a draw.
 Check for Winner (checkForWinner method):

5. Create a 3x3 string array board to represent the current state of the grid.
 Populate the board array with the text from each button.
 Check rows, columns, and diagonals for a winning line:
 For each row i, check if board[i][0], board[i][1], and board[i][2] are the same and not empty.
 For each column i, check if board[0][i], board[1][i], and board[2][i] are the same and not empty.
 Check the two diagonals.
 If a winning line is found, call announceWinner with the winning player's symbol.
 If no winner is found, check for a draw:
 If all buttons are filled, display a draw message and call resetBoard.
 Check Line (checkLine method):

6. Return true if all three input strings are the same and not empty.
  Announce Winner (announceWinner method):

7. Display a message indicating which player has won.
 Call resetBoard to reset the game.
 Reset Board (resetBoard method):

8. Clear the text of each button and enable them.
 Set isX to true to start a new game with X's turn.
 Main Method:

9.In the Xand class, define the main method:
Use SwingUtilities.invokeLater to ensure the GUI is created on the Event Dispatch Thread (EDT).
Create a new instance of Xand.
In the Main class, call the main method of the Xand class to start the game.
