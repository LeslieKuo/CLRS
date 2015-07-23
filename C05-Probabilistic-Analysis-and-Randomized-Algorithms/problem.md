### Problems 1 : Probabilistic counting
***
With a b-bit counter, we can ordinarily only count up to 2b - 1. With R. Morris's probabilistic counting, we can count up to a much larger value at the expense of some loss of precision.
We let a counter value of i represent a count of ni for i = 0, 1,..., 2b -1, where the ni form an increasing sequence of nonnegative values. We assume that the initial value of the counter is 0, representing a count of n0 = 0. The INCREMENT operation works on a counter containing the value i in a probabilistic manner. If i = 2b - 1, then an overflow error is reported. Otherwise, the counter is increased by 1 with probability 1/(ni+1 - ni), and it remains unchanged with probability 1 - 1/(ni+1 - ni).





### `Answer`
**a.**
每一次递增操作增加的期望为

![](http://latex.codecogs.com/gif.latex? E = 0 \\cdot \(1-\\frac{1}{n_{i+1}-n_i}\) + 1\\cdot \(n_{i+1}-n_i\) \\cdot \\frac{1}{n_{i+1}-n_i} = 1 )

**b.**

![](http://latex.codecogs.com/gif.latex? X_j \\quad\\text {stands for jth increment} \\\\ Var[X_j] = E[X_j^2] - E^2[X_j] = \(0^2 \\cdot \\frac{99}{100} + 100^2\\cdot\\frac{1}{100}\) - 1^2 = 99 \\\\ 
Var[X] = \\sum_{i= 1}^{n}Var[X_i] = 99n)


### Problems 2 : Searching an unsorted array
***
Thus problem examines three algorithms for searching for a value x in an unsorted array A consisting of n elements.















		B = new array[n]
		count = 0
		while(count < n):
			r = RANDOM(1, n)
			if A[r] == v:
				return r
			if B[r] == false:
				count += 1
				B[r] = true
		return false
		
**b.**
就是伯努力分布～n

**c.**
还是伯努力分布～n/k

**d.**
Section5.4.2,在每个盒子里至少有一个球前，要投多少个球.

n(lnn+O(1))

**e.**
平均查找时间是n/2,最坏查找时间是n

**f.**
最坏运行时间是n-k+1.平均运行时间是n/(k+1)

**g.**
都是n

**h.**
跟DETERMINISTIC-SEARCH是一样的，这时候的期望就是平均.

**i.**
自然是**DETERMINISTIC-SEARCH**


***
Follow [@louis1992](https://github.com/gzc) on github to help finish this task.
