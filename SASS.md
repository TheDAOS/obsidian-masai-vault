[[Get Started with SASS]]
SASS (Syntactically Awesome Stylesheets) is a preprocessor scripting language that is interpreted or compiled into CSS. It allows developers to use variables, nested rules, mixins, functions, and other features that make writing CSS more efficient and maintainable. SASS is designed to extend the capabilities of CSS, making it easier to manage large stylesheets and promote reusable code.

## Key Features of SASS:

### 1. Variables:
   SASS allows you to define variables to store values like colors, fonts, or any CSS value. This makes it easier to update styles across your entire project by changing the variable value in one place.
   ```scss
   $primary-color: #333;
   body {
     color: $primary-color;
   }
   ```

### 2. Nested Rules:
   SASS enables you to nest CSS selectors in a way that follows the same visual hierarchy of your HTML. This makes your stylesheets more readable and easier to manage.
   ```scss
   nav {
     ul {
       margin: 0;
       padding: 0;
       list-style: none;

       li {
         display: inline;
         a {
           display: block;
           padding: 6px 12px;
           text-decoration: none;
         }
       }
     }
   }
   ```

### 3. Mixins:
   Mixins allow you to define styles that can be reused throughout your stylesheet. They can also accept arguments, making them highly flexible.
   ```scss
   @mixin border-radius($radius) {
     -webkit-border-radius: $radius;
     -moz-border-radius: $radius;
     -ms-border-radius: $radius;
     border-radius: $radius;
   }

   .box {
     @include border-radius(10px);
   }
   ```

### 4. Functions:
   SASS includes a variety of built-in functions for performing operations on values, such as colors, numbers, and strings. You can also define your own custom functions.
   ```scss
   $width: 500px;
   $height: 300px;

   .box {
     width: $width;
     height: $height;
     background-color: darken(#ff0000, 10%);
   }
   ```

### 5. Importing:
   SASS allows you to import other SASS files, which helps in organizing your stylesheets into smaller, more manageable files.
   ```scss
   @import 'variables';
   @import 'mixins';
   @import 'layout';
   ```

### 6. Extends/Inheritance:
   The `@extend` directive allows one selector to inherit the styles of another, promoting code reuse and reducing duplication.
   ```scss
   .message {
     border: 1px solid #ccc;
     padding: 10px;
     color: #333;
   }

   .success {
     @extend .message;
     border-color: green;
   }
   ```

## Compilation:
SASS code needs to be compiled into CSS before it can be used in a web browser. This can be done using various tools and build systems, such as:
- **Command Line Interface (CLI)**: Using the `sass` command.
- **Build Tools**: Integrating with tools like Webpack, Gulp, or Grunt.
- **Online Compilers**: Using online services to compile SASS to CSS.

## Example:
Here is a simple example of a SASS file and its compiled CSS output:

##### SASS File (styles.scss):
```scss
$font-stack:    Helvetica, sans-serif;
$primary-color: #333;

body {
  font: 100% $font-stack;
  color: $primary-color;
}

h1 {
  font-size: 2em;
  color: darken($primary-color, 10%);
}

.nav {
  ul {
    margin: 0;
    padding: 0;
    list-style: none;

    li {
      display: inline;
      a {
        display: block;
        padding: 6px 12px;
        text-decoration: none;
      }
    }
  }
}
```

##### Compiled CSS (styles.css):
```css
body {
  font: 100% Helvetica, sans-serif;
  color: #333;
}

h1 {
  font-size: 2em;
  color: #292929;
}

.nav ul {
  margin: 0;
  padding: 0;
  list-style: none;
}

.nav ul li {
  display: inline;
}

.nav ul li a {
  display: block;
  padding: 6px 12px;
  text-decoration: none;
}
```
