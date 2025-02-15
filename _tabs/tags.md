---
layout: tags
icon: fas fa-tags
order: 2
title: Blog Two
date: 2024-05-27 -500
categories: [home]
---

# Second Design

![Design One](/assets/lib/design5.png)


<pre>
  <code class="p5">
const minLineWidth = 0;
const maxLineWidth = 100;
let lineWidthChange = 10;

function setup() {
  createCanvas(300, 300);
  frameRate(1);
  strokeWeight(2);
  stroke(255);
}

function draw() {
  background(32);

  let lineWidth = random(minLineWidth, maxLineWidth);
  for(let lineY = 0; lineY < height; lineY++){
    lineWidth += random(-lineWidthChange, lineWidthChange);
    lineWidth = constrain(lineWidth, minLineWidth, maxLineWidth);

    line(width / 2 - lineWidth, lineY, width / 2 + lineWidth, lineY);
  }
}
  </code>
</pre>

Starting off, variables are declared including the minLineWidth, maxLineWidth and lineWidthChange. I decided to set the framerate to 1. In addition, line 15 is used to create a line width a random value between the minLineWidth and the maxLineWidth. I then decided to use a for loop to iterate the code. The code on line 17 is used to adjust the lineWidth by a random value.  Finally, the code on line 20 is used to draw a horizontal line centred on the canvas. This design is my favourite out of all four as it is the most well rounded and visually pleasing.

![Design Two](/assets/lib/design2.png)

In the second design, I decided to change the colour of the circle and background, as well as the numBlobs to 10. This changes the number of Blobs to 10, which is drastically less then the 150 in my previous design. In addition, I have changed this.x and this.y to be divided by 10 and 100 rather than 20. When clicked, the circle will continue to fall for an additional few seconds, in comparison to the previous values.

![Design Three](/assets/lib/design3.png)

I have changed the ellipses to squares, changing the size of them to 15 rather than 50. However, I kept the numBlobs to 150. Other than that, the design remains the same. However, it looks drastically different. This is primary because of the combination of the size, and shape.

![Design Four](/assets/lib/design4.png)

I decided to make a design similar, however change the number of numBlobs to 2 rather than 150. In addition, I changed the colour to black, rather than grey, or previous colours I have used in my designs. I like this design as it looks somewhat basic prior to being clicked, but once hovered over, it will turn green and once again move to a random location on the canvas. I believe this is my favourite design of all four.

