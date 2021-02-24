what are the various term involved in Box Model

1.Padding
2.Margin
3.Content
4.Border
Follow this steps to see Box Model in live action inside the Browser.
1] First save the below code in name.html and open in Chrome

<html>
<style>
p{
background: coral;
padding: 20px;
margin: 20px;
border: 20px solid blue;
width: 100px;
}
</style>
<body>
<p>This is some text</p>
</body>
</html>
You will See Output like this:
https://github.com/Learn-Write-Repeat/Web-Development/blob/main/wd-cp-3/Pawan_WD_BOX_MODEL/Images/output.png

2] Now Press ctrl+shift+i OR fn+f12 OR Open Developer Tools

You will be able to see this window
https://github.com/Learn-Write-Repeat/Web-Development/blob/main/wd-cp-3/Pawan_WD_BOX_MODEL/Images/window.png


Click on Computed option i.e. Second option
You will see this 
https://github.com/Learn-Write-Repeat/Web-Development/blob/main/wd-cp-3/Pawan_WD_BOX_MODEL/Images/computed.png

Now what you need to do is Press ctrl+shift+c OR Select the Element and click on the p element

Then Hover on the Box Model you will able to see which part of the element is padding and which part is margin and which is content.

So overall it should look like this
https://github.com/Learn-Write-Repeat/Web-Development/blob/main/wd-cp-3/Pawan_WD_BOX_MODEL/Images/demo%20.gif

3] Now we need the understand how box model Works!

First we have given background: coral that means the p i.e. paragraph element will have background color coral to it.
So the background color will cover Content and Padding box as we can see.

Note: You can always go ahead change the values for padding and margin to see in action.

Border will be at above the padding and below the margin it will not affect the position.
If we hover on Content we can see that width will affect only not the Padding and Margin.
Now Margin is the main factor if we change the value then it will affect the position of element.
You can additionally change the values of margin and padding using this guide.
for the any element if we write,
**margin : 10px 20px 30px 40px;**
This means value will be set for
**margin : Top Right Bottom Left Side**

Same thing will also be aplicable for padding also
*padding : 10px 20px 30px 40px;*
This means value will be set for
**padding : Top Right Bottom Left Side**

gear Things to Remember gear
Default box behaviour of element will be content-box .
You can change this behaviour by using box-sizing property .
Possible value will be
**box-sizing: content-box**;
here if we change height and width it will include only content NOT padding and border
**box-sizing: border-box**;
here if we change height and width it will include content, padding and border as well.
Last but not least The best way to learn is by doing!
