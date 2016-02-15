# Question 1

### Problem:
Write a function to determine whether a given number is prime.

### Solution:

I have provided a python file prime.py that includes:

* the best prime number test I could come up with (in a reasonable amount of time)
* the ability to use caching to improve the speed
* prime number generator based on the Sieve of Eratosthenes
* tests that compare my implementation to lists of known primes found on the web

Here is a screencast of the prime.py in action:

![prime.py](https://raw.githubusercontent.com/jrhea/prime-numbers/master/images/prime_loops.gif)


**proof of algorithm's optimizations:**

All integers can be written in the form:

            6k+i where i = 0,1,2,3,4,5
    
_Note: We can show that 5 could be replaced by -1 by substituting k' with k+1_

            6k'-1 = 6k+5 when k'=k+1

All odd integers can be written in the form:

            6k+i where i = 1,3,5

_Note: We can remove 3 from i bc 6k+3 only generates a single prime (3) when k=0_

6k+3 is composite for all other values of k:

           6k % 3 = 0 -> (6k+3) % 3 = 0

Therefore, set containing all odd primes greater than 3 can be written as:

            6k+i where i = 1,5  

**Now I have proven that I can speed up the prime test by:**
* incrementing i by 6 each pass of the loop 
* only checking if n mod i or n mod i+2 equals 0

_Note: i is equivalent to 6k+5 & i+2 is equivalent to 6k+1_


**browse repository:**

https://github.com/jrhea/prime-numbers

**clone source:**

```
git clone https://github.com/jrhea/prime-numbers.git
```

# Question 2

### Problem:
Write an application for browsing git commit history.

### Solution:



**browse repository:**

https://github.com/jrhea/gitViewer

**clone source:**

```
git clone https://github.com/jrhea/gitViewer.git
```

**documentation**
http://jrhea.github.io/gitViewer

