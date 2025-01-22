## Question-1: Check Divisibility by 4 Using Ternary Operators

- You are given a number stored in a variable named `num`.
- Print `Yes` if the number is divisible by 4, else print `No`.

**Note**: A number is divisible by 4 `if num % 4 == 0`.

##### Input:
- The input contains a single positive integer `num`, where `num < 100000`.

##### Output:
- Print `Yes` if `num` is divisible by 4, otherwise print `No`.

##### Sample Input:
```js
12
```

##### Sample Output:
```js
Yes
```

- In the sample test case, the value stored in the variable `num` is `12`.
- Since `12 % 4 = 0`, it is divisible by 4, hence the output is `Yes`.

## Question-2: Print Grade Using Ternary Operators

- You are given a number stored in a variable named `total`.
- Based on the value of `total`, print a grade as follows:
	- If `total == 100`, print "A".
	- If `total >= 90`, print "B".
	- If `total >= 80`, print "C".
	- Otherwise, print "F".

##### Input:
- The input contains a single integer which represents the total marks.

##### Constraints:
- `total <= 100`

##### Output:
Output the grade based on the total marks:
- If marks equal to 100 print "A"
- If marks greater than or equal to 90 print "B"
- If marks greater than or equal to 80 print "C"
- Else print "F"

##### Sample Input:
```js
80
```

##### Sample Output:
```js
C
```

- In the sample test case, the value stored in the variable `total` is `80`.
- Since `80 >= 80`, the grade is "C".

## Question-3: The Ashes! (One Day Edition)
- You are given the scores of two cricket teams, Australia and England, stored in variables named `Australia` and `England` respectively.
- Determine the winner based on the scores:
	- If `Australia > England`, print "Australia".
	- If `Australia < England`, print "England".
	- If `Australia == England`, print "Tie".

##### Input:
- The input contains two space-separated integers denoting the scores of Australia and England respectively.