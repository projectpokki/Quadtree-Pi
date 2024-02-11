# Approximating Pi
The area of a circle is pi times the square of the radius. If the circle's radius is 1, the area is equal to pi. This is called a unit circle. So, by approximating the area of a unit circle, we can find the value of pi.
# Quadtree-Sector Algorithm
This algorithm is a proof of concept, and can be easily made more efficient using parallel code. When dividing a circle using a quadtree, there are 8 copies created along lines of symmetry, at 0º, 45º, 90º and 135º. So, the algorithm only calculates the area of a circular sector with angle 45º. Then, it multiplies the value by 8 at the end. At diagonals, the bottom right node is not created, because they are always outside the sector. This leads to only needing 1/8 of the calculations per iteration.
# Efficiency
This algorithm is a more efficent version of creating a grid and checking if each cell is inside the circle. It has a time efficiency of O(2^n). By iteration 20 (starting from 0), this algorithm calculates checks if 4.65\*10^6 (4 million and 650 thousand) nodes are in the circle, yet only approximates pi to 4 decimal places (3.1415833...). While this is very slow, it is a significant improvement from checking each cell of a grid to this accuracy, which would need to check if (2^20)^2 or 1.01\*10^12 (1 trillion and 10 billion) cells are in the circle.
