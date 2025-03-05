CSS Flexbox is a layout module designed to make it easier to design flexible and responsive layout structures without using float or positioning. The term "Flexbox" is often used interchangeably with "flex," but it's important to clarify the distinction between the two.

## Flexbox vs. Flex

### 1. Flexbox:
   - **Definition**: Flexbox is a CSS layout model that allows you to design a flexible and efficient layout structure without using float or positioning.
   - **Properties**: Flexbox introduces a set of properties that can be applied to both the container (parent element) and the items (child elements) within the container.
   - **Container Properties**:
     - `display: flex;`: This property defines a flex container and enables a flex context for all its direct children.
     - `flex-direction`: Defines the direction of the main axis (row, row-reverse, column, column-reverse).
     - `justify-content`: Aligns items along the main axis (flex-start, flex-end, center, space-between, space-around, space-evenly).
     - `align-items`: Aligns items along the cross axis (flex-start, flex-end, center, baseline, stretch).
     - `flex-wrap`: Controls whether the flex items should wrap or not (nowrap, wrap, wrap-reverse).
     - `align-content`: Aligns flex lines when there is extra space in the cross-axis (flex-start, flex-end, center, space-between, space-around, stretch).
   - **Item Properties**:
     - `order`: Controls the order in which flex items appear in the flex container.
     - `flex-grow`: Defines the ability for a flex item to grow if necessary.
     - `flex-shrink`: Defines the ability for a flex item to shrink if necessary.
     - `flex-basis`: Defines the default size of an element before the remaining space is distributed.
     - `align-self`: Allows the default alignment (or the one specified by align-items) to be overridden for individual flex items.

### 2. Flex:
   - **Definition**: The term "flex" is often used to refer to the individual properties and values that control the behavior of flex items within a flex container.
   - **Usage**: When you see `flex` in CSS, it is typically shorthand for setting multiple flex properties at once. For example:
     ```css
     .item {
       flex: 1 1 100px;
     }
     ```
     This shorthand sets `flex-grow`, `flex-shrink`, and `flex-basis` all at once.
     - `flex-grow`: 1
     - `flex-shrink`: 1
     - `flex-basis`: 100px

## Key Differences

- **Scope**:
  - **Flexbox**: Refers to the entire layout model and the set of properties that enable flexible and responsive design.
  - **Flex**: Refers to the individual properties and shorthand used to control the behavior of flex items.

- **Application**:
  - **Flexbox**: Applied to the container to define the flex context.
  - **Flex**: Applied to the items within the flex container to control their behavior.


### Example

```html
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Flexbox Example</title>
  <style>
    .container {
      display: flex;
      flex-direction: row;
      justify-content: space-between;
      align-items: center;
      height: 200px;
      border: 1px solid #000;
    }
    .item {
      flex: 1 1 100px;
      background-color: lightblue;
      margin: 10px;
      text-align: center;
      line-height: 100px;
    }
  </style>
</head>
<body>
  <div class="container">
    <div class="item">Item 1</div>
    <div class="item">Item 2</div>
    <div class="item">Item 3</div>
  </div>
</body>
</html>
```

In this example:
- The `.container` uses Flexbox properties to define the layout.
- The `.item` elements use the `flex` shorthand to control their individual behavior within the flex container.