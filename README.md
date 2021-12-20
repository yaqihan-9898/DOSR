
Dataset for Oriented Ship Recognition (DOSR)
------

This dataset has been published in our paper [Fine-Grained Recognition for Oriented Ship Against Complex Scenes in Optical Remote in Remote Sensing Images][1], doi:10.1109/TGRS.2021.3123666. Related ship recognition code is published on [here][2]

I. Introduction
--
DOSR is a public available dataset for fine-grained ship recognition with **1066** optical remote sensing images and **6127** ship instances. Images in DOSR are collected from Google Earth. The image size is ranged from 600 pixels to 1300 pixels with resolution of 0.5m-2.5m. To expand the diversity of data, we collect images from quantities of countries, including the United States, China, France, Japan, etc. The shooting time spans from 2001 to 2020. 

In DOSR, there are 832 nearshore scenes containing 5212 instances and 234 offshore scenes containing 915 instances. 
The dataset is divided into three sets: training set with 523 images, validation set with 223 images and testing set with 320 images. 
Fig.1 displays examples of 20 fine-grained classes in DOSR. Instance amount of each class is shown in Table I.

![image](https://github.com/yaqihan-9898/DOSR/blob/main/20class.png)
<p align="center">Fig. 1 Examples of 20 Fine-grained Classes in DOSR</p>

<p align="center">Table I Instance Amount</p>

| Class Name        | Class Short Name   |  Total amount  |  Train amount  |  Val amount|  Train+Val amount   |Test amount   |
| :--------:   | :-----:  | :----:  | :----:  | :----:  | :----:  | :----:  |
| Transpot     | Tra. |   1682     |820|358|1178|504|
| Yacht        |   Yac.   |   1188   |583|214|797|391|
| Speedboat        |    Spe.    |  529  |166|69|235|294|
| Auxiliary Ship       |    Aux.    |  426  |216|95|311|115|
| Military Ship        |    Mli.    |  419  |204|68|272|147|
| Tug        |    Tug    |  293  |169|58|227|66|
| Fishing Boat        |    Fis.    |  276  |166|49|215|61|
| Bulk Cargo Vessel        |    BCV.    |  275 | 144|60|204|71|
| Cargo        |    Car.    |  249  |109|51|160|89|
| Container        |    Con.    |  177  |92|38|130|47|
| Cruise        |    Cru.    |  165  |86|30|116|49|
| Deckbarge        |    DeB.    |  100  |51|20|71|29|
| Tanker        |    Tan.    |  86  |45|20|65|21|
| Deckship        |    DeS.    |  69  |40|12|52|17|
| Flat Traffic Ship        |    FTS.    |  59 |42|6|48|11|
| Floating Crane        |    Flo.    |  38  |16|13|29|9|
| Multihull        |    Mul.    |  36  |14|12|26|10|
| Barge        |    Bar.    |  34  |23|4|27|7|
| Communication Ship        |    Com.    |  14  |5|3|8|6|
| Submarine        |    Sub.    |  12  |7|1|8|4|

Fig.2 shows several typical scenes in DOSR such as small scene, small and dense scene, regular dense scene, irregular dense scene, scale variance scene, and clutter scene.



<div align=center><img width="900" src="https://github.com/yaqihan-9898/DOSR/blob/main/Typical%20scenes.png"/></div>
<p align="center">Fig. 3 Typical Scenes in DOSR</p>

II. Annotations
--
We provide 2 versions of annotations for study.

### 1. Five-parameter Annotations
All images are annotated in VOC format. Each instance is represented by a five-parameter tuple (x,y,w,h,θ), which is consisted with our paper "Fine-Grained Recognition for Oriented Ship Against Complex Scenes in Optical Remote Sensing Images". Fig.3 explains the meaning of five parameters.

<div align=center><img width="700" src="https://github.com/yaqihan-9898/DOSR/blob/main/annotation.png"/></div>

<p align="center">Fig. 3 Parameters of oriented bounding box. (a) Reference rectangle, θ=0；(b) θ=(0,2/pi); (c) θ=pi; (d) (2/pi,pi)</p>

### 2. Eight-parameter Annotations
All images are annotated in VOC format. Each instance is represented by an eight-parameter tuple (x1,y1,x2,y2,x3,y3,x4,y4), which describes the coordinates of the four vertices of the oriented bounding box. In addition, we also provide annotations of horizontal bounding boxes in this version. We obtained horizontal bounding boxes by calculating minimum bounding rectangles of oriented bounding boxes, and use 4-parameter (xmin,ymin,xmax,ymax) to describe the horizontal bounding boxes. 

III. How to obtain
--
You can get DOSR at (1) [Google Drive][3] or (2) [Baidu Netdisk][4] with access code **1596**

[1]: https://ieeexplore.ieee.org/document/9591580
[2]:https://github.com/yaqihan-9898/EIRNet
[3]:https://drive.google.com/file/d/1X0vKWP7TlGK_4kiVVGMVSUbEhZoFT-l3/view?usp=sharing
[4]: https://pan.baidu.com/s/1I7N0I_y2en2_PyYhMzuScg
