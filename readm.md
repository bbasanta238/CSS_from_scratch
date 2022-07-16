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

<!-- text align property -->
center: -> all text align to center
justify:-> takes all text and matched it to take all of its width as possible


<!-- mostly used fonts -->
serif
sans-serif
monospace


<!-- NOTE : !important -->

  <!-- external fonts link are place above the stylesheet so that before compiling stylesheet the fonts are ready to go -->


<link href="https://fonts.googleapis.com/css2?family=Inter:wght@300&family=Montserrat:wght@300&family=Poppins:wght@500&display=swap" rel="stylesheet">
    <!-- external fonts link are place above the stylesheet so that before compiling stylesheet the fonts are ready to go -->
    <link rel="stylesheet" href="../css/style.css">

<!-- -------------------------------------------- -->

 font-family: 'Inter', sans-serif;

 <!-- here at firs 'Inter; font is loaded that is taken from internet but if in case of failure of loading Inter font family then sans-serif is applied (NOTE: sans-serif is alredy in almost every machine) -->


<!-- float -->
first should know about inline and block level element

block level element
eg: <p>,<div>,

inline element
eg; <span>

<!-- important: inline block -->
combination of both block and inline element

lets talk about float

<!-- float--> simply how the element float in the page -->
float: right --> pushed that element in right and according below element are pushed to the left side of that element
<!--  -->
<!--  -->
DISPLAY
<!--  -->
<!--  -->
display: none -->disappears the element


<!--  -->
<!-- FLEXBOX --> all below properties are used in flex --------------------------->
<!--  -->

display : flex 

flex-direction: row or column  -> A-E
flex-direction: column-reverse //--> reverse the element like E-A
flex-wrap : wrap || reverse ||nowrap --> no wrap means all item is squezzed to fit in a single line
<!-- row is default value -->

justify-content : flex-start|| flex-end|| center|| space-between||.... -->align item between left and right corner
align-item : flex-start || flex-end || center ||stretch  --> align item betweem top and bottom

<!-- inline order element in a flexbox-container -->
<!-- ----------------------- -->
<div class="container">
        <div class="container-item" style="order:2;">A</div>
        <div class="container-item" style="order:1;">B</div>
        <div class="container-item" style="order:3;">C</div>
</div>

output order: B A C

<!-- other flex properties -->
flex-grow : 1 || 2 --> grabs the 1 or 2 times extra space available  //default for flex-grow is 0

flex-shrink : 0||1||2 -->shrinks the element 1 or 2 times fast, 0 means don't shrink that item //default is 1

flex-basis :100px -->identify minimum width of any flex-element //there is no default for flex-basis

NOTE: when the tab size goes below flex-basis minimum width, the proportion of flex-grow is lost and flex-shrink default value is applied

flex-box:1 -->default value is 1 that shrinks all the element at same rate

<!-- All three properties can be used in a single line -->

flex: frow shrink basis
eg. flex: 1 1 100px;

<!--  -->
<!-- ------ITEM ALIGNMETN------------ -->
<!--  -->
align-self will override algin-item

align-self: center||flex-start||flex-end

<!--  -->
<!-- till here flexbox-------------------------------- -->
<!--  -->

<!-- ----------------------------------- -->
<!-- GRID -->
<!-- ------------------------------------------------- -->

display: grid

Template rows and columns

grid-template-columns: auto auto auto;   unit like px,em,...,fr can also be used
<!-- elements are placed in 3columns -->

grid-template-rows: auto auto ;
<!-- elements are placed in 2 rows -->

<!--  -->
JUSTIFY AND ALIGN GRID
<!--  -->

justify-content:
align-content:

<!-- grid gap -->

grid-column-gap: 10px;
grid-row-gap: 100px;

all together can be used by foloowing ways

grid gap: 200px 150px;  //row-gap column-gap 

<!-- grid coulumn and grid row -->
grid-column : 1/2;
grid row : 1/2;

<!-- combine both column and row -->
grid-area : 1/1/2/2
row start/coulmn start/row end/column end

<!-- browser prefixes -->
-webkit-
-moz-
-o-
-ms-

<!-- particular for some browser -->
-webkit-transistion: -->for chrome and safari
-moz-transition: -->for mozilla
-o-transition: --> for opera

<!-- keyframe -->
animation has atleast two key frames one starting and other ending

<!-- @keyframes name {} -->
@keyframes translate-element{
    from{ background : red }
    to {background: black }
}

#about{
    animation-name: translate-element;
    annimation-duration:
    animation-iteration-count: 2 || infinite
    animation-timing-function:
    animation-direction:

<!-- combinily -->
    animation: animation-name, animaiton-duration ,timing-function , delay ,iteration-count ,animation-direction

}