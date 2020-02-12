- Follow along with [Sassmeister](https://www.sassmeister.com/) or in your own project notes.
- Exercises will be done using [these files]()

# 1. Variables

```scss
$variable-name: #345;
```

Color Example
```scss
$primary-color: #345;

.body {
  background: $primary-color;
}
```

Font Family
```scss
$primary-font: ‘Arail’, sans-serif;

.body {
  font-family: $primary-font;
}
```

Header Height Example
```scss
$header-height: 100px;

header {
  height: $header-height;
}

header .logo {
  display: inline-block;
  line-height: $header-height;
}
```

## Exercise
Convert our projects sass to use variables for the colors. Once all colors are converted, update the variable names to a different color scheme

# 2. Nesting
```scss
header {
  .logo {
    color: red; 
  }
}
```

Header Example
```scss
header {
  color: #222;
  
  .logo {
    color: white
  }
  
  li {
    display: inline-block;
  }
  
  a {
    color:white;
  }
}
```

Card Example
```scss
.card {
  padding: 20px;
  height: 200px;
  position: relative;
  
  h1 {
    font-size: 1.4em;
  }
  
  h2 {
    font-size: 1.2em;
  }
  
  .content-container {
    position: absolute;
    height: 80px;
    background: #222;
    bottom: 0;
  } 
}
```

## Exercise
Look for sections in our code where we are nesting css classes, and convert them over to use nesting

# 3. Imports
A common folder structure found in sass projects:
```bash
base/
  variables.scss 
  layout.scss 
  mixins.scss
components/
  header.scss 
  hero.scss 
  footer.scss 
  card.scss 
  buttons.scss 
  input.scss
pages/
  home.scss 
  about.scss 
  services.scss 
  contact.scss
```

Example of importing files into a master `app.scss` file:
```scss
@import ‘./header.scss’;
@import ‘./card.scss’;
```

## Exercise
Break up our sass file into seperate files based on the suggested structure above.


# 4. Extends
Button example
```scss
.button {
  background-color: #349;
  border: none;
  font-weight: bold;
  color: white;
}
.small-button {
  @extend .button;
  font-size: 0.8em;
  padding: 5px 10px;
}
.big-button {
  @extend .button;
  font-size: 1.2em;
  padding: 10px 20px;
}
```

## Exercise
Look for elements in our scss that could be extended. Possibly buttons or cards could be extended from a general style.

# 5. Mixins (you will recognize these as functions)
Example Mixin
```scss
@mixin verticalAlign($height) {
  display: inline-block;
  line-height: $height;
}
```

Background Image Example
```scss
 $mixin background-image($image-path) {
  background: url($image-path);
  background-size: cover;
  background-position: 50% 50%;
}
.hero {
  @include background-image(‘../img/hero.jpg’);
}
```

## Exercise
Convert our hero image into a mixin using the example above

