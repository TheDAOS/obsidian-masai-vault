Here are several **examples** that demonstrate how `this` behaves inside nested objects:
***

## Example 1: Direct Access with `this` in Nested Object

```js
const company = {
  name: "TechCorp",
  location: "New York",
  department: {
    name: "Engineering",
    getDepartmentInfo: function () {
      return `Department: ${this.name}, Location: ${this.location}`;
    },
  },
};

console.log(company.department.getDepartmentInfo());
// Output: "Department: Engineering, Location: undefined"
```

### Explanation:
- In the `department` object, `this` refers to `department`, not `company`.
- Therefore, `this.name` correctly accesses `department.name` ("Engineering").
- However, `this.location` is `undefined` because `location` exists in the `company` object, not in `department`.
***

## Example 2: Correct Access to Parent Object's Properties

To correctly access the parent object (`company`) properties, we can pass a reference:

```js
const company = {
  name: "TechCorp",
  location: "New York",
  department: {
    name: "Engineering",
    getDepartmentInfo: function () {
      return `Department: ${this.name}, Company Location: ${company.location}`;
    },
  },
};

console.log(company.department.getDepartmentInfo());
// Output: "Department: Engineering, Company Location: New York"
```

### Explanation:
- `company.location` is explicitly accessed instead of relying on `this`.
- This avoids the scoping issue of `this` in nested objects.
***

