# Blankwork SCSS Grid
So I've tried lots of grid systems, and still never really found what I was looking for. So I decided to try making my own, and this is my attempt. 
Blankwork allows you to have a wrapper, container and columns at the moment.

# Usage:
Pretty straight forward:

## Global Variables:
$_columns - Total number of columns
$_column-width - Width of a singlel column
$_gutter - Width of the gutter *(margins divided by 2 on each side of each column)*

The total width is calculated automatically.


## wrapper
And you can pass in 3 parameters:
* Column Count
* Center (true or false)
* Subtract - value in pixels, how much to subtract from the total width of this element after the math is done. 


## column
A single column, that accepts 3 parameters as well:
* Column Count
* Subtraction - A very useful option in my opinion. Say you have a block of 3 columns (each column say 10px, so 30px in total). 

* Gutter width (allows you to override the default gutter width);