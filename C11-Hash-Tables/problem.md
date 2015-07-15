### Problems 1 : Longest-probe bound for hashing
***
A hash table of size m is used to store n items, with n ≤ m/2. Open addressing is used for collision resolution.



![](http://latex.codecogs.com/gif.latex?
O\(1/n^2\) )
![](http://latex.codecogs.com/gif.latex?


### `Answer`
**a.**

P = (n/m)^k < (1/2)^k = 2^-k

**b.**

代入a中的结论即可

**c.**

![](http://latex.codecogs.com/gif.latex?P = \\prod_{i=0}^{2\\lg{n}}\\frac{m/2-i}{m} < \\prod_{i=0}^{2\\lg{n}} \\frac{1}{2} = \\frac{1}{2}^{2\\lg{n}} = \\frac{1}{4}^{\\lg{n}} = 4^{\\lg{n^{-1}}} = O\(n^{-1}\) )

**d.**

该题可以参考5.4.2节的关于**球与盒子**的结论和5.4.3节的关于**序列**的结论.

我们把每次的概率放大为1/2(实际上是≤ 1/2的) 

所以是O(lgn)



### Problems 2 : Slot-size bound for chaining
***
Suppose that we have a hash table with n slots, with collisions resolved by chaining, and suppose that n keys are inserted into the table. Each key is equally likely to be hashed to each slot. Let M be the maximum number of keys in any slot after all the keys have been inserted. Your mission is to prove an O(lg n/lg lg n) upper bound on E[M], the expected value of M.

**a.**
Argue that the probability Qk that exactly k keys hash to a particular slot is given by

![](http://latex.codecogs.com/gif.latex? Q_k = \(\\frac{1}{n}^k \) \(1-\\frac{1}{n}\)^{n-k} C_k^n)

### `Answer`



***
Follow [@louis1992](https://github.com/gzc) on github to help finish this task.
