In the *first notebook*, number_list_analysis.ipynb, we manipulate in various ways a list of 100 natural numbers that I pulled off the internet. There is no significance to the numbers, I just wanted to test out various tricks, such as 

1. counting their multiplicities 
2. using modular arithmetic to separate evens from odds, and list those divisible by 3, or divisible by 5
3. sorting them by hand
4. treating them as a sample and finding summary statistics (min, max, mean, 1st-3rd quartiles, and standard deviation)

We attempt point 4 in two different ways:  directly using NumPy + formatting the printout, and using the .describe() function in Pandas.  These were exercises in Python for me, using elementary number theory as the matter to be manipulated.  Perhaps they will come in handy later.

The *second notebook*, primes.ipynb, concerns the problem of finding all prime and coprime numbers less than a given positive $n\in\mathbb{N}$ of your choosing.  
* For example, if $n=5$, there are three primes $p = 2, 3, 5$ in the interval $[2,5]$, and four numbers $m = 1, 2, 3, 4$ coprime to $n=5$ in the intervsl $[1,5]$.
* If $n=10$, there are four primes, $p=2, 3, 5, 7$ in the interval $[2,10]$, and four numbers $m = 1, 3, 7, 9$ coprime to $n=10$ in the intervsl $[1,10]$ 

The number $k$ of integers $m\in [1,n]$ coprime to $n$, which satisfy by definition $\gcd(m,n)=1$, is the value of **Euler's $\varphi$ function**,

$$
\varphi(n)\ =\ k\ \stackrel{\text{def}}{=}\ |\{m\in [1,n]:\gcd(m,n)=1\}|
$$

There is a well known relationship between the prime factorization of $n$,

$$
n = p_1^{k_1}*p_2^{k_2}\cdots p_r^{k_r}
$$

and the Euler $\varphi$ function, namely,

$$
\varphi (n)=p_{1}^{k_{1}-1}(p_{1}{-}1)\,p_{2}^{k_{2}-1}(p_{2}{-}1)\cdots p_{r}^{k_{r}-1}(p_{r}{-}1)
$$

In the case of $n=10$, for example, the factorization $10 = 2^1*5^1$ implies that $\varphi(10)=2^{1-1}(2-1)\cdot 5^{1-1}*(5-1)=4$.

Below, we write Python functions to compute each of the lists, primes and coprimes, less than a given $n$.  Then we compare with Euler's $\varphi$ function by first giving the prime factorization of the chosen $n$.