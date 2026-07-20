# Module 01 — Python async TB

**Module id:** module01-python-async-tb
**Lab:** python-async-tb
**Tracks:** A (real cocotb) · B (browser lab)

## Slide 1 — Python async TB

cocotb tests are Python coroutines. You mark a test with async def, register it with the cocotb test decorator, and use await to suspend until the simulator resumes you—often after a timer or a clock edge. That shape replaces the procedural always-block style of classic SystemVerilog testbenches with something closer to modern async Python. This module is literacy for that pattern, not a full simulator run yet.

## Slide 2 — async, await, and the decorator

Three pieces fit together. async def declares a coroutine—the function can pause at await and come back later. await hands control to the event loop until a trigger fires, and simulation time can advance while you wait. The cocotb test decorator registers your coroutine so the runner actually starts it. A plain def test cannot await; an async test without the decorator is a valid coroutine but not a registered entry point.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the Python async testbench sketch and load the starter example. The step trace shows enter, suspend at Timer, resume, and DONE. Try presets: RisingEdge instead of a timer, two awaits in one test, or the deliberate failures—a plain def or a missing decorator. Use the challenge panel to quiz yourself on async def, await, and registration, then run until you see DONE on a valid starter test.

## Slide 4 — Real cocotb track practice

In the real cocotb track, open this module's examples prompts. Restate the async testbench idea in one sentence—coroutine plus await plus registration. Sketch a tiny async test on paper: decorator, async def test taking dut, one await on a timer or edge, then a poke or peek comment. Optional stretch: name one await you would use in a real cocotb Makefile flow you already have. No simulator required yet; the goal is to recognize the shape when you see it in code.

## Slide 5 — Pitfalls to watch

Do not use a plain def when you need await—that is not a coroutine and cocotb will not treat it as a time-advancing test. Do not forget the test decorator; without it your async function never enters the runner's queue. Do not assume await is instant—it suspends until a trigger completes, which is how simulation time moves. And remember: the browser sketch is conceptual; real cocotb still needs imports, a DUT handle, and a simulator behind the scenes.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, load starter, run to DONE, and clear a couple of quiz challenges on async and await. On paper, write one valid cocotb test skeleton with all three pieces named. When you are ready, take the short quiz, then continue to cocotb triggers.
