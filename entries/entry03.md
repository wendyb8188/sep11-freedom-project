# Entry 3
##### 2/13/23

### Context
In my previous blog entry, I learned about my tool "[Kaboom](https://kaboomjs.com)" by creating a running mini-game: [Pio](https://replit.com/@wendyb8188/Kaboom-Tinkeren#code/main.js).

### Task
My goal this time was to create a flying mini-game using [this](https://youtu.be/hgReGsh5xVU) tutorial on YouTube which is based on the viral flappy game!

### The Learning
Throughout the process of creating a flying mini-game, I came across many challenges which helped me learn about Kaboom. Here are a couple of challenges I faced and the outcomes of each of them:

* Challenge #1 
  * One common problem was that my sprites didn't correlate to my code, so whatever the man had in his video wasn't showing up on my side or didn't make sense for me to use. For the 1st piece of code, I was trying to load sprites, so that I could use it in the code. For the second one, I tried to position the new sprites on to the viewer's page. <br>
 
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

 * Challenge #2 (2012)
  * .
 
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
  * .
 
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

### Engineering Design Process

### Skills

### Next Steps: What you plan on learning next about your tool; be specific! 

[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
