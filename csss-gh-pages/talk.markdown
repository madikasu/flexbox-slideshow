flexbox

-- default display
see how each items is on its own line
divs are block level elements. 
They cause the next element to be on its new line
<p> is also a block level item, <a> is an inline item

flexbox is a display property
if we want to change this to a flex layout,
change the display type

-- display: flex
.parent { display: flex }
the items are no longer causing each 
other to be on a new line

== mess around with width

-- flex-direction
notice the numbers, 1 2 3 4 5
using flex-direction, we can reverse that
- add flex-direction: row-reverse to .parent

now they are lined up to the right, and the order 
has been reversed

the default is 'row'

we can change flex-direction to be column
we dont want them to be in a row
- change flex-direction to 'column'
now they are ordered top to bottom
- chnage flex-direction to 'column-reverse'
now they are ordered bottom to top



-- flex-wrap
the next property is flex-wrap
the default is nowrap
flex will constrain the items to be evenly distributed
- change item width to 500px

unless we tell it otherwise
flex-wrap can help us
- change flex-wrap: wrap;
- change item width to 30%;
we can also use 'wrap-reverse'
now they wrap backwards



-- justify-content
what if you want things aligned to the right
- change justify-content: flex-end;
now items are aligned to the end of the flex container
there is also center (to center horizontally)
- change justify-content: center;
this centers groups of items

- change justify-content: space-between;
this will 
	take the first item and move it all the way left
	take the last item and move it all the way right
	fill the space between evenly with remaining items
	
	
- change justify-content: space-around;
	this will add space around each item so 
	all items have even margins across container


-- align-items
align-items doesn't deal with the main axis, instead
it deals with the cross axis;
if we change it to flex-end, our items will align with the bottom of the container
- change align-items: flex-end

we can also center them
- change align-items: center;

finally we can use baseline
- change align-items: baseline;
- change item height:auto

for this, we'll need to change one of the items
to a larger font
- change an items font-size to 60px, 

see how they are all aligned to the baseline of the text

-- align-content
the next property is align-content
this applies to the items when they wrap


(the default is align-content: stretch)
- change comment out wrap and align-content
notice now our items are stretched
- change uncomment wrap and align-content
- change align-content: flex-start
this groups things to the top
- change align-content: flex-end
this groups things to the end

- change align-content: space-around
- change align-content: space-between
- change uncomment item height

space-around and space-between require a defined height


we've been doing things based on row.. flex-direction
kinda changes the x and y

- change flex-direction: column


-------------------------------------------
all these items applied to the parent, we haven't
changed the items themselves yet.
now we are going to look at the properties
a direct child of the flex element can have



properties items can have

-- order
order allows us to change the order of how flex items are displayed. the default order is 0, and all elements with the same order
are displayed in dom order.


-- flex-grow
flex-grow defines the ability for a flex item to grow, if necessary. It is a proportion of other items.
If all items have the same flex-grow (flex-grow:1), they will all have the same size proportions.
changing one to 2, that element will be twice the size

-- flex-shrink
flex-shrink defines the ability for a flex item to shrink if necessary

-- flex-basis
flex-basis defines the default size of an element before the remaining space is distributed, based on flex-direction
row -> width
column -> height


--flex
flex is the shorthand for flex-grow, flex-shrink, and flex-basis combined

-- align-self
align-self allows the default alignment to be overrideden for flex items