const COLOR = ["#ecd6c4", "#d9bba3"];
const particles = []; 
const shapeList = [];

let oneDegree;

function setup() {
  createCanvas(windowWidth, windowHeight);
  background(0);

  oneDegree = (2 * PI) / 360;

  for (let i = 100; i < width - 200; i += 10) {
    let p = new Particle(i, 100);
    particles.push(p);
  }


  for (let i = 0; i < 40; i++) {
    shapeList.push(
      new MyShape({
        type: "rect",
        x: random(width),
        y: random(height),
        w: random(50, 80),
        h: random(50, 80),
        color: random(COLOR),
        alpha: 10,
        angle: 0,
        distance: 50,
      })
    );
  }
}

function draw() {
  if (frameCount < 700) {
    for (let p of particles) {
      p.update();
      p.display();
    }
  }
  if (frameCount == 700) {
    background(0);
  }
  if (frameCount > 700) {
    drawWomen();
    for (let s of shapeList) {
      s.display();
      s.forward(random(20));
      s.rotate(random(100));
    }
  }
}

function drawWomen() {
  const xRatio = 1680 / 3000;
  const yRatio = 1050 / 2400;
  push();
  translate(width / 2 - 1200 * xRatio, 0);

  beginShape();
  fill("#FFE7CF"); //skin
  vertex(1017 * xRatio, 0 * yRatio);
  vertex(1026 * xRatio, 55 * yRatio);
  vertex(990 * xRatio, 81 * yRatio);
  vertex(990 * xRatio, 118 * yRatio);
  vertex(935 * xRatio, 181 * yRatio);
  vertex(935 * xRatio, 235 * yRatio);
  vertex(872 * xRatio, 409 * yRatio);
  vertex(983 * xRatio, 650 * yRatio);
  vertex(1053 * xRatio, 767 * yRatio);
  vertex(1080 * xRatio, 857 * yRatio);
  vertex(1142 * xRatio, 979 * yRatio);
  vertex(1108 * xRatio, 1225 * yRatio);
  vertex(1084 * xRatio, 1404 * yRatio);
  vertex(931 * xRatio, 1690 * yRatio);
  vertex(638 * xRatio, 1731 * yRatio);
  vertex(512 * xRatio, 1823 * yRatio);
  vertex(472 * xRatio, 1909 * yRatio);
  vertex(573 * xRatio, 1966 * yRatio);
  vertex(807 * xRatio, 2009 * yRatio);
  vertex(1041 * xRatio, 1984 * yRatio);
  vertex(1128 * xRatio, 1932 * yRatio);
  vertex(1174 * xRatio, 1962 * yRatio);
  vertex(1219 * xRatio, 1945 * yRatio);
  vertex(1237 * xRatio, 1967 * yRatio);
  vertex(1368 * xRatio, 1949 * yRatio);
  vertex(1392 * xRatio, 1794 * yRatio);
  vertex(1407 * xRatio, 1692 * yRatio);
  vertex(1467 * xRatio, 1695 * yRatio);
  vertex(1373 * xRatio, 960 * yRatio);
  vertex(1411 * xRatio, 811 * yRatio);
  vertex(1448 * xRatio, 650 * yRatio);
  vertex(1410 * xRatio, 515 * yRatio);
  vertex(1353 * xRatio, 361 * yRatio);
  vertex(1353 * xRatio, 121 * yRatio);
  vertex(1284 * xRatio, 95 * yRatio);
  vertex(1266 * xRatio, 63 * yRatio);
  vertex(1284 * xRatio, 35 * yRatio);
  vertex(1262 * xRatio, 17 * yRatio);
  vertex(1274 * xRatio, 0 * yRatio);
  endShape(CLOSE);
  



  

  beginShape();
  fill(255); //dress
  vertex(1069 * xRatio, 569 * yRatio);
  vertex(1053 * xRatio, 767 * yRatio);
  vertex(1142 * xRatio, 979 * yRatio);
  vertex(1142 * xRatio, 979 * yRatio);
  vertex(1108 * xRatio, 1225 * yRatio);
  vertex(1084 * xRatio, 1404 * yRatio);
  vertex(931 * xRatio, 1690 * yRatio);
  vertex(638 * xRatio, 1731 * yRatio);
  vertex(512 * xRatio, 1823 * yRatio);
  vertex(472 * xRatio, 1909 * yRatio);
  vertex(573 * xRatio, 1966 * yRatio);
  vertex(807 * xRatio, 2009 * yRatio);
  vertex(1041 * xRatio, 1984 * yRatio);
  vertex(1128 * xRatio, 1932 * yRatio);
  vertex(1174 * xRatio, 1962 * yRatio);
  vertex(1219 * xRatio, 1945 * yRatio);
  vertex(1237 * xRatio, 1967 * yRatio);
  vertex(1368 * xRatio, 1949 * yRatio);
  vertex(1392 * xRatio, 1794 * yRatio);
  vertex(1407 * xRatio, 1692 * yRatio);
  vertex(1467 * xRatio, 1695 * yRatio);
  vertex(1373 * xRatio, 960 * yRatio);
  vertex(1406 * xRatio, 834 * yRatio);
  vertex(1349 * xRatio, 755 * yRatio);
  vertex(1375 * xRatio, 617 * yRatio);
  vertex(1321 * xRatio, 506 * yRatio);
  vertex(1171 * xRatio, 521 * yRatio);
  endShape(CLOSE);

  beginShape();
  vertex(955 * xRatio, 158 * yRatio);
  vertex(990 * xRatio, 118 * yRatio);
  vertex(1026 * xRatio, 398 * yRatio);
  vertex(984 * xRatio, 329 * yRatio);
  endShape(CLOSE);
  
  
  beginShape();
  fill('#B39C89');
  vertex(991 * xRatio, 118 * yRatio);
  vertex(964 * xRatio, 209 * yRatio);
  vertex(984 * xRatio, 329 * yRatio);
  vertex(1026 * xRatio, 398 * yRatio);
  vertex(990 * xRatio, 118 * yRatio);
  vertex(955 * xRatio, 158 * yRatio);
  endShape(CLOSE);

  beginShape();
  fill(255);
  vertex(1247 * xRatio, 95 * yRatio);
  vertex(1284 * xRatio, 95 * yRatio);
  vertex(1260 * xRatio, 258 * yRatio);
  vertex(1272 * xRatio, 294 * yRatio);
  vertex(1272 * xRatio, 355 * yRatio);
  vertex(1230 * xRatio, 292 * yRatio);
  vertex(1230 * xRatio, 197 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill('#B39C89');
  vertex(1247 * xRatio, 95 * yRatio);
  vertex(1230 * xRatio, 197 * yRatio);
  vertex(1272 * xRatio, 355 * yRatio);
  vertex(1272 * xRatio, 294 * yRatio);
  vertex(1260 * xRatio, 258 * yRatio);
  vertex(1272 * xRatio, 95 * yRatio);
  endShape(CLOSE);

  beginShape();
  fill("#FFC933"); //decoration
  vertex(1060 * xRatio, 472 * yRatio);
  vertex(1158 * xRatio, 491 * yRatio);
  vertex(1288 * xRatio, 413 * yRatio);
  vertex(1321 * xRatio, 506 * yRatio);
  vertex(1171 * xRatio, 521 * yRatio);
  vertex(1069 * xRatio, 569 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#E0AA22"); 
  vertex(1060 * xRatio, 472 * yRatio);
  vertex(1145 * xRatio, 506 * yRatio);
  vertex(1069 * xRatio, 569 * yRatio);
  vertex(1171 * xRatio, 521 * yRatio);
  vertex(1321 * xRatio, 506 * yRatio);
  vertex(1288 * xRatio, 413 * yRatio);
  vertex(1158 * xRatio, 491 * yRatio);
  vertex(1060 * xRatio, 472 * yRatio);
  endShape(CLOSE);
  
    beginShape();
  fill("#FFC933"); 
  vertex(1174 * xRatio, 498 * yRatio);
  vertex(1321 * xRatio, 506 * yRatio);
  vertex(1288 * xRatio, 413 * yRatio);
  endShape(CLOSE);

  beginShape();
  fill("#A58E5A"); //hair
  vertex(1017 * xRatio, 0 * yRatio);
  vertex(1026 * xRatio, 55 * yRatio);
  vertex(990 * xRatio, 81 * yRatio);
  vertex(990 * xRatio, 118 * yRatio);
  vertex(1004 * xRatio, 233 * yRatio);
  vertex(1044 * xRatio, 290 * yRatio);
  vertex(1083 * xRatio, 290 * yRatio);
  vertex(1123 * xRatio, 274 * yRatio);
  vertex(1139 * xRatio, 346 * yRatio);
  vertex(1176 * xRatio, 325 * yRatio);
  vertex(1182 * xRatio, 286 * yRatio);
  vertex(1215 * xRatio, 292 * yRatio);
  vertex(1230 * xRatio, 258 * yRatio);
  vertex(1230 * xRatio, 197 * yRatio);
  vertex(1247 * xRatio, 95 * yRatio);
  vertex(1284 * xRatio, 95 * yRatio);
  vertex(1266 * xRatio, 63 * yRatio);
  vertex(1284 * xRatio, 35 * yRatio);
  vertex(1262 * xRatio, 17 * yRatio);
  vertex(1274 * xRatio, 0 * yRatio);
  endShape(CLOSE);

  beginShape(); //hair shadow
  fill("#826C45");
  vertex(1065 * xRatio, 7 * yRatio);
  vertex(1043 * xRatio, 95 * yRatio);
  vertex(1075 * xRatio, 277 * yRatio);
  vertex(1060 * xRatio, 95 * yRatio);
  vertex(1075 * xRatio, 75 * yRatio);
  endShape(CLOSE);

  beginShape();
  vertex(1125 * xRatio, 165 * yRatio);
  vertex(1103 * xRatio, 225 * yRatio);
  vertex(1111 * xRatio, 264 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  vertex(1230 * xRatio, 77 * yRatio);
  vertex(1191 * xRatio, 180 * yRatio);
  vertex(1200 * xRatio, 272 * yRatio);
  vertex(1200 * xRatio, 210 * yRatio);
  vertex(1215 * xRatio, 173 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill('#634D27');
  vertex(1191 * xRatio, 13 * yRatio);
  vertex(1130 * xRatio, 114 * yRatio);
  vertex(1145 * xRatio, 185 * yRatio);
  vertex(1150 * xRatio, 316 * yRatio);
  vertex(1171 * xRatio, 214 * yRatio);
  vertex(1156 * xRatio, 102 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill('#BFAD88');
  vertex(1026 * xRatio, 173 * yRatio);
  vertex(1010 * xRatio, 215 * yRatio);
  vertex(1035 * xRatio, 277 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  vertex(1257 * xRatio, 7 * yRatio);
  vertex(1230 * xRatio, 42 * yRatio);
  vertex(1257 * xRatio, 77 * yRatio);
  vertex(1257 * xRatio, 51 * yRatio);
  vertex(1245 * xRatio, 31 * yRatio);
  endShape(CLOSE);


  beginShape();
  // fill("#B72323");
  vertex(984 * xRatio, 329 * yRatio);
  vertex(1042 * xRatio, 425 * yRatio);
  vertex(1060 * xRatio, 551 * yRatio);
  vertex(1042 * xRatio, 635 * yRatio);
  vertex(944 * xRatio, 406 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#60432A"); //skin shadow
  vertex(1045 * xRatio, 290 * yRatio);
  vertex(1048 * xRatio, 290 * yRatio);
  vertex(1124 * xRatio, 274 * yRatio);
  vertex(1140 * xRatio, 346 * yRatio);
  vertex(1114 * xRatio, 322 * yRatio);
  vertex(1078 * xRatio, 322 * yRatio);
  vertex(1045 * xRatio, 290 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#DAAD87"); //skin shadow
  vertex(1060 * xRatio, 472 * yRatio);
  vertex(1138 * xRatio, 472 * yRatio);
  vertex(1120 * xRatio, 392 * yRatio);
  vertex(1160 * xRatio, 466 * yRatio);
  vertex(1266 * xRatio, 409 * yRatio);
  vertex(1259 * xRatio, 335 * yRatio);
  vertex(1272 * xRatio, 355 * yRatio);
  vertex(1272 * xRatio, 375 * yRatio);
  vertex(1288 * xRatio, 413 * yRatio);
  vertex(1158 * xRatio, 491 * yRatio);
  vertex(1060 * xRatio, 472 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#D3D3D3"); //dress decoration
  vertex(1089 * xRatio, 560 * yRatio);
  vertex(1140 * xRatio, 535 * yRatio);
  vertex(1169 * xRatio, 560 * yRatio);
  vertex(1202 * xRatio, 518 * yRatio);
  vertex(1280 * xRatio, 510 * yRatio);
  vertex(1191 * xRatio, 612 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#C9C9C9"); //dress decoration
  vertex(1058 * xRatio, 707 * yRatio);
  vertex(1191 * xRatio, 635 * yRatio);
  vertex(1375 * xRatio, 617 * yRatio);
  vertex(1368 * xRatio, 655 * yRatio);
  vertex(1200 * xRatio, 662 * yRatio);
  vertex(1055 * xRatio, 748 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#C9C9C9"); //dress decoration
  vertex(1058 * xRatio, 707 * yRatio);
  vertex(1191 * xRatio, 635 * yRatio);
  vertex(1375 * xRatio, 617 * yRatio);
  vertex(1368 * xRatio, 655 * yRatio);
  vertex(1200 * xRatio, 662 * yRatio);
  vertex(1055 * xRatio, 748 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#C9C9C9"); //shadow
  vertex(1078 * xRatio, 778 * yRatio);
  vertex(1185 * xRatio, 702 * yRatio);
  vertex(1209 * xRatio, 804 * yRatio);
  vertex(1160 * xRatio, 982 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#E8E7E7"); //shadow
  vertex(1215 * xRatio, 709 * yRatio);
  vertex(1237 * xRatio, 682 * yRatio);
  vertex(1294 * xRatio, 718 * yRatio);
  vertex(1392 * xRatio, 833 * yRatio);
  vertex(1357 * xRatio, 945 * yRatio);
  vertex(1357 * xRatio, 1046 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#E8E7E7"); //shadow
  vertex(1160 * xRatio, 1022 * yRatio);
  vertex(1200 * xRatio, 1083 * yRatio);
  vertex(1144 * xRatio, 1258 * yRatio);
  vertex(1160 * xRatio, 1022 * yRatio);
  endShape(CLOSE);

  beginShape();
  vertex(1209 * xRatio, 1107 * yRatio);
  vertex(1015 * xRatio, 1827 * yRatio);
  vertex(1170 * xRatio, 1468 * yRatio);
  vertex(1209 * xRatio, 1107 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  vertex(1310 * xRatio, 1107 * yRatio);
  vertex(1327 * xRatio, 1788 * yRatio);
  vertex(1382 * xRatio, 1635 * yRatio);
  vertex(1357 * xRatio, 1366 * yRatio);
  vertex(1327 * xRatio, 1268 * yRatio);
  vertex(1310 * xRatio, 1107 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill('#B5B5B5');
  vertex(1397 * xRatio, 1627 * yRatio);
  vertex(1413 * xRatio, 1672 * yRatio);
  vertex(1467 * xRatio, 1695 * yRatio);
  vertex(1407 * xRatio, 1692 * yRatio);
  vertex(1392 * xRatio, 1794 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill('#B5B5B5');
  vertex(1041 * xRatio, 1984 * yRatio);
  vertex(1128 * xRatio, 1932 * yRatio);
  vertex(1174 * xRatio, 1962 * yRatio);
  vertex(1219 * xRatio, 1945 * yRatio);
  vertex(1237 * xRatio, 1967 * yRatio);
  vertex(1209 * xRatio, 1959 * yRatio);
  vertex(1168 * xRatio, 1975 * yRatio);
  vertex(1112 * xRatio, 1967 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#DAAD87");
  vertex(955 * xRatio, 158 * yRatio);
  vertex(935 * xRatio, 181 * yRatio);
  vertex(935 * xRatio, 235 * yRatio);
  vertex(872 * xRatio, 409 * yRatio);
  vertex(944 * xRatio, 255 * yRatio);
  vertex(944 * xRatio, 185 * yRatio);
  endShape(CLOSE);
  
  beginShape();
  fill("#DAAD87");
  vertex(1285 * xRatio, 95 * yRatio);
  vertex(1353 * xRatio, 121 * yRatio);
  vertex(1353 * xRatio, 361 * yRatio);
  vertex(1335 * xRatio, 142 * yRatio);
  endShape(CLOSE);
  pop();
}

class Particle {
  constructor(x, y, c) {
    this.x = x;
    this.y = y;
    this.c = random(COLOR);
  }

  update() {
    this.x += sin(this.x * 10);
    this.y += noise(this.x / 200, this.y / 200, 10000) * 3;
  }

  display() {
    push();
    noStroke();
    fill(this.c);
    if (random() > 0.96) {
      ellipse(this.x, this.y, 10);
    } else {
      ellipse(this.x, this.y, 2);
    }
    pop();
  }
}


class MyShape {
  constructor(cfg) {
    this.type = cfg.type;
    this.x = cfg.x; // x-coordinate
    this.y = cfg.y; // y-coordinate
    this.w = cfg.w; // width
    this.h = cfg.h; // height
    this.r = cfg.r; // radius
    this.alpha = cfg.alpha; // transparency
    this.color = cfg.color; // color
    this.angle = cfg.angle; // angle
    this.distance = cfg.distance; // distance
  }


  rotate(a) {
    this.angle += a;
  }


  forward(d) {
    this.distance = d;
    let cx = this.distance * cos(this.angle * oneDegree); 
    let cy = this.distance * sin(this.angle * oneDegree); 
    this.x += cx;
    this.y += cy;
  }

  display() {    
    if (this.type === "circle") {
      this.displayCircular();
    } else {
      this.displayRect();
    }
  }


  displayCircular() {
    noStroke();
    const c = color(this.color);
    c.setAlpha(this.alpha);
    fill(c);
    ellipse(this.x, this.y, this.r);
  }


  displayRect() {
    noStroke();
    const c = color(this.color);
    c.setAlpha(this.alpha);
    fill(c);
    rect(this.x, this.y, this.w, this.h);
  }
}
