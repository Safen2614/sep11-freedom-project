# Entry 2
##### 12/18/2022

I tinkered with my tool a lot within these past weeks. I followed this [GitHub](https://github.com/replit/kaboom) and I followed the "Start a Project With create-kaboom" I did it. Then I started to learn how to code from the original [kaboom website](https://kaboomjs.com)  I added movements and platforms and it worked! After I did that the next week I asked Mr. Mueller if it was ok to use this way of making my game. He said I should follow the CDN way. Now I gotta recode my game with the CDN way and not the way I followed. In the engineering design process, I'm in creating the prototype stage. The next stage of the engineering design process is to test and evaluate the prototype I need to fix infinite jump in my game somehow. The skills that I improved are growth mindset and how to google. I had to look for how to add kaboom to my ide and how to make a game with movement and jumping. I developed a growth mind set because I had to fix a lot of errors that didn't make sense to me and ask people around me for help or try to google it. What I want to do in the winter break is to somehow fix infinite jumping in my game.


What my code looks like right now

``` 
kaboom()


loadSprite("bean", "/sprites/bean.png")


const SPEED = 320

const player = add([
	sprite("bean"),
	pos(center()),
	body(),
	area(),
])

onKeyDown("left", () => {
	player.move(-SPEED, 0)
})

onKeyDown("right", () => {
	player.move(SPEED, 0)
})

onKeyDown("up", () => {
	player.move(0, -SPEED)
})

onKeyDown("down", () => {
	player.move(0, SPEED)
})


add([
	text("Press arrow keys", { width: width() / 2 }),
	pos(12, 12),
])
onKeyPress("space", () => {
	    player.jump()
	})
	add([
		rect(width(), 48),
		outline(4),
		area(),
		pos(0, height() - 48),
		solid(),
	])
	player.onUpdate(() => {
		camPos(player.pos)
	})
```

[Previous](entry01.md) | [Next](entry03.md)

[Home](../README.md)
