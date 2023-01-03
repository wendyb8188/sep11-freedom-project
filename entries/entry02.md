# Entry 2: Kaboom Learning Introduction!
##### 12/19/2022

### Context
In my previous blog entry, I wrote about choosing a tool for my freedom project, I ended up electing [Kaboom](https://kaboomjs.com) which is a Javascript game programming library. Through the use of a website called [Replit](https://replit.com) which is used to create and share software, I learned about Kaboom.  

### Task
The task I gave myself was creating a mini-game that is similiar to the [dino game](https://kaboomjs.com) that appears when the internet goes out following [this](https://kaboomjs.com/doc/intro) tutorial on kaboom. 

### The Learning 
During this journey to create a running mini-game, I faced many struggles in which helped me learn about Kaboom. Here are some challenges in which I faced and what I learned from each challenge:

* Challenge #1
  * Right at the start of the process of creating my mini-game I ran into my first problem. I was supposed to be following a tutorial, but I ended up copying and pasting code without even knowing what it meant. Below is an example of code I copied and pasted:
```js
// initialize context
kaboom()

// load assets
loadSprite("bean", "sprites/bean.png")

// add something to screen
add([
// list of components
    sprite("bean"),
    pos(90, 40),
    scale(3),
    rotate(30),
])

// add a kaboom on mouse click
onClick(() => {
	addKaboom(mousePos())
})

// burp on "b"
onKeyPress("b", burp)
```

* Learning #1
 * Here is where I had my first Aha-moment. Instead of just copying and pasting, I began to tinker with each piece of code I didn't understand and commenting each line of code to fully grasp the function of the code. Below is an example of this along with a few tweaks. 

```js
// initialize context
kaboom()

// load a sprite "bean" from an image
loadSprite("bean", "sprites/bean.png")

// add- assembles parts and shows it on the screen
add(
  [sprite("bean"), // call bean
	pos(100, 80), // how far do you want bean from the left wall/right wall
  scale(2), // how big do you want bean?
  rotate(), // turn bean
  // area(), // check for collision
  // body(), // responds to gravity
  // color(500, 20, 0), // r,g,b
])
```

* Challenge #2
  * Towards the end of the tutorial there was less straightforward code and more instructions for me to read which made it harder for me. Below is an example of the type of code they gave us:

```js
// don't move these init / loader functions
kaboom()
loadSprite("bean", "sprites/bean.png");

scene("game", () => {
    // add bean
    // add platform
    // spawn trees
});

go("game")
``` 

* Learning #2
  * It took me longer to decipher the code out, but I believe it was all part of the process of learning. I ended up realizing that where it had comments I was supposed to paste the code I had before to the new piece of code and it was up to me to decide what needed changing and deleting. Below is the code I added and fixed:

```js
// gameover scene = bean hits tree
scene("game", () => {
  // add bean
  const bean = add(
    [sprite("bean"), // call bean
    pos(80, 40), // how far do you want bean from the left wall/right wall (x,y)
    area(), // check for collision with other characters
    body(), // responds to gravity
      // color(500, 20, 0), // 
    ])

  // add platform
  add([
    rect(width(), 48), // brings a rectangle that's assigned a width (width of the game) and a height (pixels)
    pos(0, height() - 48), // x:0 & y: place on top of platform  
    outline(4), // makes the black outline 4 pixels
    area(), // adds collider = platform
    solid(), // no object can pass through it
    color(127, 200, 255), // --> sky blue R-edG-reenB-lue 
  ])

  onKeyPress("space", () => {
    // .isGrounded() is provided by body()
    if (bean.isGrounded()) {
      // .jump() is provided by body()
      bean.jump()
    }
  })

  // spawn trees
  function spawnTree() {
    add([
      rect(48, rand(24, 64)), // assign different value to the tree's rect height  	
      area(),
      outline(4),
      pos(width(), height() - 48), //-->  () default orgin--> top left point of shape
      origin("botleft"), // defines orgin of positioning: bottom left point b/c we want it to be above the platform
      color(255, 180, 255),
      move(LEFT, 240), // moves to the beans left infinitely by 480 pixels per second
      "tree", // add a tag here = string
    ]);
    
    bean.onCollide("tree", () => {
      addKaboom(bean.pos);
      shake();
    });
    
    wait(rand(0.5, 1.5), () => {
      spawnTree();
    });
  }

  spawnTree(); //  call endlessly, with a random interval between 0.5 - 1.5 seconds each time
});
```

* Challenge #3
  * After finishing my code, I decided to go a even more beyond the Minimal Viable Product by making my own sprite which was something I wanted to do from the beginning. Instead of using "bean" which is shown below:

  * I created a little duck which was inspired by the duck you use for debugging things on your own. Here it is: 

  * After this, I needed to change the code to make my sprite show up instead of bean which is where I got an error saying that the sprite was not found. I wrote this code:

```js
// load a sprite "bean" from an image
loadSprite("pio", "sprites/pio.pedit")
```
* However, it didn't work and so I went to Google and found someone with the same problem. Here is the [link](https://replit.com/talk/ask/Kaboom-is-confusing/145958). Below is my solution, I had the right idea, but I was using the wrong "asset", instead of using "`loadSprite()`", I was supposed to use "`loadPedit()`"

```js
// load a sprite "pio" from an image
loadPedit("pio", "sprites/pio.pedit")
```

### Reflection
After much researching, struggling, and tinkering with code, I was able to get to the final product. Here are is the [final-result](https://replit.com/@wendyb8188/Kaboom-Tinkeren?v=1). I learned that learning this year's tool wasn't going to be as easy as the tool I learned in 10th grade. 

### Engineering Design Process 


### Skills

### Next Steps: 
For winter break, I wish to learn more about my tool through creating other mini-games by following tutorials and answering questions I have as I am learning about Kaboom.  


[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
