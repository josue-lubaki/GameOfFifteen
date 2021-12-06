## Game of Fifteen

### Demo
[![Everything Is AWESOME](https://videoapi-muybridge.vimeocdn.com/animated-thumbnails/image/050d41df-b859-4641-a4ce-af4310417a11.gif?ClientID=vimeo-core-prod&Date=1638774899&Signature=1a417625068f27259ce9ec5a22f8c2accf474a54)](https://youtu.be/1H8Bw0hgQpo "15-Puzzle")

The board for the game of Fifteen is filled randomly with numbers from 1 to 15 and
one empty space. You can move the neighboring value to the empty space.
The goal is to get the sorted sequence from 1 to 15.

You can check the Game of Fifteen online
[here](http://migo.sixbit.org/puzzles/fifteen/).
Note that in the implementation for this assignment, the values are moved
by arrows rather than mouse clicks.

* Game of Fifteen is solvable only if the initial permutation of numbers
  is [even](https://en.wikipedia.org/wiki/Parity_of_a_permutation).
  First, implement the function `isEven` declared in
  ```GameOfFifteenHelper.kt``` <br>
  checking whether a permutation is even or odd.
  Source: ```GameOfFifteenHelper.kt``` <br>;
  tests:  ```TestGameOfFifteenHelper.kt``` <br>.

You can use the following algorithm to check the given permutation.
Let `P` is a permutation function on a range of numbers `1..n`.
For a pair `(i, j)` of elements such that `i < j` , if `P(i) > P(j)`,
then the permutation is said to invert the order of `(i, j)`.
The number of such inverted pairs is the _parity_ of the permutation.
If permutation inverts even number of such pairs, it is an even permutation; else
it is an odd permutation.

* Use the `isEven` function to produce only solvable permutations as initial
  permutations.
  Source: ```GameOfFifteenInitializer.kt``` <br>;
  tests: ```TestGameOfFifteenInitializer.kt```.<br>

* Implement the `GameOfFifteen` class from scratch describing the game process.
  It should implement the `Game` interface and make use of `initializer` argument.
  Note that this argument is used in tests to provide a different initial permutation.
  Source: ```GameOfFifteen.kt```; <br>
  tests: ```TestGameOfFifteen.kt.```
