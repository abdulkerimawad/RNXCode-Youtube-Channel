## CSS Practices - 3D Cube | [Watch on Youtube](https://youtu.be/u6naLz_6YQI)

**index.html**
```
<!DOCTYPE html>
<html lang="en">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="style.css" />
    <title>CSS Practices - 3D Cube</title>
  </head>
  <body>
    <div class="threed_zone">
      <div class="base">
        <div class="floor"></div>
        <div class="right"></div>
        <div class="back"></div>
        <div class="left"></div>
        <div class="front"></div>
        <div class="ceil"></div>
      </div>
    </div>
  </body>
</html>
```
\
**style.css**
```
* {
  padding: 0px;
  margin: 0px;
  box-sizing: border-box;
}

body {
  height: 100dvh;
  display: flex;
  justify-content: center;
  align-items: center;
}

.threed_zone {
  width: 300px;
  height: 300px;
  perspective: 600px;
}

.base {
  width: 300px;
  height: 300px;
  transform-style: preserve-3d;
  transform: translateZ(-300px) rotateX(60deg) rotateZ(60deg);
  display: grid;
  transition: transform .5s ease-in-out;
}

.base > div {
  grid-column: 1;
  grid-row: 1;
  opacity: .5;
}

.floor {
  background-color: #F00;
}

.right {
  background-color: #FF0;
  transform-origin: center right;
  transform: rotateY(90deg);
}

.back {
  background-color: #0FF;
  transform-origin: top center;
  transform: rotateX(90deg);
}

.left {
  background-color: #F0F;
  transform-origin: center left;
  transform: rotateY(-90deg);
}

.front {
  background-color: #0F0;
  transform-origin: bottom center;
  transform: rotateX(-90deg);
}

.ceil {
  background-color: #000;
  transform: translateZ(300px);
}
```
