# OOPJS Script

The `Animator` class is a JavaScript script that provides methods for animating elements on a web page using CSS transitions and transformations. This script follows the principles of Object-Oriented Programming (OOP) to encapsulate the animation logic and make it reusable.

## Usage

To use the `Animator` class, follow these steps:

1. Include the script in your HTML file:

   ```html
   <script src="oops.js"></script>
   ```

2. Create an instance of the `Animator` class by passing a CSS selector as a parameter. This selector should match the element you want to animate.

   ```javascript
   const intro = new Animator("h1");
   const intro2 = new Animator("p");
   ```

3. Add event listeners or triggers to call the animation methods when necessary. In the provided example, a button click event triggers the animations:

   ```javascript
   const button = document.querySelector('button');

   button.addEventListener('click', () => {
       intro.move(1, true, { x: 100, y: 500 });
       intro2.move(2, true, { x: 200, y: 1000 });
   });
   ```

## Methods

The `Animator` class provides the following methods:

### `fadeOut(time, toggle = false)`

This method animates the element's opacity, making it fade out smoothly.

- `time` (required): The duration of the animation in seconds.
- `toggle` (optional): A boolean value indicating whether to toggle the animation. If `true` and the element has the CSS class `"fadeOut-active"`, the element will fade back in. Default is `false`.

### `move(time, toggle = false, { x = 0, y = 0 })`

This method animates the element's position, moving it horizontally and vertically.

- `time` (required): The duration of the animation in seconds.
- `toggle` (optional): A boolean value indicating whether to toggle the animation. If `true` and the element has the CSS class `"move-active"`, the element will move back to its original position. Default is `false`.
- `x` (optional): The horizontal distance to move the element. Positive values move it to the right, and negative values move it to the left. Default is `0`.
- `y` (optional): The vertical distance to move the element. Positive values move it down, and negative values move it up. Default is `0`.

## CSS Classes

The `Animator` class relies on the following CSS classes to control the animations:

- `"fadeOut-active"`: Applied to the element during a fade-out animation.
- `"move-active"`: Applied to the element during a movement animation.

Make sure to define appropriate CSS styles for these classes in your stylesheet to achieve the desired visual effects.
