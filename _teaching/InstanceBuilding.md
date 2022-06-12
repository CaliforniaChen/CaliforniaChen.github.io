---
title: "InstanceBuilding Dataset"
collection: teaching
excerpt: "A benchmark dataset, called **InstanceBuilding**, for instance segmentation of 3D buildings in urban scenes, which consists of both roof instances in RGBH images and roof/building instances in 3D mesh models.<br/><img src='/../files/DatasetInstanceBuilding/teaser.jpg'>"
type: "Released with IEEE TGRS paper"
permalink: /datasets/InstanceBuilding
venue: "Free for non-commercial use"
date: 2022-01-01
location: #"City, Country"
---

Introducation
======
The dataset, called **InstanceBuilding**, contains building instance annotation for both 3D urban scenes and UAV images simultaneously, which makes it unique. About 16 thousand roofs in UAV images are annotated, and 892 roofs/buildings in 3D urban scenes are annotated. Among these 892 buildings, more than 600 buildings are attached to others. In such crowded urban scenes, instance segmentation has a more signiﬁcant advantage over semantic segmentation in various applications. Comparisons with existing datasets can be found in our [IEEE TGRS paper](https://californiachen.github.io/publications/2022TGRS/).

2D annotation
======
We annotated 608 drone images with high resolutions for roofs. They are selected from around 20 thousand drone images acquired in more than 10 different cities by a consumer DJI drone Phantom 4 Pro with different cameras and ﬂight altitudes. There are about 16 thousand buildings in all these images, and their roofs are all manually annotated for the training of our 2D roof instance segmentation neural network.

<div align="center">
<img src='../files/DatasetInstanceBuilding/185-2400-5600-OR.jpg' width="48%" />
<img src='../files/DatasetInstanceBuilding/187-4000-5600-OR.jpg' width="48%" />
</div>
<br>
<div align="center">
<img src='../files/DatasetInstanceBuilding/s143.jpg' width="48%" />
<img src='../files/DatasetInstanceBuilding/C_C281.jpg' width="48%" />
Figure 1: Four examples of 2D annotated images.
</div>


3D annotation
======
We annotated 4 3D scenes for both roofs and entir buildings,  which are reconstructed using Bentley Acute3D ContextCapture from thousands of UAV images. To facilitate the 3D annotation, we have developed a simple but efficient brush-based annotation tool. Similar to most 2D annotation tools which semi-automatically extract pixels of an object by marking the closed boundary polygon of the object, our tool allows a user to segment a 3D building by casually drawing strokes on the building boundaries. 


<div align="center">
<img src='../files/DatasetInstanceBuilding/statistics.png' width="80%" />
</div>
* Scene1 (roofs on the left, buildings on the right):
<div align="center">
<img src='../files/DatasetInstanceBuilding/s1-roof.jpg' width="48%" />
<img src='../files/DatasetInstanceBuilding/s1-building.jpg' width="48%" />
</div>

* Scene2:
<div align="center">
<img src='../files/DatasetInstanceBuilding/s2-roof.jpg' width="48%" />
<img src='../files/DatasetInstanceBuilding/s2-building.jpg' width="48%" />
</div>

* Scene3:
<div align="center">
<img src='../files/DatasetInstanceBuilding/s3-roof.jpg' width="48%" />
<img src='../files/DatasetInstanceBuilding/s3-building.jpg' width="48%" />
</div>

* Scene4:
<div align="center">
<img src='../files/DatasetInstanceBuilding/s4-roof.jpg' width="48%" />
<img src='../files/DatasetInstanceBuilding/s4-building.jpg' width="48%" />
</div>

Download:
======
Google Driver:  

Baidu Cloud: https://pan.baidu.com/s/161n4MbaZWDfhMvMhcPedlw

Citation:
======
