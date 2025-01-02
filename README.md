# tic__.tac__.toe

The code implements a simple **two-player Tic Tac Toe game** in Python. It uses a 3x3 grid (`board`) and alternates between two players, 'X' and 'O', until a winner is determined or the board is full (a draw)......

---

### **Core Concepts and Functions**

1. **`board` Initialization**
   - The `board` is represented as a 2D list of lists, with each cell initialized to a space `' '` to indicate it's empty.

2. **Player Markers (`X` and `O`)**
   - The two players are represented by the characters `'X'` and `'O'`.

3. **`cell(mark)`**
   - This function is responsible for coloring the markers. `'X'` is displayed in **red**, and `'O'` in **green**, using the `termcolor` library for visual clarity.

4. **`print_board(board)`**
   - Displays the current state of the board with gridlines for visual representation.
   - Iterates through each row of the `board` and uses the `cell` function to display each marker in its respective color.

5. **`check_winner(board)`**
   - Checks if any player has won:
     - **Rows:** If all three cells in any row are the same and not empty, a win is detected.
     - **Columns:** Checks if all three cells in any column are the same and not empty.
     - **Diagonals:** Checks the two diagonals for three identical, non-empty markers.
   - Returns `True` if a winner is found; otherwise, `False`.

6. **`is_full(board)`**
   - Checks if the board is completely filled with no empty cells.
   - Returns `True` if the board is full; otherwise, `False`.

7. **`get_position(prompt)`**
   - Prompts the user to enter a valid row or column index (0-2).
   - Validates the input, ensuring it's an integer within the range [0, 2].
   - Keeps asking until a valid input is provided.

8. **`get_move(current_player)`**
   - Prompts the current player to choose a row and column to place their marker.
   - Ensures the chosen cell is empty before placing the marker.
   - If the cell is already occupied, it asks the player to choose again.

9. **`main()`**
   - The main game loop:
     - Alternates turns between players `'X'` and `'O'`.
     - Displays the board after every move.
     - Checks for a winner using `check_winner` or if the board is full using `is_full`.
     - Ends the game if a player wins or if the board is full (draw).
   - Uses a simple toggle mechanism (`current_player = O if current_player == X else X`) to switch players.

10. **Game Start**
    - The program starts execution with the `main()` function, which initializes and manages the game.

---

### **Execution Flow**

1. **Initialize Board**: The empty `board` is displayed.
2. **Player Input**:
   - Player `'X'` starts first.
   - Players take turns to choose a row and column to place their marker.
3. **Win/Draw Check**:
   - After every move, the game checks for a winner using `check_winner`.
   - If no winner is found, it checks if the board is full (`is_full`).
4. **End Game**:
   - If a winner is detected, a message announces the winning player.
   - If the board is full without a winner, the game declares a draw.
5. **Repeat**: The process continues until the game ends.
