//Surfboard Generator 1 Refined
//...Overlaying new designs over the top
//...by Louis Eastaugh

color pink = color(224,94,175);
color blue = color(40,96,222);
color orange = color(232,135,42);
color green = color(42,232,126);


float xNose = random(100,500); //Nose (x)
float yNose = random(50,300);  //Nose (y)

float xRailL = random(50,250);  //Left Rail (x)
float yRailL = random(300,550); //Left Rail (y)

float xRailR = random(350,550); //Right Rail (x)
float yRailR = random(300,550); //Right Rail (y)

float xTailL = random(100,250); //Left Tail (x)
float yTailL = random(600,800); //Left Tail (y)

float xTailR = random(350,500); //Left Tail (x)
float yTailR = random(600,800); //Left Tail (y)

float xTail  = random(250,350); //Middle Tail (x)
float yTail  = random(600,800); //Middle Tail (y)

float curv = random(-40,40);

void setup (){
 size (600,900);
  background(green);
 
}


void draw(){
 

  ellipse(xNose,yNose,10,10);
  ellipse(xRailL,yRailL,10,10);
  ellipse(xRailR,yRailR,10,10);
  ellipse(xTailL,yTailL,10,10);
  ellipse(xTailR,yTailR,10,10);
  ellipse(xTail,yTail,10,10);
  
  fill(green);
    //Curve from Nose To Rail Right
  bezier(xNose,yNose,((xRailR+xNose)/2)+curv,((yRailR+yNose)/2)+curv,((xRailR+xNose)/2)+curv,((yRailR+yNose)/2)+curv,xRailR,yRailR);
  
    //Curve From Rail Right to Tail Right 
  bezier(xRailR,yRailR,((xRailR+xTailR)/2)+curv,((yRailR+yTailR)/2)+curv,((xRailR+xTailR)/2)+curv,((yRailR+yTailR)/2)+curv,xTailR,yTailR);
  
    //Curve from Tail Right to Tail Middle
  bezier(xTailR,yTailR,((xTailR+xTail)/2)+curv,((yTailR+yTail)/2)+curv,((xTailR+xTail)/2)+curv,((yTailR+yTail)/2)+curv,xTail,yTail);

    //Curve from Tail Middle to Tail Left
  bezier(xTail,yTail,((xTail+xTailL)/2)+curv,((yTail+yTailL)/2)+curv,((xTail+xTailL)/2)+curv,((yTail+yTailL)/2)+curv,xTailL,yTailL);
  
    //Curve from Tail Left to Rail Left
  bezier(xTailL,yTailL,((xTailL+xRailL)/2)+curv,((yTail+yRailL)/2)+curv,((xTail+xRailL)/2)+curv,((yTail+yRailL)/2)+curv,xRailL,yRailL);
  
    //Curve from Tail Left to Nose
  bezier(xRailL,yRailL,((xRailL+xNose)/2)+curv,((yRailL+yNose)/2)+curv,((xRailL+xNose)/2)+curv,((yRailL+yNose)/2)+curv,xNose,yNose);
  
  
  
}


void mousePressed(){

float xNose = random(100,500); //Nose (x)
float yNose = random(50,300);  //Nose (y)

float xRailL = random(50,250);  //Left Rail (x)
float yRailL = random(300,550); //Left Rail (y)

float xRailR = random(350,550); //Right Rail (x)
float yRailR = random(300,550); //Right Rail (y)

float xTailL = random(100,250); //Left Tail (x)
float yTailL = random(600,800); //Left Tail (y)

float xTailR = random(350,500); //Left Tail (x)
float yTailR = random(600,800); //Left Tail (y)

float xTail  = random(250,350); //Middle Tail (x)
float yTail  = random(600,800); //Middle Tail (y)

float curv = random(-40,40);
  
  
  
  
  fill(green);
    //Curve from Nose To Rail Right
    //..Both points from anchor being added and divided by 2
    //..Finds somewhat of a "centre point" and then uses "curv" which randomly choses a point to move from
  bezier(xNose,yNose,((xRailR+xNose)/2)+curv,((yRailR+yNose)/2)+curv,((xRailR+xNose)/2)+curv,((yRailR+yNose)/2)+curv,xRailR,yRailR);
  
    //Curve From Rail Right to Tail Right 
  bezier(xRailR,yRailR,((xRailR+xTailR)/2)+curv,((yRailR+yTailR)/2)+curv,((xRailR+xTailR)/2)+curv,((yRailR+yTailR)/2)+curv,xTailR,yTailR);
  
    //Curve from Tail Right to Tail Middle
  bezier(xTailR,yTailR,((xTailR+xTail)/2)+curv,((yTailR+yTail)/2)+curv,((xTailR+xTail)/2)+curv,((yTailR+yTail)/2)+curv,xTail,yTail);

    //Curve from Tail Middle to Tail Left
  bezier(xTail,yTail,((xTail+xTailL)/2)+curv,((yTail+yTailL)/2)+curv,((xTail+xTailL)/2)+curv,((yTail+yTailL)/2)+curv,xTailL,yTailL);
  
    //Curve from Tail Left to Rail Left
  bezier(xTailL,yTailL,((xTailL+xRailL)/2)+curv,((yTail+yRailL)/2)+curv,((xTail+xRailL)/2)+curv,((yTail+yRailL)/2)+curv,xRailL,yRailL);
  
    //Curve from Tail Left to Nose
  bezier(xRailL,yRailL,((xRailL+xNose)/2)+curv,((yRailL+yNose)/2)+curv,((xRailL+xNose)/2)+curv,((yRailL+yNose)/2)+curv,xNose,yNose);
  
  
  
}
