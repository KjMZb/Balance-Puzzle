# Balance-Puzzle
This is a balance puzzle solver written in Python. In a balance puzzle, there is a system of beams and weights with some weights missing. The formula for torque ( force * distance from pivot) is used to solve for the missing weights. For example:
X * -10 = 10 * 2
X = 20 / |-10|
X = 2
Note, however, that there can be more than two weights hanging from a beam. In that case:
X * -10 = ( 10 * 2) + ( 3 * 8 )
X * -10 = 20 + 24
X * -10 = 44
X = 44 / |-10|
X = 4.4

The text file, balance, is the puzzle itself where each line represents a beam. Each line is in the following format:
<Name of beam>  { A set of objects hanging from the beam, formatted as: <distance from attachment> <name of member/weight> }
Missing weights are represented by -1.

The three Python files are needed to run the puzzle solver. Beam.py is an object that has other objects ( weights or other beams ) hanging from it. Each beam also has its own weight, given by the sum of the weights hanging from it. Weight.py is a weight with no special properties other than a weight value.

balances.py solves the balancing puzzle. Beginning at the bottom, it uses the torque formula to find the missing weights. In  addition, it makes sure that, regardless of the size of the puzzle, there is at least 10 pixels between beams on the same level. 
