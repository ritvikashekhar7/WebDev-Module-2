**What is GRID
CSS grid is a layout method that supports 2D system. Basically it can handle both columns and rows, if we consider our webpage layout in terms of columns and rows. CSS grid gives you more control on your layout, you can assign rules to the parent.
In this article you will get to know all the possible ways to use CSS grid in your website and we will acheive same output but with different approaches.
We will be creating this layout.**
https://github.com/Learn-Write-Repeat/Web-Development/blob/main/wd-cp-3/Pawan_WD_GRID_PROPERTIES/Images/sample.png
Steps will be

So visit JSBin or Create your Developement environment on the local computer.

Code:
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width">
<title>Grid Properties</title>
<style>
.container > div{
background: lightgreen;
}
.container{
display: grid;
grid-gap:10px;
grid-template-columns: 100px 100px 100px;
grid-template-rows: 100px 100px;
}
</style>
</head>
<body>
<div class="container">
<div class="a">1</div> <div class="b">2</div> <div class="c">3</div> <div class="d">4</div> <div class="e">5</div> <div class="f">6</div>
</div> </body> </html>


We have root element Container which we set display property to Grid now grid in enabled on the element.

We have six elment on the page and want to display like in output image.

Code Part
.container{
display: grid;
grid-gap:10px;
grid-template-columns: 100px 100px 100px;
grid-template-rows: 100px 100px;
}
This will enable grid behaviour in container element. grid-template-columns : 100px 100px 100px; will create 3 columns of 100px in size. grid-template-rows : 100px 100px; will arrange those columns in 2 rows of 100px height;. grid-gap will provide gap in between elements.

Instead of using it like this you can use this also,
.container{
display: grid;
grid-gap:10px;
grid-template: repeat(2,100px) / repeat(3, 100px);
}
well, I know that I want 2 rows and 3 columns of same size so I used grid-template: row / column Property here. Now consider repeat functions working like repeat(how many times, how much size).
https://github.com/Learn-Write-Repeat/Web-Development/blob/main/wd-cp-3/Pawan_WD_GRID_PROPERTIES/Images/template.png
We will create Same layout with different styles.
1]
Code:
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width">
<title>Grid Properties</title>
<style>
.container{
display: grid;
grid-gap:10px;
grid-template-columns : repeat(3,1fr);
grid-template-rows: 100px 200px 100px;
}
.header{
background: lightgray;
grid-column-start:1;
grid-column-end:-1;
}
.menu{
background: lightblue;
grid-column:1 / 2;
}
.content{
background: lightgreen;
grid-column:2 / -1;
}
.footer{
background: lightcoral;
grid-column:1 / -1;
}
</style>
</head>
<body>
<div class="container">
<div class="header">Header</div>
<div class="menu">Menu</div>
<div class="content">Content</div>
<div class="footer">Footer</div>
</div>
</body>
</html>

**For the Container styles you know very well what does repeat function means, template columns and rows as well. i.e. It will divide column into 3 parts with 1 fr that is fraction of the available space in the grid container.

**Now we want header to flow full width so, used grid-column-start:1 & grid-column-end:-1. remember -1 is for until the end. Same rules will be applicable for footer as well.**

**For the menu we want this division only 1 column wide so we used grid-column-start:1 & grid-column-end:2.**

**For the content we want this division to continue from last used column side i.e. 2 so we used grid-column-start:2 & grid-column-end:-1.**

This is how we can implement design layout in structured format.

2]
Code
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width">
<title>Grid Properties</title>
<style>
.container{
display: grid;
grid-gap:10px;
grid-template-columns : repeat(3,1fr);
grid-template-rows: 100px 200px 100px;
grid-template-areas :
"h h h"
"m c c"
"f f f";
}
.header{
background: lightgray;
grid-area: h;
}
.menu{
background: lightblue;
grid-area: m;
}
.content{
background: lightgreen;
grid-area: c;
}
.footer{
background: lightcoral;
grid-area: f;
}
</style>
</head>
<body>
<div class="container">
<div class="header">Header</div>
<div class="menu">Menu</div>
<div class="content">Content</div>
<div class="footer">Footer</div>
</div>
</body>
</html>

Look into the styles of container
.container{
display: grid;
grid-gap:10px;
grid-template-columns : repeat(3,1fr);
grid-template-rows: 100px 200px 100px;
grid-template-areas :
"h h h"
"m c c"
"f f f";
}

**Here we can see we used new property grid-template-areas what this does actually it will let you create the visual representation structure of the template.**

**So we divided our container into 3 parts with 1 fr width.**

**Now First value h h h means that for the 3 parts in 1st row h component will be present.**

**On the 2nd row value m c c means 1 part of m component and remaning 2 parts for the c component in the row.**

**On the 3rd row value f f f means f component will display in 3 parts.**


We are supposed to assign component value to our required divisions using grid-area property. that we did in this part.
.header{
background: lightgray;
grid-area: h;
}

.menu{
background: lightblue;
grid-area: m;
}

.content{
background: lightgreen;
grid-area: c;
}

.footer{
background: lightcoral;
grid-area: f;
}

If you prefer to learn grid by playing you can visit CSS Grid Garden link
Always change the values and play around with code, this will give you better understanding
