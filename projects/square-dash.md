---
layout: default
---

# Square Dash

## Step 1: Draw the background


---

## Step 2: Draw the player sprite


---

## Step 3: Draw a spike sprite


---

## Step 4: Position the player on the ground

```scratch
when green flag clicked
go to x: [-150] y: [-75]
```

---

## Step 5: Make the player jump

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

