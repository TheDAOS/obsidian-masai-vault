## Question-1: Divisibility by K using While loop
- You are provided with two numbers stored in variables named `num` and `K`.
- Your task is to print all numbers within the range `[1, num]` for which the number is divisible by `K`.
- A number `i` is divisible by `K` if `i % K == 0`.

##### Input:
The first and the only line of input contains two values, `num` and `K`, stored in the variables respectively.

##### Output:
Print all numbers from 1 to `num` that are divisible by `K`, each on a new line.

##### Sample Input:
```text
7 2
```
​
##### Sample Output:
```text
2 4 6
```

##### Hint:
- In the sample test case, the value stored in `num` is 7, and the value stored in `K` is 2.
- All the values in the range from `[1, 7]`, for which the condition `i % K == 0` is true, are 2, 4, and 6.

## Question-2: Identify Prime using While loop
- You are given a number stored in a variable named `num`.
- Determine if `num` is a prime number. A prime number is only divisible by 1 and itself.
- Print "Yes" if `num` is a prime number, otherwise print "No".

##### Input:
The first and the only line of input contains the value stored in `num`.

##### Output:
Print "Yes" if the number is a prime, otherwise print "No".

##### Sample Input:
```text
13
```

##### Sample Output:
```text
Yes
```

##### Hint:
- In the sample test case, the value stored in `num` is 13. Since 13 is a prime number (not divisible by any other numbers except 1 and itself), the output is "Yes".

## Question-3: Fizzbuzz Challenge using While loop
Fizzbuzz is a popular challenge for all types of programming languages. It is a simple challenge that tests your ability to use control structures. You will use loops and conditionals to solve this challenge.

1. Write a program that prints the numbers from 1 to 100.
2. For multiples of 3 print “Fizz” instead of the number
3. For the multiples of 5 print “Buzz”.
4. For numbers which are multiples of both 3 and 5 print “FizzBuzz”.

##### Hints
- You can use the modulus operator to check if a number is divisible by another number.
- You can echo `<br>` tag to add a line break after each number.

## Question-4 : Find Sum of Multiples using While loop
- You are given three integers: `n`, `k`, and `y`.
- Calculate the sum of the first `k` multiples of `n` that are also divisible by `y`.

##### Input: 
- The input consists of three spaced integers: `n`, `k`, and `y`.

##### Output:
- Output the sum of the first `k` multiples of `n` that are divisible by `y`.

##### Sample Input:
```js
3 10 5
```

##### Sample Output:
```js
45
```

##### Output Explanation:
- For the sample input, n = 3, k = 10 and y = 5.
- The first 10 multiples of n (3) are: 3, 6, 9, 12, 15, 18, 21, 24, 27, 30.From these, the multiples of n that are also divisible by y (5) are: 15, 30.
- The sum of 15 and 30 is 45.