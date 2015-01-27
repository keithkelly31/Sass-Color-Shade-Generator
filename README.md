# sass-color-maps
Sass-color-maps allows you to easily set colors and generate a Sass map with all of the base colors and shades.

Setup:

1.  Copy or import the code to your sass project
2.  Set your base colors in the $colors valiable
    Colors can be named how you want, but it is recommended that the names are relevant and easy to remember as they will be used to call the color in your code.
3.  Compile your Sass code
4.  Enjoy!


Usage:

Once you set your base colors and compile the code you can use the colors in your Sass by using the color() function.  The function takes two arguments: color and shade.

The color argument is any of the named colors you set up in the $colors variable.

The shade argument are the shades of the color.  The options include:

1.  base - The value is the same as the value described during the setup
2.  lightest - sets the lightest color tint by mixing the base with 80% white
3.  lighter - sets the light color tint by mixing the base with 20% white
4.  darker - sets the color tone by mixing the base with 20% mid-gray (#555)
5.  darkest - sets the color shade by mixing the base with 20% black


Example:

If the colors variable sets the following colors:

```
$colors: (
    blue:   #0000FF,
    green:  #00FF00
);
```
    
The colors can be called in the code by using the color function.  The following example will set the body background to the lightest shade of the base blue color.

```css
body {
    background-color: color(blue, lightest);
}
```