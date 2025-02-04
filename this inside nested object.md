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
- 