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

For my second task, I followed the part of my plan as shown below (general). I would say that I am 30% done with my project. 

![load scene](/images/mvp1.png)

Below is a table I created to help me with cross things out of my plan in a more detailed format. 

![load scene](/images/sprites:scenes.png)

One of the section on my table is "sprites" which is describing the sprites I created myself. The other section is labeled "scenarios" that I searched for online, until I was happy with the scenes. Below is the story of the progress I've made so far:
* First, I began by creating a sketch of my sprites: How I wanted each sprite to look like? My inspiration was figurines I used to collect as a child called [shopkins](https://shopkinsgame.com). After much drawing, erasing, and using paper after paper, eventually I finalized my drawings. Here is my sketch:

![load sketch](/images/sketchmvp.png)

* Then, I continued on to making my idea come to life! However I ran into my first problem, I completely forgot that drawing online isn't as smooth as it is on paper. Therefore, I had to adjust some details, but was able to get the hang of it pretty quickly. Just when I was starting to feel better about drawing using pixels, I couldn't find the *return* button, so I had to restart each sprite at least twice. Luckily they turned out to be better than I expected! After, I searched for images for the background and through the process of elimination I chose my scenes. Finally, I began to implement my sprites (and scenes) onto my code, and through the process I discovered how to use debugging  on replit using this: 
```js 
// inspect mode 
debug.inspect = true;
```
### Results
Here is the [link]() to the final product for task 1 and below is an image of how my platformer game is looking so far!

![load platformgame1](/images/platformgame1.png)

[Previous](entry03.md) | [Next](entry05.md)

[Home](../README.md)
