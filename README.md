# what-tye
burning ship infinite zoom its already there and its a fractal ig
Give you the live URL where your fractal viewer will be accessible
<!DOCTYPE html>
<html lang="en">
<head>
  <meta charset="UTF-8">
  <title>Burning Ship Fractal Infinite Zoom</title>
  <style>
    html, body {margin:0; padding:0; background:#000;}
    #canvas {display:block; margin:0 auto; background:#111;}
    #instructions {
      position:fixed;
      top:8px; left:8px;
      background:rgba(32,32,32,0.7);
      color:#fff; font-family:sans-serif;
      padding:10px 12px; border-radius:8px;
      font-size:14px;
      z-index:10;
    }
  </style>
</head>
<body>
<div id="instructions">
  <b>Burning Ship Fractal: Infinite Zoom</b><br>
  <b>Mouse Wheel / Pinch</b>: Zoom<br>
  <b>Click+Drag / Touch-Drag</b>: Pan<br>
  <b>Double Click</b>: Zoom in at point<br>
</div>
<canvas id="canvas" width="700" height="500"></canvas>
<script>
const canvas = document.getElementById('canvas');
const ctx = canvas.getContext('2d');
const W = canvas.width, H = canvas.height;

// Initial view for Burning Ship
let state = {
    x: -1.8,
    y: -0.02,
    scale: 2.2,
    maxIter: 120
};

function draw() {
    let image = ctx.createImageData(W, H);
    let baseScale = state.scale;
    let xMin = state.x - baseScale, xMax = state.x + baseScale;
    let yMin = state.y - baseScale*H/W, yMax = state.y + baseScale*H/W;
    let maxIter = state.maxIter;
    let zoomExp = -Math.log2(state.scale/2.2);

    for(let py=0; py<H; ++py) {
        let y0 = yMin + (y
        
