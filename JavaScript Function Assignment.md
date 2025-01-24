## Question-1 : Odd Sum Below N

- You are given a number stored in a variable named `num`.
- Your task is to find the sum of all odd numbers that are greater than 0 and less than or equal to `num`.
- You will also write a function `isOdd` that returns a boolean value indicating whether a number is odd.

##### Input: 
The input consists of a single integer value stored in `num`.

##### Output: 
Find the sum of all odd numbers greater than 0 and less than or equal to `num`, and print it.

##### Function Requirement:
- Define a function `isOdd(n)` that returns `True` if `n` is odd, and `False` otherwise.

##### Sample Input:
```js
7
```

##### Sample Output:
```js
16
```

##### Explanation:
- For the input `num = 7`, the odd numbers less than or equal to 7 are: 1, 3, 5, 7.
- The sum of these numbers is 1 + 3 + 5 + 7 = 16, which is the required output.

## Question-2: Change the Case

- You are given a string containing both uppercase and lowercase characters.
- Your task is to change each uppercase character to lowercase and each lowercase character to uppercase.
- You must create a function named `changeCase` which takes a single character (either uppercase or lowercase) and returns the opposite case of that character.

##### Input:
- The next line will contain the string.

##### Function Requirement:
- Define a function `changeCase(c)` that takes a character `c` and returns its opposite case (uppercase to lowercase or lowercase to uppercase).

##### Output: 
- Output the string after changing the case of each character as described.

##### Sample Input:
```js
aBbcd
```

##### Sample Output:
```js
AbBCD
```

##### Explanation:
- The function `changeCase` should convert each character to its opposite case:
	- `a` to `A`
	- `B` to `b`
	- `b` to `B`
	- `c` to `C`
	- `d` to `D`
- The resulting string `"AbBCD"` is the output.
