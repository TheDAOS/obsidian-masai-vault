## Question-1: Check Divisibility by 4
- You are given a number stored in a variable named `num`.
- Print `Yes` if the number is divisible by 4, else print `No`.

**Note:** A number is divisible by 4 if `num % 4 == 0`.

**Input:**
- The input contains a single positive integer `num`, where `num < 100000`.
**Output:**
- Print `Yes` if `num` is divisible by 4, otherwise print `No`.

**Sample Input:**
```js
12
```
**Sample Output:**
```js
Yes
```

- In the sample test case, the value stored in the variable `num` is `12`.
- Since `12 % 4 = 0`, it is divisible by 4, hence the output is `Yes`.

```js
let num = 8; // Replace with any number you want to check
if (num % 4 === 0) {
    console.log("Yes");
} else {
    console.log("No");
}
```

## Question-2: Print Grade
- You are given a number stored in a variable named `total`.
- Based on the value of `total`, print a grade as follows:
	- If `total == 100`, print `"A"`.
	- If `total >= 90`, print `"B"`.
	- If `total >= 80`, print `"C"`.
	- Otherwise, print `"F"`.

**Input:**
- The input contains a single integer which represents the total marks.

**Constraints:**
- `total <= 100`

**Output:**
Output the grade based on the total marks:
- If marks equal to 100 print "A"
- If marks greater than or equal to 90 print "B"
- If marks greater than or equal to 80 print "C"
- Else print "F"

**Sample Input:**
```js
80
```

**Sample output:**
```js
C
```

- In the sample test case, the value stored in the variable `total` is `80`.
- Since `80 >= 80,` the grade is "C".
	```js
	let total = 85; // Replace with any value of total
	
	if (total == 100) {
	    console.log("A");
	} else if (total >= 90) {
	    console.log("B");
	} else if (total >= 80) {
	    console.log("C");
	} else {
	    console.log("F");
	}
	```

## Nested
### Question: Admission Eligibility with Age Restriction
You are given two variables:
- `age`: Age of the candidate.
- `marks`: Entrance exam marks of the candidate.

Determine the eligibility for admission based on the following criteria:
1. If `age > 28`, print `"Not Eligible due to Age"`.
2. If `age >= 18` and `age <= 28`:
	- If `marks >= 70`, print `"Eligible for Admission"`.
	- Otherwise, print `"Marks too low"`.
3. If `age < 18`, print `"Not Eligible due to Age"`.

```js
let age = 20; // Replace with the candidate's age
let marks = 75; // Replace with the candidate's marks

if (age > 28) {
    console.log("Not Eligible due to Age");
} else if (age >= 18 && age <= 28) {
    if (marks >= 70) {
        console.log("Eligible for Admission");
    } else {
        console.log("Marks too low");
    }
} else if (age < 18) {
    console.log("Not Eligible due to Age");
}
```

#### Using &&
```js
let age = 20; // Replace with the candidate's age
let marks = 75; // Replace with the candidate's marks

if (age > 28) {
    console.log("Not Eligible due to Age");
} else if (age >= 18 && age <= 28 && marks >= 70) {
    console.log("Eligible for Admission");
} else if (age >= 18 && age <= 28 && marks < 70) {
    console.log("Marks too low");
} else if (age < 18) {
    console.log("Not Eligible due to Age");
}
```
