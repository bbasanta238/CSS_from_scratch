<!--  -->
<!-- SELECTOR -->
<!-- element selsector -->
tag name is element selcect0r

p{

}

h1{

}


<!-- class selector -->

.aclass{

}

<!-- ID selector -->
#someID{

}

<!-- when we shold use id and class -->
normally classes are used to select multiple elements
id is used only once and used to select only one element

<!-- priority of selection -->
element selector/headers
class selector
id selector
iniline selectot
<!-- eg. inline selector overrides above selector -->
<!-- eg. id selector overrides class,element -->


<!-- pseudo-selectors -->
:hover
::before
::after
:only-child
....so on

for a link some of the pseudo-selector
<!-- show link in color blue as the page is not visited -->
#google-link:link{
    color:blue;
}

<!-- after page visited the color is changed to purple -->
#google-link:visited{
    color:purple;
}



<!--  -->
<!-- Advanced Selector -->
<!--  -->
eg.

h2 + a{
    color: red;
}

 <!-- change the anchor links color red that comes after every h2 --> (h2 + a)

<!-- /* every butto after text area but under same parent element */ -->
textarea ~ button{
    color: green;
}

<!-- /* every single li inside of ul change color to blueviolet*/ -->
ul>li{
    color: blueviolet;
}
<!-- -----------------------------IMPORTANCE -->

">" is the child selector(ul>li)

"" is the descendant selector(ul li)

The difference is that a descendant can be a child of the element, or a child of a child of the element or a child of a child of a child ad inifinitum.

A child element is simply one that is directly contained within the parent element:

<foo> <!-- parent -->
  <bar> <!-- child of foo, descendant of foo -->
    <baz> <!-- descendant of foo -->
    </baz>
  </bar>
</foo>


<!-- other seector -->
eg. img[src="../img/"]{

}
<!--selectingElement[attribute = value]  -->



<!-- CSS general rules -->
selector{
    property: value;
}

<!--background  -->
background-size: contain; 
<!-- it stretch the image with constant proportion -->

background-size: cover; i
<!-- it fills the div with image nut doesnot care about proportion, it will simply remove the part that goes out of div while stretching -->


<!-- different types of units -->

PX
% --> depends on its parent element
em -->depends on its parent element  // 1em = 16px
rem --> depends on ::root or html 

<!-- NOTE: -->
in padding,margin use of em makes alot responsive since em depends on its font size;

eg:
.p{
    font-size: 2em;
    padding: 1em; //here padding 1em = font-size 2em
}

.p{
    font-size: 2rem;
    padding: 1rem; //here 1rem of padding depends on root but not its font-size---
}