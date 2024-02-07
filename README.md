# Approximating Pi
The area of a circle is pi times the square of the radius. If the circle's radius is 1, the area is equal to pi. This is called a unit circle. So, by approximating the area of a unit circle, we can find the value of pi.
# Quadtree-Sector Algorithm
This algorithm is a proof of concept, and can be easily made more efficient using parallel code. When dividing a circle using a quadtree, there are 8 copies created along lines of symmetry, at 0º, 45º, 90º and 135º. So, the algorithm only calculates the area of a circular sector with angle 45º. Then, it multiplies the value by 8 at the end.<br><br>At diagonals, the bottom right node is not created, because they are always outside the sector, and this reduces the amount of calculations.
# Efficiency
This algorithm is a more efficent version of creating a grid and checking if each cell is inside the circle. However the algorithm is still extremely slow, with a time efficiency of O(2^n).
