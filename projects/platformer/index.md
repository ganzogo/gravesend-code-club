---
layout: default
---

<section markdown="1">

# Platformer

These steps are available at [bit.ly/platformer-steps](https://bit.ly/platformer-steps).

{% include scratch-embed.html id="1264077576" %}

---

</section>
<section markdown="1">

## Step 1: Open the starter project

-

---

* *Can you use a different sprite?*

</section>
<section markdown="1">

## Step 2: Add a variable called *jump speed*


-

---

</section>
<section markdown="1">

## Step 3: Make the character fall to the bottom of the screen

```scratch
when green flag clicked
set [jump speed v] to (0)
go to x: (0) y: (-100)
repeat until <touching color (#78cdee)?>
    change y by (jump speed)
    change [jump speed v] by (-1)
end
```

---

</section>
<section markdown="1">

## Step 4: Make the character stop falling when they hit the ground

```scratch
if <<touching color (#000000)?> and <(jump speed) < (0)>> then
    repeat until <not <touching color (#000000)?>>
        change y by (1)
    end
    set [jump speed v] to (0)
end
```

---

</section>
<section markdown="1">

## Step 5: Add a block to fix the weird animation!

```scratch
define put on ground
repeat until <not <touching color (#000000)?>>
    change y by (1)
end
set [jump speed v] to (0)

if <<touching color (#000000)?> and <(jump speed) < (0)>> then
    put on ground
end
```

---

</section>
<section markdown="1">

## Step 6: Add a variable called *on ground?*

We are going to add a variable called *on ground?*. This is going to be set to **1** if the character is on the ground or **0** if the character is jumping or falling.

After you set the *jump speed* at the start of the script, you also need to set *on ground?* like this:

```scratch
set [on ground? v] to (0)
```

And we need to update our custom block to set *on ground?* to **1**, like this:

```scratch
define put on ground
repeat until <not <touching color (#000000)?>>
    change y by (1)
end
set [jump speed v] to (0)
set [on ground? v] to (1)
```

---

</section>
<section markdown="1">

## Step 7: Make the character jump

```scratch
if <<key (up arrow v) pressed?> and <(on ground?) = (1)>> then
    set [on ground? v] to (0)
    set [jump speed v] to (10)
end
```

---

</section>
<section markdown="1">

## Step 8: Make the character move left and right

```scratch
if <key (left arrow v) pressed?> then
    change [run speed v] by (-2)
end
if <key (right arrow v) pressed?> then
    change [run speed v] by (2)
end
```

---

* *Can you make the character look to the left or right when they are moving?*

</section>
<section markdown="1">

## Step 9: Make the character slow down

Right now, the character slides left and right like they are on an ice rink. We need to add some friction to slow the character down! 

```scratch
set [run speed v] to ((run speed) * (0.7))
```

---

</section>
<section markdown="1">

## Step 10: Add some platforms

---

</section>
<section markdown="1">

## Challenges

* *-*

</section>