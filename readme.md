# We had a good run
## Attention!: Blankwork is  outdated
It's about time to kill Blankwork as a Sass Grid system. The ideas were simple and easy to grasp, but it is time you stopped using Blankwork and use something modern instead for all the responsive goodness. I would personally recommend you look at [Bourbon Neat](http://neat.bourbon.io) or [Susy](http://susy.oddbird.net)



<hr>




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


## wrapper() (
*mixin()*  

And you can pass in 3 parameters:	  
 + Column Count  
 + Center (true or false)  
 + Subtract - value in pixels, how much to subtract from the total width of this element after the math is done.   


## column()
*mixin()* 

A single column, that accepts 3 parameters as well:
 + Column Count  
 + Subtraction - A very useful option in my opinion. Say you have a block of 3 columns (each column say 10px, so 30px in total), and for that block you want 2px border and 5px padding. Well if you'll add them, you'll break the grid.   
Well, now _there is a cure_!  
column(3, 14px); Will automatically calculate a width of 16px and let you have the 14px for padding and the border!  
+ Gutter width (allows you to override the default gutter width);  

## container()  
*mixin()*  

If you want to have columns inside columns, usually grids break because you need either alphas and omegas, or they just don't work at all. Now they do, you just need to put your columns inside a container. This would for example be the #main-content or #sidebar  

## get_width() 
*function()*

When all you need is a specific width of column-count X, you can get that value from this function (this is not a mixin). Use for example like this:
		
		width: get_width(3);

get_width() has 2 parameters.   

 + Column Count  
 + Return Type. By default, it returns the width without margins(gutter), if you want to know the width including the gutter, you type get_width(x, false);  

The code is as documented as possible, so go ahead and read through it, nothing that much there, really. Please give me any feedback on the system, I'd really love to know what you think about it.  

You can reach me here or by mail me/at/themer/.me
