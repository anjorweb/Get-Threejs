

**网格，也是3D环境里使用比较多的物体对象**

var mesh = new THREE.Mesh( geometry, material );

网格 = 几何体+材质







**线条**

var line = new THREE.Line( geometry, material )  //线绘制方式：连续绘制

var line = new THREE.LineSegments( geometry, material )  //线绘制方式：绘制线段，相邻2点相连

