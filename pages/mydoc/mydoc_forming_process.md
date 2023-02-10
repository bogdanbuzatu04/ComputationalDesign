---
title: Forming Process
sidebar: mydoc_sidebar
permalink: forming_process.html
folder: mydoc
---
This section will cover the facades and the plans.

## Inspiration
The Hague is filled with beautiful traditional brick buildings. Take for example the Binnenhof. The Neorenaissance style is found in the late 19th century neighborhood nearby the site, see the images below. Characteristic is the use of the bricks with ‘ speklagen’ in between, which creates striking horizontal lines in the masonry. Traditionally, a lighter natural stone is used for the layer. The combination of traditional red brown bricks with a speklaag is the main inspiration for our building. It is meant to give the modernly shaped building a connection with the old architecture. Thereby, bricks are a durable material which can be reused and come from a renewable source.  

![binnenhof](../images/thehague.jpg)
*Binnenhof The Hague*

![weq1](../images/loosduinseweg.jpg)
*Loosduinseweg*

![weq2](../images/vangoghstraat.jpg)
*Van Goghstraat*



## The Moving Bricks facade
At first our plan was to implement moving bricks in our building, to really give the connection with the old architecture a modern twist. This facade is based on the ‘ Gallery of Cloaked Bricks’ in Israel. 


![cloaked](../images/galleryofcloakedbricks.jpg)
*Gallery of Cloaked Bricks*


The facade consists of bricks connected with a metal rod, as shown in the image below. This makes it possible to individually move each brick. This principle can be used to block the warming sunlight in the summer and let it in during the winter. Thereby, more or less privacy can be created.


![bricks](../images/bricks.jpg)
*Bricks with rods*


The rotating facades can be used two ways in our building; as a double facade, where behind the rotating bricks a wall with windows is placed, and as a screen in front of the balcony. 

![rotating_bricks](../images/optionsrotatingbrickscreen.jpg)
*Rotating brick screen options*

The created moving facade is 3x3 meters to make placing on the voxels possible. A tutorial by Adrien Lambert (https://www.youtube.com/watch?v=bwekX8EJyus&t=222s&ab_channel=AdrienLambert) with some adjustments was used to create the facade. 

![rotflowchart](../images/brickmovingwall.jpg)
*Rotating brick flowchart*


Finally, we wanted to place the rotating bricks on the facades facing the main street. This would help create privacy, reduce noise from the street and also work as a sunscreen considering this facade faces south. However due to difficulties the facade is not placed in the final outcome. 

![bricksrot](../images/movingfacade.gif)
*Resulting 3x3 of the rotating brickstating brick screen options*




## The Static Facades

![eight](../images/different-facade-types.gif)
*The eight facades*

The static facades are designed to fit seamlessly against each other and follow the design of the rotating facade. To continue the ‘speklaag’ line, the green facade has planters of identical height on the same place. The ground floor facade is primarily meant as a facade for the public functions. It has a window/door reaching to the ground. The facades all have individual bricks and the green facade has plant obj’s. To save computing power, of all facades a ‘flat version’ has been made, where all the bricks are just one solid block.


![allfacades](../images/facades.jpg)
*The different types of static facades*


## Construction of the facades
### Brick facade
![flowbricks](../images/brickfacade.jpg)
*Flowchart of the brick facade construction process*


To make sure the same dimensions are used as for the rotating facade, the process starts off with the same grid. A loop is used to divide the points in speklaag and brick points. A ratio of 2 speklaag stones and 7 bricks is used. The top and bottom only have one layer of speklaag so that different facades parts can create a two layer speklaag together.  To create a stretcher bond part of the brick points (the uneven ones)  are translated. This added the need for half bricks on the sides of the facade, to make a seamless connection with other brick facades possible. Finally all parts are merged.


![gifbricks](../images/facade-construction.gif)
*GIF of the brick facade construction process*


### Windows
![flowwindows](../images/window.jpg)
*Flowchart of the window construction process*



The construction of the windows is a pretty straightforward process with multiple boolean intersections. The height and width of the different types of window sills is chosen so they exactly fit between the bricks. 

![flowwindows](../images/window-construction.gif)
*GIF of the window construction process*

The walls with windows are created by using the window block to remove points, and selecting outer rows in the windowblock to copy half bricks or the new half speklaag type to. This integrates the window into the brickfacade design.


### Green facade

![flowwgreen](../images/greenfacade.jpg)
*Flowchart of the green facade  construction process*

The green facade uses the speklaag points of the brick facade. To center the planters, for the double row speklaag points the middle points are translated to be exactly in between the top and bottom row. The speklaag box is scaled into a planter. Multiple points are selected to place the plant obj on.

![flowwgreen](../images/greenfacade.gif)
*GIF of the green facade construction process*


## Roofs and undersides

![roofsexplanation](../images/wadiandgreenroof.jpg)


To reach the goal of required green space, all roofs are green sedum roofs. As shown in the image above , this will help with water retention during rainfall. During dry times the water evaporates.  Abundant water can be stored in the wadi in the courtyard. 
Other benefits of green roofs are the cooling and insulating effect, the addition of biodiversity and the reduction of the urban heat island effect. 
By placing wooden decks on the sedum roof as shown in the other image above, the green roofs can be used as terraces for the inhabitants. 

![roofs](../images/roofs.gif)
*GIF of the different types of roofs and the underside*


The roofs and undersides are all 3x3 boxes. Roof tiles with different edges have been made to be able to follow the shape of the roof . However we haven’t been able yet to place them correctly and computationally on the final building, therefore in the final product only the roof tiles without edges are used.

![roofsflow](../images/roof.jpg)
*Flowchart of the roof construction*


## Facade showcase
![facadeshowcase](../images/facadesshowcase.jpg)
*Examples of what the facade would look like put together*

## Placing the facade

![facadesplacement1](../images/facadesplacement1.jpg)
*Flowchart of the facade placement*


The facade is placed automatically. This means that if the voxel input is changed, for example by a different type of agent growth, the facade tiles will still be applied correctly. 
For the north, west, south and east facades the same way of tile placement is used, however the facades have to be rotated respectively 0, 90, 180, and 270 degrees. The detailed placement is explained further below.


![facadesplacement1](../images/facadesplac.gif)
*GIF of the facade placement*

For the detailed placement of the facade, one of the eight facade tiles is placed on the centroids of the exterior primitives. First the entrance facades are placed with data from the entrance placement. Then the remaining ground floor points are selected to add the public ground floor facade to. Then points are randomly selected to place the remaining 6 facade tiles.

![facadesplacementdetailflow](../images/facadesplacement2.jpg)
*Flowchart of the facade placement detail*

![facadesplacementdetailgif](../images/facadeplacementdetail.gif)
*GIF of the facade placement detail*


## The placed facades
![placed](../images/incontext2.jpg)
*The placed facades*


## Sections and plans
![legend](../images/legend.jpg)
*Legend*

![pg1](../images/plattegrond_2-1.jpg)
*Map first floor*

![pg1](../images/plattegrond_4-1.jpg)
*Map fifth floor*

![pg1](../images/doorsnede_1.jpg)
*Cross section 1*

![pg1](../images/doorsnede_2.jpg)
*Cross section 2*

