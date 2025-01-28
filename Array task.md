1. Create an empty array and assign it to a variable named `animalList`.
	`let animalList = [];`

2. Check and print the type of the empty array you just created using `typeof`.
	`console.log(typeof animalList);`

3. Declare an array called `wildAnimals` and populate it with five animal names as strings.
	`let wildAnimals = ["lion", "tiger", "elephant", "cheetah", "zebra"];`

4. Print the first animal from the `wildAnimals` array to the console.
	`console.log(wildAnimals[0]);`

5. Access and log the third animal in the `wildAnimals` array using `console.log()`.
	`console.log(wildAnimals[2]);`

6. Log the last animal from the array to the console.
	`console.log(wildAnimals[wildAnimals.length - 1]);`

7. Update the first animal in the `wildAnimals` array to "panther" and print the updated array.
	`wildAnimals[0] = "panther";`

8. Change the last animal in the `wildAnimals` array to "rhino" and print the updated array.
	`wildAnimals[wildAnimals.length - 1] = "rhino";`

9. Find and store the total number of elements in the `wildAnimals` array in a variable called `totalAnimals`.
	`let totalAnimals = wildAnimals.length;`

10. Assign the fourth animal from the array to a new variable named `speedyAnimal`.
	`let speedyAnimal = wildAnimals[3];`

11. Append a new animal "hyena" to the end of the `wildAnimals` array.
	`wildAnimals.push("hyena");`

12. Insert the animal "wolf" at the beginning of the array using an array method.
	`wildAnimals.unshift("wolf");`

13. Remove the first animal from the array and print the updated array.
	`wildAnimals.shift();`

14. Remove the last animal from the array and print the new length of the array to the console.
	`wildAnimals.pop();`
	`console.log(wildAnimals.length);`

15. Delete the second-to-last animal in the `wildAnimals` array.
	`wildAnimals.splice(wildAnimals.length - 2, 1);`

16. Write a `for` loop to print all the animals in the `wildAnimals` array to the console.
	```js
	for (let i = 0; i < wildAnimals.length; i++) {
	    console.log(wildAnimals[i]);
	}
	```

17. Modify the above loop to display both the index and animal in the format `index: animal`.
	```js
	for (let i = 0; i < wildAnimals.length; i++) {
	    console.log(`${i}: ${wildAnimals[i]}`);
	}
	```

18. Use a `for..of` loop to iterate through `wildAnimals` and log each animal.
	```js
	for (let animal of wildAnimals) {
	    console.log(animal);
	}
	```

19. Create a variable named `lastAnimal` that always stores the last animal in the `wildAnimals` array.
	`let lastAnimal = wildAnimals[wildAnimals.length - 1];`

20. Add a new animal "gorilla" at index 50 in the `wildAnimals` array and print the array to see the effect.
	`wildAnimals[50] = "gorilla";`
	`console.log(wildAnimals);`

***
## Solution
Here’s the revised version with animals as the theme and solutions included below each question:
***
### 1. Create an empty array and assign it to a variable named `animalList`.
##### Code:
```js
let animalList = [];
```

**Solution**: An empty array `animalList` is declared using `let`.
***
### 2. Check and print the type of the empty array you just created using `typeof`.

##### Code:
```js
console.log(typeof animalList);
```

**Solution**: The `typeof` operator checks and prints the type of `animalList`, which is `object` because arrays in JavaScript are technically objects.
***
### 3. Declare an array called `wildAnimals` and populate it with five animal names as strings.

##### Code:
```js
let wildAnimals = ["lion", "tiger", "elephant", "cheetah", "zebra"];
```

**Solution**: The array `wildAnimals` is created and initialized with five animal names.
***
### 4. Print the first animal from the `wildAnimals` array to the console.

##### Code:
```js
console.log(wildAnimals[0]);
```

**Solution**: Using the index `0`, the first element (`"lion"`) is accessed and printed to the console.
***
### 5. Access and log the third animal in the `wildAnimals` array using `console.log()`.

##### Code:
```js
console.log(wildAnimals[2]);
```

**Solution**: The element at index `2` is `"elephant"`, which is printed to the console.
***
### 6. Log the last animal from the array to the console.

##### Code:
```js
console.log(wildAnimals[wildAnimals.length - 1]);
```

**Solution**: The `length` property is used to find the last index (`wildAnimals.length - 1`), which is `"zebra"`.
***

### 7. Update the first animal in the `wildAnimals` array to `"panther"` and print the updated array.

##### Code:
```js
wildAnimals[0] = "panther";
console.log(wildAnimals);
```

**Solution**: The value at index `0` is changed to `"panther"`. The updated array is printed.
***
### 8. Change the last animal in the `wildAnimals` array to `"rhino"` and print the updated array.

##### Code:
```js
wildAnimals[wildAnimals.length - 1] = "rhino";
console.log(wildAnimals);
```

**Solution**: The last element is updated to `"rhino"` using the `length` property.
***
### 9. Find and store the total number of elements in the `wildAnimals` array in a variable called `totalAnimals`.

##### Code:
```js
let totalAnimals = wildAnimals.length;
console.log(totalAnimals);
```

**Solution**: The `length` property returns the number of elements in the array, which is stored in `totalAnimals`.
***
### 10. Assign the fourth animal from the array to a new variable named `speedyAnimal`.

##### Code:
```js
let speedyAnimal = wildAnimals[3];
console.log(speedyAnimal);
```

**Solution**: The element at index `3` (`"cheetah"`) is assigned to `speedyAnimal` and logged.