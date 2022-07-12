<!--  -->
<!-- SELECTOR -->
<!-- element selsector -->
tag name is element selcectit

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

 <!-- change the anchor links color red that comes after every h2 --> 