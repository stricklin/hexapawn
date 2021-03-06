This is a program that uses adverserial search to solve the game Hexapawn.
It takes game state input from stdin or a file name as an argument.
To run it with input from stdin:
python3 Hexapawn.py < test1-out.txt

To run it with input from an argument:
python3 Hexapawn.py test1-out.txt

The input must represent black pawns as 'p', white pawns as 'P' and spaces as '.'
Whos turn it is is represented by a 'W' or a 'B' in the first row.
The 3x3 starting board as an example:
W
ppp
...
PPP

I chose to represent the state of the board as a numpy array to make access faster.
I keep both a board and a piece list because getting a list of pieces everytime
it's needed is much more expensive than maintaining the piece list. Keeping a board
representation helps minimally because it cuts out scanning the oppositions piece 
list every time a capture move is checked, but mostly it makes the code more readable
because humans think about the game in terms of a board.

I didn't add any move sorting optimization because it was already fast enough to pass
all of the test boards provided.

This was my first program where I used TDD and while getting that set up took time
time, I think that the debugging process took much much less time. I'm going to 
be using TDD for probably all of my programs from here on out.
