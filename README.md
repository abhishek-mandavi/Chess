# Chess
#Frontend
Socket.io Initialization:
Establish WebSocket connection to the server using Socket.io (const socket = io();).

Chess Game Initialization:
Create an instance of the Chess class from the chess.js library to manage the game logic (const chess = new Chess();).

DOM Elements:
Select the HTML element with the ID "chessboard" to render the chessboard (const boardElement = document.querySelector("#chessboard");).

Drag and Drop:
Implement drag and drop functionality for moving chess pieces on the board.
Pieces are draggable only if it's the player's turn.
Event listeners for drag start, drag end, drag over, and drop events are attached to handle drag and drop interactions.

Rendering the Board:
Generate the HTML representation of the chessboard based on the current game state.
Iterate over the board array and create square elements for each cell.
Create piece elements for occupied squares and append them to square elements.
Flip the board for the black player's view.

Handling Moves:
Handle player moves when dragging and dropping pieces.
Construct a move object containing the source and target squares in algebraic notation.
Emit a "move" event to the server via Socket.io.

Unicode Chess Pieces:
Return Unicode characters representing chess pieces based on their type.

Socket.io Event Handlers:
Listen for various events from the server such as player role assignment, spectator role assignment, board state updates, and opponent moves.
Update the local game state and render the board accordingly when receiving events.

Initial Rendering:
Call the renderBoard function initially to render the initial state of the chessboard.
 
