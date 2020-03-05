Write a program to score a game of Ten-Pin Bowling.<br>

This online app can help you: http://www.bowlinggenius.com/

**Input**: string (described below) representing a bowling game<br>
**Ouput**: integer score<br>
# The scoring rules
Each game, or "line" of bowling, includes ten turns, or "frames" for the bowler.<br>
<br>
In each frame, the bowler gets up to two tries to knock down all ten pins.<br>
<br>
If the first ball in a frame knocks down all ten pins, this is called a "strike". The frame is over. The score 
for the frame is ten plus the total of the pins knocked down in the next two balls.<br>
<br>
If the second ball in a frame knocks down all ten pins, this is called a "spare". The frame is over. The score 
for the frame is ten plus the number of pins knocked down in the next ball.<br>
<br>
If, after both balls, there is still at least one of the ten pins standing the score for that frame is simply the total number of pins knocked down in those two balls.<br>
<br>
If you get a spare in the last (10th) frame you get one more bonus ball. If you get a strike in the last (10th) frame you get two more bonus balls. These bonus throws are taken as part of the same turn. If a bonus ball knocks down all the pins, the process does not repeat. The bonus balls are only used to calculate the score of the final frame.<br>
<br>
The game score is the total of all frame scores.
# Symbol meanings
* `X` indicates a strike
* `/` indicates a spare
* `-` indicates a miss
* `|` indicates a frame boundary
* The characters after the `||` indicate bonus balls

# Examples
`X|X|X|X|X|X|X|X|X|X||XX`<br>
Ten strikes on the first ball of all ten frames.<br>
Two bonus balls, both strikes.<br>
Score for each frame == 10 + score for next two<br> 
balls == 10 + 10 + 10 == 30<br>
Total score == 10 frames x 30 == 300<br>
<br>
`9-|9-|9-|9-|9-|9-|9-|9-|9-|9-||`<br>
Nine pins hit on the first ball of all ten frames.<br>
Second ball of each frame misses last remaining pin.<br>
No bonus balls.<br>
Score for each frame == 9<br>
Total score == 10 frames x 9 == 90<br>
<br>
`5/|5/|5/|5/|5/|5/|5/|5/|5/|5/||5`<br>
Five pins on the first ball of all ten frames.<br>
Second ball of each frame hits all five remaining pins, a spare.<br>
One bonus ball, hits five pins.<br>
Score for each frame == 10 + score for next one<br>
ball == 10 + 5 == 15<br>
Total score == 10 frames x 15 == 150<br>
<br>
`X|7/|9-|X|-8|8/|-6|X|X|X||81`<br>
Total score == 167<br>

