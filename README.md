# bouncingball
Using the if statement to create a [bouncing ball](https://benjaminfox1.github.io/bouncingball/)

// Using the if statement to create a bouncing ball that changes
// colour

// initialize variables
var mySwitch=true;
var mySpeedX=2;
var mySpeedY=2;
var myX;
var myY;

function setup() {
  createCanvas(400, 400);
  
  //random placement of ball and colour
  myX=random(40,300);
  myY=random(40,300);
  fill(random(255),random(255),random(255));
}

function draw() {
  background(220);

  //draw my ellipse
  ellipse(myX,myY,80,80);

  myX=myX+mySpeedX*1;
  
  // if my ball hits the RHS or LHS, reverse the speed (-1)
  if (myX>width-40)
  {
    mySpeedX=mySpeedX*-1
    fill(random(255),random(255),random(255));
  } else if (myX<0+40)
  {
    mySpeedX=mySpeedX*-1;
    fill(random(255),random(255),random(255));
  }

  myY=myY+mySpeedY*1.2;
  
  // if my ball hits the Top or Bottom, reverse the speed (-1)
  if (myY>height-40)
  {
    mySpeedY=mySpeedY*-1
    fill(random(255),random(255),random(255));
  } else if (myY<0+40)
  {
    mySpeedY=mySpeedY*-1
    fill(random(255),random(255),random(255));
  }
  
}
