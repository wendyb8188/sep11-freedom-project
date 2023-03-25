# Entry 4
##### 3/25/23

### Context
Previously, I learned about my tool "Kaboom" by creating a flying mini-game using a YouTube Tutorial. 

### Tasks
This time I had two tasks: 
1) Create a platformer mini-game using [this](https://kaboomjs.com/doc/21-scenes) tutorial on Kaboom.js that requires the usage of scenes 
2) Begin making progress for my Minimal Viable Plan through the creation of sprites, selection of scenes (prior to knowledge thus far: scene game tutorial), and application on code 

### The Learning 
While creating the platformer mini-game there were moments where I was confused, but mananged to discover the answers to my questions which helped me get a better understanding of Kaboom and its functions. Here are a couple of discoveries I faced and how I learned from them:

* Discovery #1
  * In blog 3 I wanted to figure out how to create sound, I ended up unexpectedly learning about it through the process of creating this mini-game. 
    * How did I arrive at this discovery? Well in the beginning, I was asked to load the sprites, then assign the loaded sprites to the different symbols on the "map," and create collisions between the player and coins/spikes. When I tried to run the code, it gave me an error message that said "Failed to load (image)" and "Failed to fetch (sound)" as shown below. From previous challenges I knew how to load images, so I assumed that for sounds it would be a similar process and I was right.  
 
![load img](/images/img.png)
![load sound](/images/sound.png)

* Discovery #2
 * I learned that every time you create a scene you need to close the brackets!!! When you think of a scene, it's like changing a background, you can't have two backgrounds in one scene. I learned this from a mistake with brackets placement where I was receiving the message as shown below. I had forgotten the main scene (setup of the game displayed while player is playing) end brackets which I didn't find, until I spent a solid fifteen minutes looking for the open and close brackets for each piece of code (`})`). 
 
![load scene](/images/scene.png)





[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
