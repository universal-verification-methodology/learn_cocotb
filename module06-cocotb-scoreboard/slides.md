---
marp: true
title: cocotb scoreboard
paginate: true
---

# cocotb scoreboard

A scoreboard checks that what the DUT actually did matches what you expected, transaction by transaction

---

## Expect queue and observe
- Order matters, the queue is a FIFO
- Push expect hex A five before the DUT responds, then observe A five when data is valid
- One match empties the queue
- Push two expects in order and observe both in order for two passes
- Observe the wrong byte and you fail without popping
- Observe when the queue is empty and you fail too, there was nothing left to check against

---

## Browser lab
![Browser lab starter](assets/lab-starter.png)

---

## Real cocotb practice
- In the real cocotb track
- Draw a three-step timeline: push expect, DUT responds, compare and pop or fail
- Write pseudocode for expect push and compare on one byte
- Optional: open the lab’s source sketch and read how match and mismatch are commented
- This module is expect-versus-observe literacy, not a full pyuvm scoreboard yet

---

## Pitfalls to watch
- Do not compare before the transaction is complete
- Do not pop the queue on failure; you need the expected value left for debug
- A common miss is pushing expects out of order when the DUT returns in order
- And remember

---

## Your turn
- Complete the checklist for at least one track, preferably both
- In the browser, load the starter and predict pass before you observe
- On paper, sketch push, observe, and pop for two expects in sequence
- When you are ready

