---
layout: default
---

# Square Dash

## Step 1: Draw the background

![Step 1 - Draw background](img/step-01-01.png)

---

## Step 2: Draw the player sprite

![Step 2 - Draw player](img/step-02-01.png)

---

## Step 3: Position the player on the ground

```scratch
when green flag clicked
go to x: [-150] y: [-75]
```

---

## Step 4: Make the player jump

Add a forever loop

```scratch
when green flag clicked
go to x: [-150] y: [-75]
forever
    if <key (space v) pressed?> then
        repeat (12)
            change y by (10)
        end
        repeat (12)
            change y by (-10)
        end
    end
end
```

* Can you make the player spin do a backflip when they jump?

---

## Step 5: Draw an obstacle sprite

![Step 5 - Draw obstacle](img/step-05-01.png)

---

## Step 6: Create a clone

```scratch
when green flag clicked
hide
forever
    create clone of (myself v)
    wait (2) seconds
end

when I start as a clone
go to x: (240) y: (-100)
show
repeat until <(x position) < (-240)>
    change x by (-10)
end
hide
```


## Step 7: End the game when the player hits the obstacle

```scratch
when I start as a clone
go to x: (240) y: (-100)
show
repeat until <(x position) < (-240)>
    change x by (-10)
    if <touching (player v)?> then
        broadcast (game over v)
    end
end
hide
```

## Step 8: Create a game over sprite

![Step 8 - Draw game over](img/step-08-01.png)

## Step 9: Display the game over sprite

```scratch
when green flag clicked
go to x: (0) y: (36)
hide
```

```scratch
when I receive [game over v]
show
stop [all v]
```

## Challenges

* High score
* Change the background colour
* Add levels and make the game get faster with each level
* Add rocket level
* Add sound effects
* Add background music
* Different obstacle sizes
* Obstacles more often
* Different types of obstacles
* Make the obstacles spin
* Make the obstacles move up and down
* Add lives
* Choose player avatar
* Animate the player (e.g. make it blink)
