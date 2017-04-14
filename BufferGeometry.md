

更高效的Geometry

高效的秘诀：将数据放在一块连续的内存空间内，和geometry一样，它存储顶点、面索引、法线、颜色、纹理、坐标和自定义的一些几何数据。

连续的存储空间能够节省传递数据到GPU的空间。

Javascript的Unit16Array、Float32Array等对象能够分配指定数目的整形或者浮点型数组，由他们分配的数组是线性的，连续的单元，所有CPU访问的速度极快无比。

根据顶点算顶点的法线：

```javascript
var pA = new THREE.Vector3();
var pB = new THREE.Vector3();
var pC = new THREE.Vector3();

var cb = new THREE.Vector3();
var ab = new THREE.Vector3();

pA.set( ax, ay, az ); 
pB.set( bx, by, bz );
pC.set( cx, cy, cz );

cb.subVectors( pC, pB );  //设置向量pC - pB
ab.subVectors( pA, pB );   //设置向量pA - pB
cb.cross( ab );   //设置cb 和 ab的叉积

cb.normalize();   //向量归一
```

