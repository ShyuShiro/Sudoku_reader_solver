# Sudoku_reader_solver
Sudoku can easily be solved. 

But what about reading a sudoku grid, processing the numbers seen, and then solving? 

Real-world application for CV2 and EMNIST dataset.

# Goal
1) Utilize opencv2 to read an image (ideally webcam, but I don't own any physical sudoku books) <br>
2) Train a deep learning model to interpret numbers <br>
3) Solve a sudoku grid via interpreting the numbers on the grid (as opposed to hard coding in the numbers)

# Process:
1) The Sudoku Grid
> a) Need to detect the grid which may not be centered or straight <br>
> b) Straighten the grid layout <br>
> c) Split the grid from 9x9 to 81 images <br>
> d) Feed those images into the CNN model to be interpretted 

2) Deep Learning model
> a) MNIST dataset is great, but most sudoku grids are filled with digitized numbers, not handwritten numbers. <br>
> b) EMNIST dataset (https://www.nist.gov/itl/products-and-services/emnist-dataset) contains 1016 images for digits [0,9] as well as characters [Aa-zZ] -- I'll only train the model utilizing the digits <br>
> c) Save the model once trained & load it as a method of detecting the numbers generated from (1c)

3) Solving the grid
> a) Can be solved in a number of ways --- Brute force (backtracking), as an optimization problem, or more sophisticated algorithms (which i can't seem to find at the time of typing this readme doc). <br>
> I'll likely approach this as an optimization problem
