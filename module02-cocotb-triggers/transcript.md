# Module 02 — cocotb triggers

**Module id:** module02-cocotb-triggers
**Lab:** cocotb-triggers
**Tracks:** A (real cocotb) · B (browser lab)

## Slide 1 — cocotb triggers

Every await in a cocotb test waits on a trigger—an object that tells the simulator when to resume your coroutine. RisingEdge and FallingEdge watch clock transitions. Timer waits a fixed delay in simulation time. First and Combine compose multiple triggers: First finishes when the earliest one completes; Combine waits until all of them have. Triggers are how Python testbench code stays synchronized with RTL events instead of busy-waiting.

## Slide 2 — Edge, timer, and compose triggers

RisingEdge on a clock resumes on the next zero-to-one transition; FallingEdge on the next one-to-zero. Timer ignores pins and completes after N time units—useful for reset delays or timeout checks. First is a race: whichever trigger finishes first wins and the others are cancelled. Combine is a join: you resume only after every listed trigger has completed—often at the latest finish time. Pick the trigger that matches the event you actually care about.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the cocotb triggers sketch and load the starter preset. The timeline shows clock edges and when RisingEdge fires—starter waits for the first rise at time ten. Switch presets: FallingEdge, Timer, First where the edge beats the timer, First where the timer wins, and Combine waiting for both. Watch the verdict panel name the winning trigger and fire time. Challenges ask you to load specific presets and answer quiz questions on each trigger type.

## Slide 4 — Real cocotb track practice

In the real cocotb track, open this module's examples prompts. Restate what a trigger does in one sentence—resume the coroutine when a simulator event completes. Sketch one await chain on paper: wait for a rising clock edge, then a timer delay, then another edge. Optional stretch: write when you would choose First over Combine—hint: timeout versus join. Again, no live simulator required here; you are building a mental model you will apply in later offline modules.

## Slide 5 — Pitfalls to watch

Do not await RisingEdge when you meant FallingEdge—the resume time differs by half a cycle or more. Do not treat Timer like a wall-clock sleep—it advances simulation time, not your laptop clock. First cancels losing triggers; Combine waits for all—swapping them changes test semantics. If no edge ever arrives, an edge trigger may hang or fail—always check reset and clock generation. The browser timeline is simplified; real waveforms still need you to confirm the DUT actually toggles the pin you await.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, run starter RisingEdge at ten, load a First preset where the timer wins, and clear quiz items on Timer and Combine. On paper, draw a tiny timeline with one rise, one fall, and mark where RisingEdge and Timer of twenty-five nanoseconds would each fire. When you are ready, take the short quiz, then continue to the cocotb clock helper.
