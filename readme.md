# advenced-css-sass

## Three Pillars to write good html and css... and build good websites

1. Responsive design

- Fluid layouts
- Media queries
- Responsive images
- Correct units
- Desktop-first vs mobile-first

2. Maintainable and scalable code

- Clean
- Easy-to-understand
- Growth
- Reusable
- How to organize files
- How to name classes
- How to structure html

3. Web performance

- Less HTTP requests
- Less code
- Compress code
- Use a CSS preprocessor
- Less images
- compress images

# cascade and specificity:

- CSS declarations marked with !important have the highest priority.
- But, only use !important as a last resource. It's better to use correct specificities -- more maintainable code!
- Inline styles will always have priority over styles in external stylesheets.
- A selector that contains 1 ID is more specific than one with 1000 classes.
- A selector that contains 1 class is more specific than one with 1000 elements.
- The universal selector \* has no specificity value (0, 0, 0, 0).
- Rely more on **specificity** than on the order of selectors.
- But, rely on order when using 3rd-party stylesheets -always put your author stylesheet last.

# Inheritance in css

- Inheritance passes the values for some specific properties from parents to children -- **more maintainable code;**
- Properties related to text are inherited: font-family, font-size, color, etc;
- The computed value of a property is what gets inherited, not the declared value.
- Inheritance of a property only works if no one declares a value for that property;
- The _inherit_ keyword forces inheritance on a certain property;
- The _initial_ keyword resets a property to its initial value.

---

## Main SASS Features

- **Variables:** for reuseable values such as colors, font-sizes, spacing, etc;
- **Nesting:** to nest selectors inside of one another, allowing us to write less code;
- **Operators:** for mathematical operations right inside of CSS;
- **Partials and imports:** to write CSS in different files and importing them all into one single file;
- **Mixins:** to write reusable pieces of CSS code;
- **Functions:** similar to mixins, with the difference that they produce a value that can than be used;
- **Extends:** to make different selectors inherit declarations that are common to all of them;
- **Control directives:** for writing complex code using conditionals and loops(not covered in this course).

---

**NPM:**

1. package.json

- npm init
- npm install node-sass --save-dev
- npm install jquery
- npm uninstall jquery --save

2. npm run compile:sass
