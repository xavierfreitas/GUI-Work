# HW5: Shortened Scrabble Game

## Contact
Name: Xavier Freitas
Email: Xavier_Freitas@student.uml

##### Working Features #####
# Tile Generation and Draggability:
Random tiles are generated based on the distribution of Scrabble tiles in the "ScrabbleTiles" associative array.
All tiles are made draggable, and upon being generated they get unique IDs and can be dragged onto the board or returned to the tile holder.

# Tile Dropping on Board:
Tiles can be dropped onto the board, and the board-cells accept only valid tiles. The correct placement behavior is handled when a tile is dropped onto a new cell. If a tile is dropped onto a cell that is not a valid placement spot, it will bounce back to either the rack or the board-cell it was previously in.
If a tile is replaced in a cell, the previous tile is returned to the tile holder.

# Submit Button for Word Validation and Scoring:
The user can submit a word formed on the board.
The score for the word is calculated based on the tiles' values, with additional scoring rules for the double letter/word tiles. There is also a added gap check function (mentioned bellow).
# Extra Credit:
Before being submitted, the word is validated against a dictionary loaded from an external file (https://xavierfreitas.github.io/hw5/dict/words.txt).

# Alert box:
Working alert box that notifies the user if there is an issue once they try to submit a word.
Will display success message on successful word submission.
Box goes away as soon as a tile is moved again.

# Reset Button:
Clicking the reset button clears the board and resets the score to zero.
New tiles are generated for the player, the original tile distribution values are restored, and the tiles on the board are cleared.

##### Partially Working Features #####
# Gap Check Between Tiles:
The gap check function correctly identifies if there are any gaps between tiles placed on the board, but the behavior may be impacted by the current implementation of the tile placement. The gap detection logic needs a little more work (e.g., multiple consecutive gaps due to the way replacing a tile works).