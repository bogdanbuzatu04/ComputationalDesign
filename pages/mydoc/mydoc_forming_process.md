---
title: Forming Process
sidebar: mydoc_sidebar
permalink: forming_process.html
folder: mydoc
---
This section will cover the facades and the plans.

## Inspiration
The Hague is filled with beautiful traditional brick buildings. Take for example the Binnenhof. The Neorenaissance style is found in the late 19th century neighborhood nearby the site, see the images below. Characteristic is the use of the bricks with ‘ speklagen’ in between, which creates striking horizontal lines in the masonry. Traditionally, a lighter natural stone is used for the layer. The combination of traditional red brown bricks with a speklaag is the main inspiration for our building. It is meant to give the modernly shaped building a connection with the old architecture. Thereby, bricks are a durable material which can be reused and come from a renewable source.  

<figure>
    <img src="../images/pedestriandistance.jpg"
         alt="binnenhof">
    <figcaption><i>Binnenhof The Hague<i></figcaption>
</figure>

<figure>
    <img src="../images/loosduinseweg.jpg"
         alt="weg1">
    <figcaption><i>Loosduinseweg<i></figcaption>
</figure>

<figure>
    <img src="../images/vangoghstraat.jpg"
         alt="weg2">
    <figcaption><i>Van Goghstraat<i></figcaption>
</figure>


## The Moving Bricks facade
At first our plan was to implement moving bricks in our building, to really give the connection with the old architecture a modern twist. This facade is based on the ‘ Gallery of Cloaked Bricks’ in Israel. 

<figure>
    <img src="../images/galleryofcloakedbricks.jpg"
         alt="cloaked">
    <figcaption><i>Gallery of Cloaked Bricks<i></figcaption>
</figure>

The facade consists of bricks connected with a metal rod, as shown in the image below. This makes it possible to individually move each brick. This principle can be used to block the warming sunlight in the summer and let it in during the winter. Thereby, more or less privacy can be created.

<figure>
    <img src="../images/bricks.jpg"
         alt="bricks">
    <figcaption><i>Bricks with rods <i></figcaption>
</figure>

The rotating facades can be used two ways in our building; as a double facade, where behind the rotating bricks a wall with windows is placed, and as a screen in front of the balcony. 

<figure>
    <img src="../images/optionsrotatingbrickscreen.jpg"
         alt="bricks">
    <figcaption><i>Rotating brick screen options <i></figcaption>
</figure>

