In this notebook, we manipulate in various ways a list of 100 natural numbers that I pulled off the internet. There is no significance to the numbers, I just wanted to test out various tricks, such as 

1. counting their multiplicities 
2. using modular arithmetic to separate evens from odds, and list those divisible by 3, or divisible by 5
3. sorting them by hand
4. treating them as a sample and finding summary statistics (min, max, mean, 1st-3rd quartiles, and standard deviation)

We attempt point 4 in two different ways:  directly using NumPy + formatting the printout, and using the .describe() function in Pandas.
