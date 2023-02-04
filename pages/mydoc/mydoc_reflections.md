---
title: Reflections & Pitfalls
sidebar: mydoc_sidebar
permalink: reflections.html
folder: mydoc
---

# Project reflections & pitfalls


Our team has undoubtedly learn alot during the course of this project. This page elaborates on problems that we encountered which are not represented in the final product.


## Pitfalls
We mentioned a few pitfalls in the presentation; here we elaborate more on them.

- **Learning houdini and Vex** Starting an advanced project while learing the tooling is always a challenge. With Vex and houdini especially were difficult as : to BK students all programming is new, to CS students these are very unlike other programming alnguages.
- **Lack of resources online for architectural implementation in Houdini** Especially at the start of the project we found it difficult to design with the scope of the project in mind, as we were unfamiliar with houdini so could not predict its limits and strengths. 
- **Placing facades fiasco part 1, 2 & 3** These pitfalls are described in detail at the end of this page.
- **Time constraint** By the end of the project, we ound ourselves in a relative time crunch. There were many things we would have liked to do but didnt have the time for. Some of these aer listed ni the next section.
- **Github** Working with git and github pages was another new tool for the majority of the group, which we struggled to use effectively untill the end of the project. We feel this has greatly affected the quality of the website, and was in retrospect not the best method of documentation.
- **Building depth algorithm :** At the start of our implementation phase, we wanted to create a function that would ensure that the building would have a maximum depth (distance to windows) per level, which would make certain that each voxel in the building would get enough light dependant on the level each voxel was on. This function would modify the given voxel cloud such that the top levels would have a lower maximum depth than the bottom levels, improving the reach of natural light in the building. Creating this function was attempted using mainly VEX, and proved very difficult. This was in part due to inexperience with VEX, and creating a function that would remove points without leaving floating masses nor internal holes in the building (which do not improve sunlight) proved not feasible after many hours spent. - Pauline
- **Facade placing:** When the rotating facade was meade, came the challenge of the application of the facade on the voxelcloud. First we tried to place it on the facade, this took a lot of time and it created a repeating pattern all around the building. This effect was not what we wanted. So then we tried to manually add the facades in Rhino. This was also very time consuming. After 8 hours only 15% of the building was done. Then we tried it again with static facades in Houdini. Also a randomizer was used to apply different types of facades. Then the file had to be exported so the materials could be edited. This resulted in a lot of group forming and struggling a bit with the Houdini license before it could be uploaded properly.


## What would we have liked to improve given more time?

- Implement the weighting function.
- Make the growth agent less random.
- Generate hallways and elevator shafts using the defined entrance points, and place the growth seeds adjactent to these.
- Start earlier with docuemntation and the website to improve the quality.
- Work out more features that we had intended to implement in the design phase, such as: using different student housing types as noise buffers, placing facades to according to surroundings (eg using green facades to block noise), ensuring that the surface of each function complies with the metro networks that were designed.



## LOGBOEK

Here is a short overview of what each person in the team worked on per week of the project (besides following lectures etc). 

| week | Bogdan                                                             | Jessica | Noor                                           | Pauline                                                                  |
|:----:|:------------------------------------------------------------------:|:-------:|:----------------------------------------------:|:------------------------------------------------------------------------:|
| 1    | Design & familiarizing with houdini                                |         | Design & familiarizing with houdini            | Design & familiarizing with houdini                                      |
| 2    | Design & familiarizing with houdini                                |         | Research surrounding areas                     | Initializeing voxel cloud                                                |
| 3    | Familiarizing with houdini                                         |         | Working on brick moving facade                 | Plaza cut out                                                            |
| 4    | Sun analysis                                                       |         | Making brick moving facade                     | Attempted building depth algorithm                                       |
| 5    | Preparing midterm presentation                                     |         | Preparing midterm presentation                 | Preparing midterm presentation                                           |
| 6    | Exam Bk7084                                                        |         | Exam Bk7084                                    | Exam Bk7084                                                              |
| 7    | Fixing Sun Analysis                                                |         | Working on website                             | Placing moving facade on building (pt 1)                                 |
| 8    | Weights calcutation and brainstorm                                 |         | Working on website                             | Growth agent                                                             |
| 9    | Weights calcutation and merging with other parts of the project    |         | Working on exporting houdini and twinmotion    | Merging massing function with existing houdini pipeline & seed placement |
| 10   | Preparing for final presentation, writing report and documentation |         | Working on poster, presentation, documentation | Preparing for final presentation, writing report and documentation       |




## Placing facades fiasco

Arguably one of the most difficult problems we encountered was placing the facades we created onto the generated building. We had a total of 3 attempts at this (attempted by Pauline, Noor, and Jessica), of which the 3rd proved to be succesful. This section explains the process.

### Placing facades Part 1 : Normal generation

Once the Moving facade was created, it had to be applied to real facade of the generated building. This section descibes an attempted method to do so, but which did not lead to a satisfactory result.

**Given** are the moving facade peice of the same size as the face of a voxel and the voxel cloud with its outer facades seperated in a group. 
**Goal:** to place the facades by turning each point into a face using it neighbors, and using this face to calculate the normal of the point. 
1. Per point, we find its direct neighbors using houdini's 'nearpoints' function.
2. Using an attributewrangle, we create a face for each point by traversing its neighors: for each point we take the neighbor to its right, and for this neighbor we take its neighbor below it. We use these three points to construct a face, and add the face to the geometry using the 'addpolygon' function.
3. Using a 'normals' node, replace the normal of each point with the normal of its accoring face. 

**Result**
Implementing this gave the following results:

!!! TODO INSERT SCREENSHOT!!!

This method shows that this method worked for trivial shapes (the faces generated worked correctly on a rectangularly shaped voxel cloud), but became inconsistend when applied to more irregular shapes. The reaon for this was unknown, as it was decided that enough time had been spended on this method.

**Why didnt it work?**

The most likely reason this didnt work is because of the traversal method used. Typically to solve the described problem, one would put the point cloud in a linked data structure (such as a graph or a linked list like), which would make traversing positional neighbors (left, right, above, below) trivial. However, the Vex language does not support recursion, and in turn does not implement graph-like nor linked-list-like data structures. Implementing these from scratch was deemed out of scope for this problem. As a placeholder, the positional neigbors were found using maximal distances to neighbors; a horizontal neighbor ebing found with the maximum distane on the XZ plane, and a vertical neighbor being found witht the largest distance of the XY plane. This rule is most likely the reason this method did not work on less uniform point clouds, as the heuristic might nor always hold.
