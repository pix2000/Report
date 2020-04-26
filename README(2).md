1주차 과제 펜 만들기

 void setup(){
  size(500,500);
  stroke(0,0,255); //RGB
  strokeWeight(16); // 크기 16 
}
void draw(){
  if(mousePressed) // 마우스를 누를 시 작동
      line(pmouseX,pmouseY,mouseX,mouseY);  
}

2주차 과제 베너 만들기

void setup(){

size(500, 300); textSize(100);
}

int i, dir=1, sp=1;

void draw(){
fill(0); background(255,255,255); text("andong", i, 200);
if(i>width) dir=-1;
if(i<0) dir=1; i = i+dir*sp;
} 

void keyPressed(){
sp = key-'0';
}

3주차 과제 Examples 중에 하나를 선택해서 수정하기

float x;
float y;
void setup() {
  size(600, 600); 
  noStroke();  
}
void draw() { 
  background(0);
  x = lerp(x, mouseX, 0.1);
  y = lerp(y, mouseY, 0.1);
  
 fill(mouseX, mouseY, 255);
  stroke(200);
  ellipse(x, y, 30, 30);
}

4주차 과제 나의 도형 만들기

int a = 150;

int x1=a;    int y1=a;
int x2=a+30;  int y2=a+20;
int x3=a+80;  int y3=a+30;
int x4=a+130;  int y4=a+15;
int x5=a+170;  int y5=a-10;
int x6=a+190;  int y6=a-20;
int x7=a+180;  
int x8=a+20;  int y7=a-5;

 
size(640, 360);

noSmooth();
background(0);
translate(140, 0);

//Draw circle

stroke(255,255,255);

noFill();

ellipse(250,150,130,130);

// Draw white points

stroke(255);

point(x8, y7);
point(x1, y2);
point(x2, y3);
point(x3, y3);
point(x4, y4);
point(x5, y1);
point(x6, y5);
point(x7, y6);


//Draw line
stroke(153);

line(x8,y7,x1,y2);
line(x1,y2,x2,y3);
line(x2,y3,x3,y3);
line(x3,y3,x4,y4);
line(x4,y4,x5,y1);
line(x5,y1,x6,y5);
line(x6,y5,x7,y6);


//Draw star

point(20,50);
point(140,200);
point(80,100);
point(230,70);
point(120,80);
point(240,250);
point(210,300);
point(10,320);
point(320,350);

 5주차 과제 OpenGL PGraphics, PShape
 
 PGraphics pg;
void setup() {
  size(800, 800);
  pg = createGraphics(240, 240);

}

void draw() {

  pg.beginDraw();
  pg.background(100);
  pg.stroke(255);
  pg.line(220, 220, mouseX, mouseY);
  pg.endDraw();

  image(pg, 230, 380); 
  image(pg, 461, 380);

 
  rect(80,550,220,760);
  rect(580,550,220,760);
}




float x,y;

void setup(){
  size(500,500);

}

void draw() {
 background(51);

  x = lerp(x, mouseX, 0.1);
  y = lerp(y, mouseY, 0.1);

  translate(mouseX, mouseY);
  fill(mouseX, mouseY, 255);

  stroke(255);
  strokeWeight(3);
  beginShape();

  vertex(0, -50);
  vertex(14, -20);
  vertex(47, -15);
  vertex(23, 7);
  vertex(29, 40);
  vertex(0, 25);
  vertex(-29, 40);
  vertex(-23, 7);
  vertex(-47, -15);
  vertex(-14, -20);
  endShape(CLOSE);

}
