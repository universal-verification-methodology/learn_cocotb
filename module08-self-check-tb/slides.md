---
marp: true
title: Self-check pattern
paginate: true
---

# Self-check pattern

Before scoreboards and agents, every testbench needs a self-check loop

---

## Stimulus, expect, compare
- Starter: a two-input AND gate with a equals one and b equals one
- The expect comes from the AND truth table, not from copying the DUT output back
- Change one input and recompute expect before you compare
- Wrong expect on purpose should fail so you practice the error path
- Compare after the signal settles, not mid-transition

---

## Browser lab
![Browser lab starter](assets/lab-starter.png)

---

## Real cocotb practice
- In the real cocotb track, restate the loop on paper before you write a live assert
- Draw four boxes: stimulus, reference model, DUT sample, compare
- Write one cocotb-style check in pseudocode
- Optional: open the lab’s source sketch and read the commented bench template
- This module is compare literacy, the scoreboard queue comes from the same expect idea

---

## Pitfalls to watch
- Do not treat no error as pass if you never compared anything
- Do not echo the DUT output into expect, that hides bugs
- A common miss is comparing before the simulator has settled after a poke
- Another trap is only checking in waves
- And remember

---

## Your turn
- Complete the checklist for at least one track, preferably both
- In the browser, load the starter and predict pass before you run check
- On paper, write the four self-check steps for one input change on the AND gate
- When you are ready

