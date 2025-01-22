### Question-1: Compare two Numbers
You are given two numbers stored in two variables, with the name, `num1` and `num2`

Print the result of the following operations

```js
1. num1 > num2 -> this operation prints true, if num1 is greater than num2, otherwise it prints false
2. num1 < num2 -> this operations prints true, if num1 is smaller than num2, otherwise it prints false
3. num1 == num2 -> this operation print true, if num1 is equal to num2, otherwise it prints false
```

You have to print the result of three operations in the order as shown above

Print the result of three operations, one by one, on a new line

Sample Input
```js
4 16
```
Sample Output
```js
False
True
False
```

#### Hint
- In the sample test case, the value stored in `num1 = 4` and value stored in `num2 = 16`
- In the first operation `num1 > num2`, `4` is not greater than `16`, so we get the output as `false`
- In the second operation `num1 < num2`, `4` is lesser than `16`, so we get the output as `true`
- In the third operation `num1 == num2`, `num1` is not equal to `num2`, so we get the output as `false`

### Question-2: Compare Seven Numbers

You are given seven numbers, stored in the variable with the following names
```js
a,b,c,d,e,f,g
```

You have to declare two variables, `sum1` and `sum2`, such that `sum1 = (a + b) * c` and `sum2 = (d + e + f + g)`

Print the output of the following operation
```js
sum1 > sum2
```

Sample Input
```js
1 2 3 4 5 6 7
```

Sample Output
```js
False
```

#### Hint
- In the sample test case, the value stored in the variables is as follows
	```note
	a = 1,b = 2,c = 3,d = 4,e = 5,f = 6,g = 7
	```
- The value of `sum1`, as explained in the problem statement will be, `sum1 = (a + b) * c = (1 + 2) * 3 = (3) * 3 = 9`
- Similarly, the value of `sum2`, as explained in the problem statement will be `sum2 = (d + e + f + g) = (4 + 5 + 6 + 7) = 22`
- The operation `sum1 > sum2` will print false, as the value of `sum2` is greater than `sum1`, hence the output false

### Question-3: Cube and Square
You are given two numbers `n` and `m`, you need to check if cube of `n` is greater than square of `m`.

Print `True` if the cube of `n is greater than the square of m`, or else print `False`.

Sample Input
```js
2 3
```

Sample Output
```js
False
```

#### Hint
- In the given sample test case `n = 2` and `m = 3` , so cube of `n` is `2*2*2 =8` and square of `m` is `3*3 = 9`
- Here cube of `n` is less than the square of `m`
- Therefore Output is `False`
