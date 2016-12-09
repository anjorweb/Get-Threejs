---
title: three.js-光源
date: 2016-12-07 21:42:37
tags: three.js
---




### **光源**

发光的物体叫光源，如太阳、电灯、燃烧的蜡烛、萤火虫等。



**ThreeJs中的光源**

光源基类`THREE.Light(hex)` 

由基类派生出的其他类

- `THREE.AmbientLight()`  环境光，环境光是一种无处不在的光，来自各个方向。

- `THREE.PointLight(color, intensity, distance)` 点光源，这种光源放出的光线来自同一点，且方向辐射自四面八方。

- `THREE.SpotLight(hex, intensity, distance, angle, exponet)` 聚光灯，这种光源的光线从一个锥体中射出，在被照射的物体上产生聚光的效果。

- `THREE.PointLight(hex)` 点光源

- `THREE.DirectionalLight(hex)`方向光，没有衰减的平行的光线，类似太阳光的效果，方向光只余方向有关，与远近无关。

  ​

各种光线是会产生叠加效果的，比如设置了0xff0000的环境光，再设置0x00ff00的方向光，最终作用到物体上是0xffff00的光。