The created moving facade is 3x3 meters to make placing on the voxels possible. A tutorial by Adrien Lambert (https://www.youtube.com/watch?v=bwekX8EJyus&t=222s&ab_channel=AdrienLambert) with some adjustments was used to create the facade. 

<figure>
    <img src="../images/brickmovingwall.jpg"
         alt="rotflowchart">
    <figcaption><i>Rotating brick flowchart <i></figcaption>
</figure>

Finally, we wanted to place the rotating bricks on the facades facing the main street. This would help create privacy, reduce noise from the street and also work as a sunscreen considering this facade faces south. However due to difficulties the facade is not placed in the final outcome. 

<figure>
    <img src="../images/movingfacade.gif"
         alt="bricksrot">
    <figcaption><i>Resulting 3x3 of the rotating brickstating brick screen options <i></figcaption>
</figure>


## The Static Facades
<figure>
    <img src="../images/different-facade-types.gif"
         alt="eight">
    <figcaption><i> The eight facades <i></figcaption>
</figure>

The static facades are designed to fit seamlessly against each other and follow the design of the rotating facade. To continue the ‘speklaag’ line, the green facade has planters of identical height on the same place. The ground floor facade is primarily meant as a facade for the public functions. It has a window/door reaching to the ground. The facades all have individual bricks and the green facade has plant obj’s. To save computing power, of all facades a ‘flat version’ has been made, where all the bricks are just one solid block.

<figure>
    <img src="../images/facades.jpg"
         alt="allfacades">
    <figcaption><i> The different types of static facades <i></figcaption>
</figure>


## Construction of the facades
### Brick facade

<figure>
    <img src="../images/brickfacade.jpg"
         alt="flowbricks">
    <figcaption><i> Flowchart of the brick facade construction process <i></figcaption>
</figure>

To make sure the same dimensions are used as for the rotating facade, the process starts off with the same grid. A loop is used to divide the points in speklaag and brick points. A ratio of 2 speklaag stones and 7 bricks is used. The top and bottom only have one layer of speklaag so that different facades parts can create a two layer speklaag together.  To create a stretcher bond part of the brick points (the uneven ones)  are translated. This added the need for half bricks on the sides of the facade, to make a seamless connection with other brick facades possible. Finally all parts are merged.

<figure>
    <img src="../images/facade-construction.gif"
         alt="gifbricks">
    <figcaption><i> GIF of the brick facade construction process <i></figcaption>
</figure> 


### Windows
<figure>
    <img src="../images/window.jpg"
         alt="flowwindows">
    <figcaption><i> Flowchart of the window construction process <i></figcaption>
</figure>


The construction of the windows is a pretty straightforward process with multiple boolean intersections. The height and width of the different types of window sills is chosen so they exactly fit between the bricks. 

<figure>
    <img src="../images/window-construction.gif"
         alt="flowwindows">
    <figcaption><i> GIF of the window construction process <i></figcaption>
</figure>

The walls with windows are created by using the window block to remove points, and selecting outer rows in the windowblock to copy half bricks or the new half speklaag type to. This integrates the window into the brickfacade design.


### Green facade
<figure>
    <img src="../images/greenfacade.jpg"
         alt="flowwgreen">
    <figcaption><i> Flowchart of the green facade  construction process <i></figcaption>
</figure>

The green facade uses the speklaag points of the brick facade. To center the planters, for the double row speklaag points the middle points are translated to be exactly in between the top and bottom row. The speklaag box is scaled into a planter. Multiple points are selected to place the plant obj on.


<figure>
    <img src="../images/greenfacade.gif"
         alt="flowwgreen">
    <figcaption><i> GIF of the green facade  construction process <i></figcaption>
</figure>


## Roofs and undersides
<figure>
    <img src="../images/wadiandgreenroof.jpg"
         alt="roofsexplanation">
    </figure>

To reach the goal of required green space, all roofs are green sedum roofs. As shown in the image above , this will help with water retention during rainfall. During dry times the water evaporates.  Abundant water can be stored in the wadi in the courtyard. 
Other benefits of green roofs are the cooling and insulating effect, the addition of biodiversity and the reduction of the urban heat island effect. 
By placing wooden decks on the sedum roof as shown in the other image above, the green roofs can be used as terraces for the inhabitants. 

<figure>
    <img src="../images/roofs.gif"
         alt="roofs">
    <figcaption><i> GIF of the different types of roofs and the underside <i></figcaption>
</figure>

The roofs and undersides are all 3x3 boxes. Roof tiles with different edges have been made to be able to follow the shape of the roof . However we haven’t been able yet to place them correctly and computationally on the final building, therefore in the final product only the roof tiles without edges are used.

<figure>
    <img src="../images/roof.jpg"
         alt="roofsflow">
    <figcaption><i> Flowchart of the roof construction <i></figcaption>
</figure>


## Facade showcase
<figure>
    <img src="../images/facadesshowcase.jpg"
         alt="facadeshowcase">
    <figcaption><i> Examples of what the facade would look like put together <i></figcaption>
</figure>


## Placing the facade
<figure>
    <img src="../images/facadesplacement1.jpg"
         alt="facadesplacement1">
    <figcaption><i> Flowchart of the facade placement <i></figcaption>
</figure>

The facade is placed automatically. This means that if the voxel input is changed, for example by a different type of agent growth, the facade tiles will still be applied correctly. 
For the north, west, south and east facades the same way of tile placement is used, however the facades have to be rotated respectively 0, 90, 180, and 270 degrees. The detailed placement is explained further below.


<figure>
    <img src="../images/facadesplac.gif"
         alt="facadesplacement1">
    <figcaption><i> GIF of the facade placement <i></figcaption>
</figure>

For the detailed placement of the facade, one of the eight facade tiles is placed on the centroids of the exterior primitives. First the entrance facades are placed with data from the entrance placement. Then the remaining ground floor points are selected to add the public ground floor facade to. Then points are randomly selected to place the remaining 6 facade tiles.

<figure>
    <img src="../images/facadesplacement2.jpg"
         alt="facadesplacementdetailflow">
    <figcaption><i> Flowchart of the facade placement detail <i></figcaption>
</figure>


<figure>
    <img src="../images/facadeplacementdetail.gif"
         alt="facadesplacementdetailgif">
    <figcaption><i> GIF of the facade placement detail <i></figcaption>
</figure>


## The placed facades

<figure>
    <img src="../images/incontext2.jpg"
         alt="placed">
    <figcaption><i>The placed facades<i></figcaption>
</figure>


## Sections and plans
<figure>
    <img src="../images/legend.jpg"
         alt="legend">
    <figcaption><i>Legend<i></figcaption>
</figure>

<figure>
    <img src="../images/plattegrond_2-1.jpg"
         alt="pg1">
    <figcaption><i>Map first floor<i></figcaption>
</figure>

<figure>
    <img src="../images/plattegrond_4-1.jpg"
         alt="pg1">
    <figcaption><i>Map fifth floor<i></figcaption>
</figure>

<figure>
    <img src="../images/doorsnede_1.jpg"
         alt="pg1">
    <figcaption><i>Cross section 1<i></figcaption>
</figure>

<figure>
    <img src="../images/doorsnede_2.jpg"
         alt="pg1">
    <figcaption><i>Cross section 2<i></figcaption>
</figure>

