# Module 08 — Self-check pattern

**Module id:** module08-self-check-tb
**Lab:** self-check-tb
**Tracks:** A (concept / offline) · B (browser lab)

## Slide 1 — Self-check pattern

Before scoreboards and agents, every testbench needs a self-check loop: apply stimulus, compute expected from a reference model, sample the DUT output, then pass or fail loudly. cocotb coroutines do the same job with await and asserts—stimulus, golden expect, compare. Good benches fail with a clear message; great benches also tally passes so you trust a green run.

## Slide 2 — Stimulus, expect, compare

Starter: a two-input AND gate with a equals one and b equals one, expect y equals one, got one, pass. The expect comes from the AND truth table—not from copying the DUT output back. Change one input and recompute expect before you compare. Wrong expect on purpose should fail so you practice the error path. Compare after the signal settles, not mid-transition.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the self-check TB sketch. You will see a challenge panel, stimulus fields, expect and got readouts, and a pass or fail verdict. Load the starter—AND gate, both inputs high, expect one, pass—then switch to the adder or mux preset and run check after you set a real reference expect. Work a few challenges and use Check when ready. Orient here; do not tour every button.

## Slide 4 — Real cocotb practice

In the real cocotb track, restate the loop on paper before you write a live assert. Draw four boxes: stimulus, reference model, DUT sample, compare. Write one cocotb-style check in pseudocode—poke inputs, await a cycle, assert output equals expected. Optional: open the lab’s source sketch and read the commented bench template. This module is compare literacy—the scoreboard queue comes from the same expect idea.

## Slide 5 — Pitfalls to watch

Do not treat no error as pass if you never compared anything. Do not echo the DUT output into expect—that hides bugs. A common miss is comparing before the simulator has settled after a poke. Another trap is only checking in waves; self-check means the log or exit status tells the story. And remember: the browser sketch is literacy; real fidelity is assert or scoreboard on live simulator handles.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, load the starter and predict pass before you run check. On paper, write the four self-check steps for one input change on the AND gate. When you are ready, take the short quiz, then continue to waveform literacy in the next module.
