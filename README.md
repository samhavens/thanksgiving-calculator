# thanksgiving-calculator

## paul justison turkey planner 3000

a single-file, early-90s-style web page that tells you exactly when to do turkey things on thanksgiving.

you type in:

- turkey weight (lbs)  
- when you want to EAT

it spits out:

- a timestamped schedule (out of fridge, preheat, into oven, pull, carve, eat)  
- step-by-step directions that use those exact times  
- core numbers (cook time, rest time, etc.)

no build, no deps, no framework, no cloud, just vibes.

---

## files

- `turkey-planner.html` – the whole app in one file (html + css + js)

---

## how to use

1. download or copy `turkey-planner.html`.
2. open it in a browser (chrome, firefox, safari, even your nostalgia copy of netscape if it still runs).
3. enter:
   - **turkey weight (lbs)** – e.g. `16.7`
   - **time you want to eat** – e.g. `16:00` for 4pm
4. click **“calculate my turkey fate.”**
5. follow the schedule + directions:
   - it tells you when to take the bird out of the fridge,
   - when to preheat,
   - when to put it in,
   - when to pull and rest,
   - when to carve.

print the page or keep it open on a tablet/phone in the kitchen.

---

## cooking assumptions

these are baked into the math:

- oven temp: **325°f** the whole time  
- cook time: **15 minutes per pound** (rounded to nearest 5 minutes)  
- rest time: **75 minutes** (1 hour 15)  
- carving window: **15 minutes**  
- fridge-to-oven warmup: **120 minutes**  
- preheat time: **30 minutes**

the script then works backward from your desired meal time.

---

## customizing (if you want to tinker)

open `index.html`, find the `calculatePlan()` function, and tweak these constants:

```js
var cookMinutesRaw = weight * 15; // minutes per lb
var restMinutes = 75;
var carveMinutes = 15;
var preheatMinutes = 30;
var temperMinutes = 120;
```

change them if your oven runs hot, you like a longer rest, etc.
