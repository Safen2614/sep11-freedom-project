# Entry 5
##### 4/19/2023

## The Challenges

The DOMS project was very difficult project for me to do. the first part was making the game first.

## Part 1 making the game

This part wasn't too bad because of the documentation of kaboom. I had to first add multiple levels to my game. To do this I have to make symbols to means to make the map of the level. For example

```js
 [
                "                *    *       $",
                "    *                        $",
                "                           $",
                "                       =    $",
                "                  =    =   $",
                "           $$     =    =    $",
                "       ====       ===    = $" ,
                "         *              =    $",
                "                      =       ",
                "       ^^     =      =  >       =",
                "===========================     =",
                "=             =                 =  ",
                "=             =                 =",
                "=             =          =      =  ",
                "=             =          =      = ",
                "= @   >     =          =        =",
                "============    ================",
                "            $$$                       ",
                "            ====                   ",

            ],

```
all of these symbols means something and to define these symbols you have `tileWidth: 64, tileHeight: 64, tiles: {}` you then for example
```js
"=": () => [
			sprite("grass"),
			area(),
			body({ isStatic: true }),
			anchor("bot"),
			offscreen({ hide: true }),
			"platform",
		],
```
you add the sprite name you wanted to to load each time you add it to the map. `area()` give like collision detection and so my player won't fall through the block. The `body({ isStatic: true })` makes it so the block won't move. `offscreen()` allows you to control what the object does when it reaches the end of the screen. After we named all the objects we needed the plan now is to make the level itself.

```js
[	"  ====               ",
	    "          *           ",
	    "                   ",
	    "   *                ",
		"         *   ",
		"  *         ",
		"                    ",
		"       $$    *   ",
		"     ===           ",
		"                    ",
		"   ^^  > = @  ",
		"============  ",
	]
```

This is one of our levels. When I started to play the level though I wanted the camera to follow my player instead of just the whole screen because my player would be out of my veiw. So I went back to Kabooms website and made this.

```js
player.onUpdate(() => {
		camPos(player.pos)
	})
```
I learned that `.onUpdate` is used to lets say you wanted to change the color of something every frame then you add the name of the object and then `.onUpdate` and add an action or an event and it will run every frame.


### How I added a portel and make it change the level

this was the hardest part of my MVP. What I did was go to the Kaboom wesbite and I remember that it showed us how to use `scene()` to make the game and switch the levels. So then I learned how to use it but there was this one error that I cound't fix. For 2 hours I've been just reading the code commenting out, see maybe this was the error. The error was when I die then respond I coudn't move it would keep putting me back the the starting position. Then for a while I was thinking. On the last few peices of code it's this.


``` js
scene("lose", () => {
	add([
		text("You Lose"),
	])
	onKeyPress(() => go("game"))
})

scene("win", () => {
	add([
		text("You Win"),
	])
	onKeyPress(() => go("game"))
})

go("game")
```
now I thought "ok each time I lose, when I press my key it would restart the game. So I went back to Kaboom and trying to see if I can replace it with something else. I found `onMousePress()` so then I just replaces that with `onMousePress()`.









[Previous](entry04.md) | [Next](entry06.md)

[Home](../README.md)