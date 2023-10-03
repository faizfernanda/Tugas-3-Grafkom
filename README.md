# Tugas-3-Grafkom

## 2D square
![RGB Square](https://github.com/faizfernanda/Tugas-3-Grafkom/assets/101172294/43417155-d111-4ca4-b690-3026d1a5eeaa)
Berikut ini codingan dari gambar di atas :
```
 function draw() { 
    
        gl.clearColor(0,0,0,1); 
        gl.clear(gl.COLOR_BUFFER_BIT);
        
        //Melakukan penetapan koordinat segitiga pertama 
        let  coords = new Float32Array([-0.5, -0.5, -0.5, 0.5, 0.5, 0.5 ]);
       
        gl.bindBuffer(gl.ARRAY_BUFFER, bufferCoords);
        gl.bufferData(gl.ARRAY_BUFFER, coords, gl.STREAM_DRAW);
        gl.vertexAttribPointer(attributeCoords, 2, gl.FLOAT, false, 0, 0);
        gl.enableVertexAttribArray(attributeCoords); 
       
        // Pewarnaan segitiga pertama (RGB)
        let  color = new Float32Array( [0,1,0, 0,0,1, 1,0,0] );
    
        gl.bindBuffer(gl.ARRAY_BUFFER, bufferColor);
        gl.bufferData(gl.ARRAY_BUFFER, color, gl.STREAM_DRAW);
        gl.vertexAttribPointer(attributeColor, 3, gl.FLOAT, false, 0, 0);
        gl.enableVertexAttribArray(attributeColor); 
        
        // Menggambar segitiga pertama
        gl.drawArrays(gl.TRIANGLES, 0, 3);
    
        //Melakukan penetapan koordinat segitiga kedua 
        let  coords2 = new Float32Array([-0.5, -0.5, 0.5, -0.5, 0.5, 0.5]);
    
        gl.bindBuffer(gl.ARRAY_BUFFER, bufferCoords);
        gl.bufferData(gl.ARRAY_BUFFER, coords2, gl.STREAM_DRAW);
        gl.vertexAttribPointer(attributeCoords, 2, gl.FLOAT, false, 0, 0);
        gl.enableVertexAttribArray(attributeCoords); 
    
        // Pewarnaan segitiga kedua (RGB)
        let  color2 = new Float32Array( [0,1,0, 1,1,1, 1,0,0] );
    
        gl.bindBuffer(gl.ARRAY_BUFFER, bufferColor);
        gl.bufferData(gl.ARRAY_BUFFER, color2, gl.STREAM_DRAW);
        gl.vertexAttribPointer(attributeColor, 3, gl.FLOAT, false, 0, 0);
        gl.enableVertexAttribArray(attributeColor); 
        
        //Menggambar Segitiga kedua
        gl.drawArrays(gl.TRIANGLES, 0, 3);
    }
```

## 3D Cube
``![Cube 3D](https://github.com/faizfernanda/Tugas-3-Grafkom/assets/101172294/abbd9a69-2421-4665-965a-c99f196924f3)
Berikut Codingan gambar di atas :
```
function draw()
{ 
    gl.clearColor(0,0,0,1);
    gl.clear(gl.COLOR_BUFFER_BIT | gl.DEPTH_BUFFER_BIT);
    //depan
    drawPrimitive( gl.TRIANGLE_FAN, [0,1,1,1], [-0.5,-0.5,-0.5, -0.5,0.5,-0.5, 0.5,0.5,-0.5, 0.5,-0.5,-0.5]); 
    //atas
    drawPrimitive( gl.TRIANGLE_FAN, [1,0,0,1], [0.5,0.5,-0.5, -0.5,0.5,-0.5, -0.2,0.7,0.5, 0.8, 0.7, 0.5]);
    //belakang
    drawPrimitive( gl.TRIANGLE_FAN, [1,1,1,1], [-0.2,-0.3,0.5, -0.2,0.7,0.5, 0.8,0.7,0.5, 0.8,-0.3,0.5]); 
    // kiri
    drawPrimitive( gl.TRIANGLE_FAN, [0,0,1,1], [-0.5,0.5,-0.5, -0.5,-0.5,-0.5, -0.2,-0.3,0.5, -0.2,0.7,0.5]);
    //kanan
    drawPrimitive( gl.TRIANGLE_FAN, [1,1,0,1], [0.5,0.5,-0.5, 0.5,-0.5,-0.5, 0.8,-0.3,0.5, 0.8,0.7,0.5]); 
    //bawah
    drawPrimitive( gl.TRIANGLE_FAN, [0,1,0,1], [-0.5,-0.5,-0.5, -0.2,-0.3,0.5, 0.8,-0.3,0.5, 0.5,-0.5,-0.5]); 
}
```
- Cube With Not Font
![Cube with not font](https://github.com/faizfernanda/Tugas-3-Grafkom/assets/101172294/ef07fcd4-ade8-4be3-9ab7-e0a32c3db469)

- Cube With Not Top
![not top](https://github.com/faizfernanda/Tugas-3-Grafkom/assets/101172294/e2914624-fbb5-427b-a8c2-de5bb67aa18a)

