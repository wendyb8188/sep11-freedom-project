# Entry 5
##### 4/23/23

### Context
In my previous entries, I created a [platformer mini-game](https://replit.com/@wendyb8188/Game-Scene-mini-game?v=1) and worked on making progress towards my Minimal Viable Product using [Kaboom](https://kaboomjs.com/). 

### Goal(s)
1) My first goal was to finish my MVP!!!
2) My second goal was to do learn more about Kaboom to go BEYOND MVP (later on) by doing researching 

### MVP + Challenge(s)
For my first goal, I had already started it and completed about 30% of it, so my task was to finish it and reach 100%. As a reminder the second part of my plan is the second bullet point:

![image](https://user-images.githubusercontent.com/91750546/235041139-758d5d35-78fa-46cd-ab14-d5a301cc3602.png)

Below is a list of ideas I used to finish my MVP:
![image](https://user-images.githubusercontent.com/91750546/235042090-6ae38eca-cd5b-4857-b1aa-1b21c939c4cc.png)

Here is how I tackled the bullets:
1) I ended up using the following code to identify each sprite. Let me explain using the comment numbers, the 0 is the symbol I selected which in this case is "@", the 1 is me selecting the chosen sprite called by its `id` which in this case is the watermelon sprite, the 2 is me giving the sprite the ability to collide with other objects/sprites, the 3 is me giving the sprite gravity, the 4 means that it is computer controlled, the 5 is giving the sprite a new name (nickname for code), and the 6 is me scaling the sprite (size). 
 ```js
        "@": () => [ // 0
            sprite("watermelon"), // 1
            area(), // 2
            body(), // 3
            origin("bot"), // 4
            "player", // 5
            scale(4.2), // 6
        ],

    
        "#": () => [
            sprite("basket"),
            area(),
            origin("bot"),
            "enemy",
            scale(.8),
        ],
        "=": () => [
            sprite("crate"),
            area(),
            solid(),
            origin("bot"),
            scale(1),
        ],
        "$": () => [
            sprite("heart"),
            area(),
            origin("bot"),
            "heart",
            scale(1),
        ],
        "*": () => [
            sprite("door"),
            area(),
            origin("bot"),
            "door",
            scale(1),
        ],
```
2) At the very start of the coding process, I realized and very happy I did, that if I wanted to create more levels on the game, I would have to make a flexible platform not just a flat-straight block as my background which I originally thought of doing. Therefore, I had to create a new sprite, below is the before and after. Notice how in the after image, I was able to add spaces in between crates. 
![load platformgame1](/images/platformgame1.png)
![image](https://user-images.githubusercontent.com/91750546/235047706-5125bd30-09ad-4583-a862-c202184bd0bc.png)
3) For the functionality of each sprite, I decided to keep it simple as it the MVP, so the baskets and the hearts also known as the enemies and prizes stayed still. Meanwhile the player, watermelon's goal was to collect the hearts and avoid the baskets (if it touches it, the player loses). 
4) For the length of the game, I chose to do three levels starting from easy going to medium than hard. Below is the map (code) for the levels along with the picture to go along side them. One of the challenges was testing the game out, as the creator I should know how to beat all three levels, but it took time, patience, and lots of adjusting before I was satisfied with the difficulty range. After I beat it, I needed to see if others could too, so I asked for help from my family and friends, and they gave me advice on ways to improve it. One of my favorite reactions came from my sister who said that "this is like one of those games that makes you want to throw the computer out the window" and from a friend's who said "this is rigged" (as they proceded to try over and over and over again). 
```js

const LEVELS  = [ // levels = 3 
    [
        "@ $#$  $#$  $#$ *", // sprites (watermelon = @, hearts = $, baskets = #)
        "==================", // ground level (crates)
    ],
    [
        "@  $#$  $  $#$ $ *",
        "=  ===  =  === =  ", 
    ],
    [
        "@  $#$  $    # $",
        "=  ===  =  =====",
        "                ",
        "$   $   $   $ *#",
        "======  =  === =",
    ],
]
```
![image](https://user-images.githubusercontent.com/91750546/235047639-e45fe508-0dce-4b99-acf8-a7de81da8826.png)
![image](https://user-images.githubusercontent.com/91750546/235047706-5125bd30-09ad-4583-a862-c202184bd0bc.png)
![image](https://user-images.githubusercontent.com/91750546/235047811-8f058ea9-74b6-4938-964b-ae7ea54e4d2b.png)

### *The Just About Final Learnings*
After I completed my MVP, I worked on my second goal, here are new things I learned from researching:
* Just like how I used `const SPEED = 480 // speed = player sprite`, You can use: 
  * ` const JUMP_FORCE = ...` to determine how much you want a sprite to jump (with what force)
  * ` const MOVE_SPEED = ...` instead of using just SPEED
* I am thinking on using these for going beyond MVP (increase difficulty). For example, instead of making my player go one speed or do a specific amount of height for jumping, I could change them, so that my player can go at a faster speed an jump over more obstacles (maybe bigger crates)!

### Engineering Design Process
As of right now, I feel like I am in two stages: "Create a Prototype" AND "Test and Evaluate the Prototype." As I *created* my projoct, I *tested* and *evaluated* it to have a platformer game by doing the least I can do to make it work.

### Skills
Through the process of bringing my game to life, I felt like I used the skills "Consideration" and "Growth Mindset." As I created my project, I tried my best to consider other peoples opinions about the game. Through my consideration, I worked on developing a *growth mindset* by being patient, preserving through challenges, and asking for help to make improvements. 

### The Results
After many entries speaking about a project using Kaboom, I finally created that long-awaited project... Here is the [link](https://replit.com/@wendyb8188/FreedomProject?v=1) to my MVP!!! :D 

### Next Steps
Implement my learnings to go beyond MVP or find out other ways to make my game more efficient and fun. Here are other ideas:
* Include audio by applying my learnings
* Make the crates (enemies)/hearts move slightly

[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)
