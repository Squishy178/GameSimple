# GameSimple
A Javascript library containing super easy to use assets for Making games, making use of Canvas. 

What is Game Simple? Game simple is a very easy to use Javascript engine, which allows for easy creation of any Web based Video Games, Assuming you have Javascript knowledge


This here is documentation for each function. Thanks for reading

_________________________________________________________________________________________________________________________________________________________________________________

CURSOR/MOUSE

___________________________________________________________________________________________________________________________________________________________________

**Game.mouse.x   (NUMBER)**
This tracks the mouse x position relative to the webpage. 

**Game.mouse.y   (NUMBER)**
This tracks the mouse y position relative to the webpage

**Game.mouse.down   (BOOL)**
Detects if the mouse is held down or not.

**Game.mouse.click   (BOOL)**
Single frame, once the mouse is pressed initially

**Game.mouse.release   (BOOL)**
Single frame, once the mouse is released. Slightly inconsistent

**Game.mouse.movementX   (NUMBER)**
The x distance from the position of the last frame, and the current position

**Game.mouse.movementY   (NUMBER)**
The y distance from the position of the last frame, and the current position

**Game.mouse.previousX   (NUMBER)**
The previous mouse x position last time it was moved

**Game.mouse.previousY   (NUMBER)**
The previous mouse y position last time it was moved

**Game.mouse.clickArea(x, y, sx, sy)   (BOOLEAN)**
Returns if the mouse clicks in the area (x, y, x+sx, y+sy). Useful for UI and Buttons

_________________________________________________________________________________________________________________________________________________________________________________

CANVAS

___________________________________________________________________________________________________________________________________________________________________
**Whenever c is referenced as a parameter, use the Canvas CTX.**
Global refers to the canvas, relative to the camera location. Local is the canvas, excluding the camera. Good for UI work.

**Game.canvas.(global or local).image(c, x, y, sx, sy, rotation)   (FUNCTION)**
Draws an image at (x, y) with the size of (sx, sy) with a rotation (rotation) with ctx of c


_________________________________________________________________________________________________________________________________________________________________________________

COLLISION DETECTION

___________________________________________________________________________________________________________________________________________________________________

**Game.collide.rect2D(x1, y1, sx1, sy1, x2, y2, sx2, sy2)   (BOOLEAN)**
Detects collision between 2 rectangles! Detects if the rectangle at (x1, y1) with a size of (sx1, sy1) is colliding with a rectangle at (x2, y2) with a size of (sx2, sy2)

**Game.collide.circle2D(x1, y1, rad1, x2, y2, rad2)   (BOOLEAN)**
Detects collision between 2 circles! Detects if a circle at (x1, y1) with a radius of rad1 is colliding with a circle at (x2, y2) with a radius of rad2
	
_________________________________________________________________________________________________________________________________________________________________________________

KEYS

___________________________________________________________________________________________________________________________________________________________________
When referencing a KEY, use a string in all Caps, example 'D'

Some other important keys to reference are..
SHIFT, ENTER, ESCAPE, LEFT, RIGHT, UP, DOWN, ALT, BACKSPACE, TAB, F1, F2, F3... F12, SPACE, and CONTROL
I would not use control or most of the F's however, as this may accidentally trigger web based commands


**Game.key.pressed(keyName)   (BOOLEAN)**
Detects if the key keyName is being pressed on the keyboard. Note that the keyName parameter is string, and has to be in all caps. 
Returns a Boolean

**Game.key.released(keyName)   (BOOLEAN)**
Detects if the key keyName is being released on the keyboard. Note that the keyName parameter is string, and has to be in all caps. This only outputs true for a single frame.
Returns a Boolean

**Game.key.click(keyName)   (BOOLEAN)**
Detects if the key keyName is being pressed on the keyboard, but only the intial moment. Note that the keyName parameter is string, and has to be in all caps. This only outputs true for a single frame.
Returns a Boolean


_________________________________________________________________________________________________________________________________________________________________________________

MISC

___________________________________________________________________________________________________________________________________________________________________

**Game.chance(percent)   (BOOLEAN)**
Returns a Boolean is randomized, the chance of true being displayed via the percent.

**Game.randomInt(min,max)   (BOOLEAN)**
Returns a random number between min and max.

**Game.randomDirection()   (NUMBER)**
Returns a random direction in RADIANS

**Game.quarterTurn   (NUMBER)**
Returns PI / 2. (A quarter of a rotation in radians. Neat CONSTANT to have)

**Game.directionFrom(x1, y1, x2, y2)   (NUMBER)**
Returns the direction from the point (x1, y1) to (x2, y2)

**Game.camera   (OBJECT)**
The CAMERA object is a pre-constructed variable, in which can be accessed and utilized well. Its subvariables are X, Y. Zooming and Roll are planned for later
Globally rendered objects will have the camera offset applied. 

**Game.globalPos2Dx (x)  (NUMBER)**
This converts the x position given into where It would be placed on the canvas

**Game.globalPos2Dy (y)  (NUMBER)**
This converts the y position given into where It would be placed on the canvas

___________________________________________________________________________________________________________________________________________________________________

SAMPLES

___________________________________________________________________________________________________________________________________________________________________
These functions are for those who honestly do not know what they are doing, or are just lazy. These are the only functions I would NOT recomend using, however they are here to make your life easier if you so want it. More will be added to this later

**Game.sample.cameraSmooth2D(x, y, ease)   (FUNCTION)**
This eases the cameras current position to the provided (x, y). The speed is dictated by the provided "ease" prompt. If you would like the camera to be CENTERED on the camera, add half the canvas width to the x, and half the canvas height to the y
