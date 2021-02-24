Topic : Introduction to CSS GRID gear
**What is CSS grid?
CSS grid is a layout method that supports 2D system. Basically it can handle both columns and rows, if we consider our webpage layout in terms of columns and rows. CSS grid gives you more control on your layout, you can assign rules to the parent.
So basically what we do in CSS Grid is actually divide our design components into rows and columns. with the help of GRID we can design complex structures in simple manner.
Okay so. Take a look at this layout. We will try to understand GRID working by building this layout.
https://github.com/Learn-Write-Repeat/Web-Development/blob/main/wd-cp-3/Pawan_WD_INTRODUCTION_GRID/Images/layout.png
We are going to build this layout.
Steps will be**

So visit JSBin or Create your Developement environment on the local computer.

Initially there will be 2 tabs open i.e. html and output Part. click on the css. Your screen should look like this.
https://github.com/Learn-Write-Repeat/Web-Development/blob/main/wd-cp-3/Pawan_WD_INTRODUCTION_GRID/Images/environment.png
Okay. copy this code first, I will expalin in upcoming points.
<html>
<head>
<meta charset="utf-8">
<meta name="viewport" content="width=device-width">
<title>CSS Grid</title>
<style>
.container{
display: grid;
grid-template-columns : 25% 25% 25% 25%;
grid-template-rows: 50px 100px 50px;
}
nav{
grid-column-start:1;
grid-column-end:-1;
background:pink;
}
main{
grid-column-start:1;
grid-column-end:4;
background: orange;
}
aside{
grid-column-start:4;
grid-column-end:-1;
background: lime;
}
footer{
grid-column-start:1;
grid-column-end:-1;
background:lightblue;
}
</style>
</head>
<body>
<div class="container">
<nav>This is navigation part.</nav>
<main>This is Body part. </main>
<aside>This is aside (Ads Part).</aside>
<footer>This is Footer part.</footer>
</div>
</body>
</html>

*As you can see First at the ROOT level Only one element is there i.e. Container in the stylings I made its display property to Grid. Which enables Grid behaviour on this element.
.container{
display: grid;
grid-template-columns : 25% 25% 25% 25%;
grid-template-rows: 50px 100px 50px;
}
Four times I used 25% it means create 4 column structure with equal width, and in the rows i have used 50px 100px 50px it means give height to the 3 respective rows.*

**Now I will explain the nav the same rule follows for remaining sections.
nav{
grid-column-start:1;
grid-column-end:-1;
background:pink;
}
So as per our layout I want navigation to cover whole width i.e. we have divided our continer into 4 columns right?. Now I will tell my nav to cover from grid-column-start:1** to grid-column-end:-1;. -1 nothing but go until the END.

**Same concept will be applicable for remaining elements.
Example
I want my Body part extend till 4th side and Ads part from the 4th to end. I will write.
main{
grid-column-start:1;
grid-column-end:4;
background: orange;
}
aside{
grid-column-start:4;
grid-column-end:-1;
background: lime;
}**

Overall your final code should look like this.
https://github.com/Learn-Write-Repeat/Web-Development/blob/main/wd-cp-3/Pawan_WD_INTRODUCTION_GRID/Images/final.png
