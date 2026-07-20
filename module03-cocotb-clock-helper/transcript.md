# Module 03 — cocotb Clock helper

**Module id:** module03-cocotb-clock-helper
**Lab:** cocotb-clock-helper
**Tracks:** A (concept / offline) · B (browser lab)

## Slide 1 — cocotb Clock helper

After triggers, you need a clock that runs while your test does other work. cocotb’s Clock helper does that: you pass the clock signal handle, a period, and units, then call start. That launches a background coroutine that toggles the clock for you. Your test keeps awaiting RisingEdge on the same signal—no hand-toggling every half period.

## Slide 2 — Period, start, and edge times

The period is the full cycle length—low half, then high half. With period ten and units nanoseconds, the first posedge lands at ten, the second at twenty, the third at thirty. start runs alongside your async test; it does not block the rest of the coroutine. Pair this with RisingEdge from the last module and you have a clean rhythm: generate the clock once, then sync every test step to its edges.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the cocotb Clock helper sketch. You will see a challenge panel, period and units controls, and a timeline of posedge times. Load the starter—period ten gives edges at ten, twenty, and thirty—then try a shorter or longer period preset so the edge list moves. Work a few challenges and use Check when ready. Orient here; do not tour every button.

## Slide 4 — Real cocotb practice

In the real cocotb track, sketch the helper on paper before you run a simulator. Write Clock with dut dot clk, period ten, units ns, then start on its own line. List the first three posedge times you expect. Optional: open the lab’s source sketch panel and read the comment block—it shows the same shape real cocotb imports use. This module is clock-generation literacy, not a full UART testbench yet.

## Slide 5 — Pitfalls to watch

Do not confuse the Clock helper with manually flipping dut dot clk dot value every step—the helper owns the toggle loop. A common miss is mixing up period with half-period; posedges are spaced by the full period, not half of it. Watch units too—ten nanoseconds and ten microseconds are not the same timeline. And remember: the browser sketch shows edge math; real fidelity is start running against your simulator’s time base.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, load the starter and predict the third posedge before you reveal it. On paper, write the Clock line and three edge times for period eight. When you are ready, take the short quiz, then continue to the cocotb DUT handle in the next module.
