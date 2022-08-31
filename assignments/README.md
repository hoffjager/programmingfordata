# programming-for-data-analysis-assignment
Programming for Data Analysis Assignment @ GMIT 2021

This README outlines the Python library, numpy.random, and provides information on numerous topics, such as:
#1.	The overall purpose of the library.
#2.	The use of the “Simple random data” and “Permutations” functions.
#3.	The use and purpose of at least five “Distributions” functions.
#4.	The use of seeds in generating pseudorandom numbers.

#1. Purpose of numpy.random library:
To begin, what is a random number? In computing, programs are a defined set of instructions that a computer carries out. You would expect that programmers have created an algorithm that can generate a random number. Can this be known as truly random, seeing as the algorithm was established and programmed by humans?
If there is an algorithm that can generate a random number, then it can be predicted, therefore it is not truly random. Random numbers that are generated through such an algorithm are labelled as pseudo-random. A pseudo-random number is a number that is almost random, but is not truly random.
Pseudo-random numbers are actually predetermined, as computers are deterministic, this is an issue when working with computers to simulate randomness.
Computers are designed to be deterministic and behave as such, if a computer is given a certain input, it will precisely follow those instructions and produces an output. If you later give the computer the same input, it will always produce the same output. Therefore, the behavior of computers isn't random.

Can we make truly random numbers? Yes we can.
In order to generate a truly random number on a computer, we would need to get the random data from outside sources, such as our keystrokes, our mouse movements, our data stored on a network, etc.
We need truly random numbers, which are used in the digital gambling industry with slot machines, roulette wheels, various card games, etc.
Random number generation (RNG) is a feature also used in video gaming, for example in the popular role-playing game (RPG) Pokémon, when there are approximately 5 different Pokémon in a certain wild area on the map, the game is coded in a manner where the rarest Pokémon does not show up very often, whereas more common Pokémon would always pop up in the wild.
Truly random numbers are also used in the matter of user online security, with encryption keys that are randomly generated to serve as login passwords.

There are many programming languages that can be used to generate random numbers, such as Python (numpy, numbers & Python). Numpy’s random number functions (numpy.random) produce pseudo-random numbers using a combination of a BitGenerator and a Generator.
BitGenerators are objects which generate random numbers that are filled with sequences of either 32 or 64 random bits.
Generators are objects that transform the above sequences of bits into sequences of numbers, that then follow a defined probability distribution in the numpy.random library.

We will select and discuss the most important libraries and modules in Python that help users to generate random data and are the most useful.

#2.	Use of random & permutations:
To use the random module in Python's numpy library, we must import it as follows: from numpy import random.
The permutation() function takes a single declared variable as input, returning an array of randomly assorted values, as shown in the corresponding Jupyter notebook.

#3. Use and purpose of five distributions functions:
Distribution #1: randint()
The randint() function takes in a minimum integer value as our starting parameter, and a maximum integer value as our final parameter.
The function will then print a single random number within the range of both parameters, or even print one of the chosen parameters.
randint() is also capable of printing an array of random numbers. To print an array, we establish minimum and maximum values like before, only in this instance, an internal bracket with two integers will be set up:
(a) the number of instances a random integer is output, and also:
(b) the number of random integers per instance.
The numbers are not truly random, they are completely determined by the algorithm, making these pseudo-random generated numbers. 

Distribution #2: choice()
This function is generally used when a random value is required from a set list of integers.
The choice function can prove useful when it comes to raffles, where tickets are purchased and the corresponding ticket numbers are then specified in an array for the choice() function to randomly choose a ticket number from the array in order to declare a winner.

Distribution #3: shuffle()
This function is used to shuffle the values within an array.
The shuffle() function is similar to the choice() function, except in this instance, the integers inside the array are shuffled instead of a single integer being displayed from the array.
This function would commonly be used in shuffling a music album's tracks, where the album's ordered list of tracks can be shuffled when the listener wishes to play an album on shuffle mode.

Distribution #4: randn()
This function is used to create random arrays where the random float numbers generated are structured from normal distribution.
The standard normal distribution is known as a continuous probability distribution, which has a Mu (mean) of 0, and a Sigma (standard deviation) of 1.
If no argument value is provided within the function, then a single float value is returned, otherwise, the function returns an array of a size that can be set by the user.

Distribution #5: uniform()
This function is used to create random arrays where the numbers generated are drawn from a uniform distribution, as opposed to the normal distribution as seen in the randn() function above.
The uniform distribution is known as a probability distribution, known as a function that returns the probability of various outcomes.
Within the uniform() function, three integers are placed, the low and high values as a range, in addition to the size of the array.
Within this range, the probability of drawing a particular number is given by the formula: P(x) = 1/high-low, whereas the probability of drawing a number outside of the low-high range is 0.

#4.	The use of seeds in generating pseudo-random numbers:
NumPy contains a function within its random module which is known as seed(). The numpy.random.seed function provides the input (seed) to the algorithm that will generate pseudo-random numbers from the BitGenerator.
The psuedo-random numbers that are generated appear to be random, but low and high values must be set by the user for the computer to read the range and the size of the output.
As shown in the Jupyter notebook, we enter the seed function, followed by the randint() function, and upon running this code multiple times, the same value is returned each time, the same input will produce the same output.
If you provide the same seed, you get the same output. If you change the seed, you then get a different output. A different output is achieved if the value of the seed is modified.
Psuedo-random generators are used to produce random numbers to give the impression of randomness, but the output is determined by the user's input.
numpy.random.seed() works best when incorporated with other functions from the numpy.random namespace, such as randint(), choice(), randn(), etc for random sampling. The function works best if we wish to get repeatable results for the purpose of testing and sharing code.

References:
https://numpy.org/doc/stable/reference/random/index.html
https://www.w3schools.com/python/numpy/numpy_random.asp
https://pythonguides.com/python-numpy-random/
https://towardsdatascience.com/most-important-random-number-python-modules-to-keep-always-by-your-side-ef99a4ae624b
https://www.pythonpool.com/numpy-random-permutation/
https://www.geeksforgeeks.org/random-numbers-in-python/
https://www.datacamp.com/community/tutorials/numpy-random
https://www.sharpsightlabs.com/blog/np-random-randn-explained/
https://www.sharpsightlabs.com/blog/numpy-random-seed/