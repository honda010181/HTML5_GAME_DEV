var canvasBg = document.getElementById('canvasBg'); 
var ctxBg =canvasBg.getContext('2d');

var canvasJet = document.getElementById('canvasJet'); 
var ctxJet =canvasJet.getContext('2d');

var gameWidth = canvasBg.width;
var gameHeight = canvasBg.height;// forgot the h not H
var fps = 10 //how fast should the canvas be redrawn mili sec
var drawInterval;
var jet1;
var imgSprite = new Image();
imgSprite.src = 'sprite.png';
imgSprite.addEventListener('load',init,false);
function init()
{
	drawBg();
	startDrawing();
	jet1 = new Jet();
}
function draw(){
	//drawJet()
	jet1.draw();
}
function startDrawing(){
	stopDrawing();//stop the first draw before calling the second one
	drawInterval = setInterval(draw,fps);//fucntion name for first param, second is time
}
function stopDrawing(){
	clearInterval(drawInterval)
}


function Jet(){ //createing object
	this.srcX = 0;
	this.srcY=500;
	this.drawX = 220;
	this.drawY = 200;
	this.width = 100;
	this.height = 40; 
}
Jet.prototype.draw = function(){ //this function can be shared between all Jet objects
	clearCtxJet();
	ctxJet.drawImage(imgSprite,this.srcX,this.srcY,this.width,this.height,this.drawX,this.drawY,this.width,this.height);
};
/*
function drawJet()
{
	clearCtxJet();
	var srcX = 0;
	var srcY = 500;
	var drawX = 200;
	var drawY = 200;
	var width = 100;
	var height = 40;
	ctxJet.drawImage(imgSprite,srcX,srcY,width,height,drawX,drawY,width,height);
}
*/
function drawBg()
{
	var srcX = 0;
	var srcY = 0;
	var drawX = 0;
	var drawY = 0;
	ctxBg.drawImage(imgSprite,srcX,srcY,gameWidth,gameHeight,drawX,drawY,gameWidth,gameHeight);
}
function clearCtxBg(){
	ctxBg.clearRect(0,0,gameWidth,gameHeight)
}
function clearCtxJet(){
	ctxJet.clearRect(0,0,gameWidth,gameHeight)
}

