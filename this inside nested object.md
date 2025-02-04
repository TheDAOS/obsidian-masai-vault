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

