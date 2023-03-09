# Entry 3
##### 2/06/2023

I have been tinkering with my tool by fixing errors and adding new blocks and spikes to make my game more interesting and look like a real game. adding the new blocks was very difficult. The first error I encountered was them not loading into the game. This happened from a simple mistake: I didn't write the right path for the computer to go to get the images and add them to the game. The first problem was the image being too big for the game so you couldn't see the sprite being in the game because of the big blocks, the sprite would also just go right through the blocks. So I thought to myself and asked "how can I find the right proportions for the game to handle and for me to see my game character walk." then I came up with an idea. I download my game character and see how big it is. I then made all my blocks with the same height and width. This fixed my problem with some of the images. For some reason the images I downloaded I couldn't change the width and height so I got other images to fix that. After that, I had to fix the problem of my game character falling through my blocks. I went to the [kaboom website](https://kaboomjs.com/) and find what components I need for my game character not to fall through. I saw the component [``soild()``](https://kaboomjs.com/#solid) this makes objects sold and not make stuff fall right through. I also needed to add an area comp as well for it to work as it says on the website.

before
```js
"=": () => [
		sprite("grass"),
		area(),
	],
```
after
```js
"=": () => [
		sprite("grass"),
		area(),
		solid(),
```
This fixed my problem for my character falling through. In the engineering design process I am creating a prototype its very early to call this the final product the next step to so be on test and evaluate the prototype. The skill/skills I developed was how to read articles and growth mindset. I had to read the kaboom website to learn how to code with kaboom. I had  growth mindset because it took a lot of time and I didn't give up on fixing the problem and I failed multiple times.



[Previous](entry02.md) | [Next](entry04.md)

[Home](../README.md)
