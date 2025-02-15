---
# the default layout is 'page'
icon: fas fa-info-circle
order: 4
title: Blog Four
date: 2024-05-27 -500
categories: [home]
---

# Fourth Design

![Design One](/assets/lib/design13.png)

I like this design as it is very unique, and the user is able to interact with it by moving their mouse. The lower the mouse is to the bottom of the screen, the closer the points will appear. The design shows several bright colours, in a star field. I believe that of all three, this is my favourite design of them all. I like the concept of it being a star field, with a vast variety of different colours that appear to come closer to the screen with mouse movement.
<pre>
  <code class="p5">
let victors = [];
let factor = 100;

function setup() {
  createCanvas(windowWidth, windowHeight);
  for (let i = 0; i < 500; i++) {
    victors[i] = createVector(
      random(-width * factor, width * factor),
      random(-height * factor, height * factor),
      random(width)
    );
  }
}

function draw() {
  background(0);

  translate(width / 2, height / 2);

  for (let v of victors) {
    let x = v.x / v.z;
    let y = v.y / v.z;
    let maxSize = map(mouseY, 0, height, 0, 50);
    let d = map(v.z, 0, width, maxSize, -5);

    fill(x, y, x * y, 2 * d);
    stroke(x, y, x * y);
    circle(x, y, d);
    arc(x, y, d, d, 0, PI + d / 2, PIE);
    
    
    v.z -= map(mouseX, 0, 400, -5, 5);
    if (v.z < 1) {
      v.x = random(-width * factor, width * factor);
      v.y = random(-height * factor, height * factor);
      v.z = random(width);
    }
  }
}
  </code>
</pre>
Looking at the code, we can see that the variables are declared, both victors and factor. Victor is an array containing objects representing the points. Factor is used to determine the starting position of the points. Each vector has their random coordinates distributed on the canvas. In addition, the z coordinate controls the depth of the point. Line 18 is used to move back to the centre of the canvas. The maxSize is used by mapping the Y position of the mouse, resulting in a range of circles, they will be larger when the mouse is lower. Line 32 is used to decrease the z value, resulting in the point moving towards the user. 

![Design Two](/assets/lib/design14.png)

I changed the value on line 32 from -5, 5 to -2, 2. This resulted in the colours being a solid colour when the mouse is moved to the bottom of the screen, however, remain normal otherwise.

![Design Three](/assets/lib/design15.png)

I changed line 24 from -15 to 100, resulting in changing the size of the circles to full size ‘blobs’.