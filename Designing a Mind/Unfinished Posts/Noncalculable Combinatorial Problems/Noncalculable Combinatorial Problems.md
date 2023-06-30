[https://www.youtube.com/watch?v=bOXCLR3Wric&t=595s](https://www.youtube.com/watch?v=bOXCLR3Wric&t=595s)

- The problem presented comes from ************************102 Combinatorial Problems************************ by Titu Andresscu and Zuming Feng
- The problem being from Chapter 2 Problem number 10:
    - Find the number of subset of $\{1, 2, 3, ..., 2000\}$, the sum of whose elements is divisible by 5.

### Simplifying the problem

We’ll start by parsing the subsets of the set $A = \{1, 2, 3, 4, 5\}$, and group those subsets by their sums. Notice that the 8 sets on the far left’s sums are divisble by 5

![[screenshot.png]]

So now we will consider the polynomial

$$
p(x) = (1 + x^1)(1 + x^2)(1+x^3)(1+x^4)(1+x^5)
$$

This polynomial has an exponent equal to each value in our simplified set. Whenever we do expand it notice how the polynomial, generates out sets for us before it gets simplified down

![[screenshot 1.png]]

Now if we fully expand the polynomial 

$$
p(x) =x^{15}+x^{14}+x^{13}+2x^{12}+2x^{11}+3x^{10}+3x^9+3x^8+3x^7+3x^6+3x^5+2x^4+2x^3+x^2+x+1
$$

Expanding this polynomial interestingly enough groups the subsets generated above automatically. If we were to look at the term $3x^{10}$ the number of subsets that sums are equal to 10, there are 3, which is the coefficient of the given term. But why does this happen?

$$
(1 + x^1)(1 + x^2)(1+x^3)(1+x^4)(1+x^5)
$$

Expanding this polynomial comes down to making 5 binary choices, which term from each parenthetical do you use. Which mirrors the process of building out the subset list from above. There we see 5 numbers where we make 5 binary choices, whether to add the number to the subset, or to not add it. 

That is to say, to answer the simplified version of this question, we can simply look at the terms of the expanded polynomial and where the exponent is divisible by 10, we add the coefficient to the count of valid subsets. Those terms are $1$ (the exponent is 0, which is divisible by 5 and the coefficient is 1), $3x^5$, $3x^{10}$, and $x^{15}$. **Giving us an answer of 8 sets** 

---

### Back to the actual problem

From our example up there, we can see that we can glean a lot of important details from a generating functions based upon the parameters. That generating function being:

$$
p(x) = (1+x^1)(1+x^2)(1+x^3)...(1+x^{2000})
$$

So how do we evaluate this function to get the output we want (subsets whose sums is divisible by 5). 

$$
p(x) = \sum_{n=0}^{N} c_nx^n=c_0+c_1x+c_2x^2+c_3x^3+c_4x^4+...

$$

First lets evaluate $p(0)$ which will equal 1 since all that we get $c_0$ which is equal to 1. Below we show that all $x$ equal 0 so all we are left with is our first coefficient $c_1$ . Which if we use our logic learned from above will generate an empty set since, there is 1 set with a sum of 0 and 0 elements. All we get from this is that there is one subset with nothing in it (our singular empty set)

$$
p(x) = \sum_{n=0}^{N} c_nx^n=c_0+c_1(0)+c_2(0)^2+...
$$

Now lets try $f(1)$

$$
p(x) = \sum_{n=0}^{N} c_nx^n=c_0+c_1(1)^1+c_2(1)^2+...
$$

$$
p(x) = 2^{2000}
$$

But what does *****this***** tell us? This will deduce the sums of all the coefficients, which we can also find by applying set logic to the original prompt. Even though this evaluation doesn’t tell us anything new either, we are getting closer to what will actually help

But now we try $f(-1)$. Do note that even though this evaluates to 0, it tell us a lot about how we can use this function to solve our problem

$$
p(x) = \sum_{n=0}^{N} c_nx^n=c_0(-1)^0+c_1(-1)^1+c_2(-1)^2+...
$$

As we evaluate think of each term as a vector on a one-dimensional plane. 

![[screenshot 2.png]]

Each term will rotate the vector 180 degrees. This just makes an oscillating function. Which just says that there are an equal number of positive and negative subsets. This is another show of how as we evaluate this function, we gain new information about our subsets. And there’s a lot more we can do with this. If we evaluate 2 functions togethers, $f(1)$ and $f(-1)$ we can find the sum of even coefficients

$$
\frac{1}{2}(f(1)+(f(-1)) = c_0+c_2+c_4+c_6
$$

So think about the rotation example, to find all coefficients divisible by 5, we can extend our one-dimensional plane into the complex range. Where the horizontal axis is labeled -1 to positive 1 and the vertical axis is labeled -1i to 1i. But how do use this complex plane to solve our problem? First we need to define a complex unit to work with. Lets use $\zeta$.

![[screenshot 3.png]]

We define $\zeta$ as a fifth of the way around the unit circle — $360 = 5(72)$ — so that it will take $\zeta^5$ to fully rotate 360 degrees in the complex plane. 








