# Entry 3
##### 2/13/23

### Context
In my previous blog entry, I learned about my tool "[Kaboom](https://kaboomjs.com)" by creating a running mini-game: [Pio](https://replit.com/@wendyb8188/Kaboom-Tinkeren#code/main.js).

### Task
My goal this time was to create a flying mini-game using [this](https://youtu.be/hgReGsh5xVU) tutorial on YouTube which is based on the viral flappy game!

### The Learning
Throughout the process of creating a flying mini-game, I came across many challenges which helped me learn about Kaboom. Here are a couple of challenges I faced and the outcomes of each of them:

* Challenge #1 
  * One common problem was that my sprites didn't correlate to my code, so whatever the man had in the video wasn't showing up on my side or didn't make sense for me to use. Below are two examples of this problem.
    * For the 1st piece of code, I was trying to load sprites, so that I could use it in the code. For the second one, I tried to position the new sprites on to the viewer's page. <br>
 
 1st Part
 ```js
// load assets- insert load code
loadSprite("heart", "sprites/heart.png");
loadSprite("sky", "sprites/sky.png");
loadSprite("cloud", "sprites/cloud.png");
```

2nd Part
```js
// add sprites on to webpage
    add([ // right-side up
      sprite("cloud"),
      pos(width() - 300, height()/2 + offset + PIPE_GAP/2),
    ]);

    add([ // upside-down cloud
      sprite("cloud", {flipY: true}),
      pos(width() - 300, height()/2 + offset - PIPE_GAP/2),
      origin("botleft"),
    ]);
 ```
 
![image](https://user-images.githubusercontent.com/91750546/221428702-87c7ec65-205b-4450-a0f7-500cd1022076.png)
 
* Outcome
  *  In the beginning of the tutorial, I realized that if I wanted to incorporate some of my ideas into the mini-game, I would have to do something different. That's when I decided to use sprites of my own choice: heart, clouds, blue sky. However in changing the sprites, I forgot that I would have to remember to tinker/adjust every time that the man did something with his sprites: bird, heart, land. For the 1st one, I was using .png for all of them, but since I had gotten an image from google, I needed to use jpg. For the second one, I tried using the code that was explained by the man in the video, but realized that mine were CLOUDS not PIPES, so I ended up fixing the name and instead of turning my second cloud upside down, I left it rightside up because it looked strange having a cloud one way and one the other way. <br>

1st Part
```js
// load assets- insert load code
loadSprite("heart", "sprites/heart.png");
loadSprite("sky", "sprites/sky.jpg");
loadSprite("cloud", "sprites/cloud.png");
```

2nd Part
```js
  add([ // top cloud
    sprite("cloud"),
    pos(width() - 300, height()/2 + CLOUD_GAP/2) // x: width of screen - (bigger # => left); y: (big # => lower down)
  ])

  add([ //btm cloud
    sprite("cloud"),
    pos(width() - 300, height()/2 - CLOUD_GAP/2) // x: width of screen - (bigger # => left); y: (big # => lower down)
  ])
```
 
![image](https://user-images.githubusercontent.com/91750546/221428818-7a8dcef5-b0a6-464d-8ab6-c619a25557c0.png)

 * Challenge #2 
  * I wanted to see "GAMEOVER!" like in the tutorial when my heart player collided with the cloud, but was seeing "gameover!" I tried to fix it by changing the `go`
 in `player.collides` from "gameover" to "GAMEOVER!" This led me to getting an error message which can be seen in the image below.
 
 ```js
player.collides("cloud", () =>{ // cloud is detected colliding with player
  go("GAMEOVER!")
  // debug.log('collided'); // show string when colliding 
});
...
scene("gameover", () =>{ //new scene called gameover
  add([
    text("gameover!")
  ])
})
 ```
 
 ![image](https://user-images.githubusercontent.com/91750546/221447695-1bbeccb3-1a0d-4601-90ee-40518bac01a2.png)

 * Outcome
  * I decided to tinker around with it, then changed it back to the way it was. After doing that, I realized that instead of changing what's inside `go`, I needed to change what was inside `text` which can be seen in the image below. The reason is that `go` is calling your scene by its name which I named "gameover", if I change it, then I'm calling a scene that doesn't exist. 
 
```js
player.collides("cloud", () =>{ // cloud is detected colliding with player
  go("gameover")
  // debug.log('collided'); // show string when colliding 
});
...
scene("gameover", () =>{ //new scene called gameover
  add([
    text("GAMEOVER!")
  ])
})
 ```
 
![image](https://user-images.githubusercontent.com/91750546/221447818-d2a8ccf2-75fa-4858-b2bc-86faae4634e0.png)
 
### Reflection
During this entire process, I faced challenges like shown above, some of them were easy to solve while others took more time and patience. Despite the challenges I faced, I came to the solutions and learned from them. I think that this game is my favorite so far, [here](https://replit.com/@wendyb8188/heart-cloud-sky?v=1) is the final product!

### Engineering Design Process
At the moment, I feel like I'm in two stages, "Research the problem" and "Create a prototype" as I am still learning about Kaboom by creating a mini-game through research on [YouTube](https://www.youtube.com/).

### Skills
I believe that I've worked on "How to learn" and "Debugging" skills. As I followed a tutorial and used some of my own ideas, I *learned* about kaboom. During the process of learning, I faced challenges in which I had to *debug* the problems to make my mini-game work the way I wanted to. 

### Next Steps
I feel more confident in my tool, and hope to learn how to make more mini-games in the future. I'm thinking about creating a ping-pong game or maybe a shooting game and want to figure out how to create sound. 

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
