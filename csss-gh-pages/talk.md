# Flexbox
## Introduction

### Intro (3)
This is the layout I'll be using throughout. As you can see,
each item is on its own line. divs are block level elements. They cause the next element to be on its new line. 
**FlexBox** is a display property. If we want to change this to a flex layout, we need to change the display type.

So what is Flex box

	
### What is Flexbox (4)
Flexbox is a new layout mode for CSS3

### Why Flexbox
Flexbox aims to change the need to use tables, floats, inline-blocks and other CSS properties
needed to lay out complex sites

### Concepts and Terminology (5)
Flexbox consists of *Flex Containers* and *Flex Items*. A Flex Container is declared
by setting the display property of an element to either **flex** or **inline-flex**.

Every child of a Flex Container is a Flex Item. There can be any number of Flex Items.
Everything outside a Flex Container and inside a Flex ITem is rendered as usual.

#### The Main Axis and the Cross Axis
Flexbox uses the concepts of the *Main Axis* and the *Cross Axis*. Flex Lines follow the
Main Axis. The Cross Axis is perpendicular to the Main Axis



#### Display:Flex (7)
Once we apply display:flex to the parent, it becomes a flex container. Each child element becomes
a flex item.  You can see that the items are no longer causing each other to be on a new line
 `mess around with width`

#### flex-direction (9)
The flex-direction allows you to change the axes of the Flex Container. The default is 'row'. 
With this value, Flex Items are laid out in the direction of the 'writing mode', left-to-right, 
top-to-bottom.

The other values are:
1. row-reverse: The main start and main end are swapped, flex items are now laid out right-to-left
2. column: the main axis and the cross axis are swapped. flex items are now laid out vertically
3. column-reverse: same as column, but reversed.


notice the numbers, 1 2 3 4 5
using flex-direction, we can reverse that
- add flex-direction: row-reverse to .parent

now they are lined up to the right, and the order 
has been reversed


we can change flex-direction to be column
we dont want them to be in a row
- change flex-direction to 'column'
now they are ordered top to bottom
- chnage flex-direction to 'column-reverse'
now they are ordered bottom to top



#### flex-wrap (12)
Using flex-wrap, you can create Flex Containers with multiple flex lines. If flex-wrap is
set to wrap, flex items wrap onto additional flex lines if there is not enough
room for them on one flex line. Additional flex lines are added in the direction of the 
Cross Axis. The default is nowrap

When flex-wrap is set to nowrap, items will be evenly distributed inside the flex container.
- change item width to 500px
unless we tell it otherwise

flex-wrap can help us
- change flex-wrap: wrap;
- change item width to 30%;
we can also use 'wrap-reverse'. wrap-reverse is the same as wrap except new flex lines
will be added in the opposite direction on the cross axis


#### justify-content (16)
the justify-content propert of the flex containers adjusts the positions of flex items 
on the main axis.

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


#### align-items (19)
align-items is complementary to justify-content. align-items adjusts the way
flex items are positioned on the cross axis. 
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

#### align-content (22)
align-content modified the behavior of flex-wrap. it is similar to align-items, but instead
of aligning flex items, it aligns flex lines.

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


### Properties of Flex Items
all these items applied to the parent, we haven't
changed the items themselves yet.
now we are going to look at the properties
a direct child of the flex element can have


#### order (26)
order is the simplest one. Setting orders for flex items adjusts their order when rendered.
The default order is 0, and all elements with the same order are displayed in dom order.

#### align-self (29)
the align-self property of flex items effectively overrides the flex containers align-items
property for that item.


#### flex-grow
flex-grow defines the ability for a flex item to grow, if necessary. It is a proportion of other items.
If all items have the same flex-grow (flex-grow:1), they will all have the same size proportions.
changing one to 2, that element will be twice the size

#### flex-shrink
flex-shrink defines the ability for a flex item to shrink if necessary

#### flex-basis
flex-basis defines the default size of an element before the remaining space is distributed, based on flex-direction
row -> width
column -> height

#### flex
flex is the shorthand for flex-grow, flex-shrink, and flex-basis combined



