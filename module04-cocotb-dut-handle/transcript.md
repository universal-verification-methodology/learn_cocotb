# Module 04 — cocotb DUT handle

**Module id:** module04-cocotb-dut-handle
**Lab:** cocotb-dut-handle
**Tracks:** A (concept / offline) · B (browser lab)

## Slide 1 — cocotb DUT handle

Triggers tell you when to act. The DUT handle tells you what to poke and peek. This module is that handle: how dotted paths walk the design hierarchy from Python, and how dot value reads or writes a signal. Get this right and every later driver or monitor is just choosing the right leaf.

## Slide 2 — Path walk and dot value

dut is the hierarchy root the simulator hands your test. Attribute dots walk instances—dut dot uart dot txd means the txd signal under uart under the top. Reading dot value peeks; assigning dot value pokes. A missing name raises AttributeError—there is no silent None for a bad path. Deeper nests like dut dot core dot regs dot r zero are the same idea: keep walking attributes until you reach the leaf.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the cocotb DUT handle sketch. You will see a challenge panel, a path resolver, and peek or poke controls. Load the starter—dut dot uart dot txd resolves with value one—then try a deeper path and a missing-path demo so you see AttributeError in the sketch. Work a few challenges and use Check when ready. Orient here; do not tour every button.

## Slide 4 — Real cocotb practice

In the real cocotb track, restate the handle idea on paper before you touch a simulator. Draw a tiny hierarchy: top, uart block, txd leaf. Write one peek line and one poke line using dot value. Optional: open the lab’s source sketch and read the comment header—it shows resolve, poke, peek, and a ghost path that fails. This module is handle literacy—not a full live UART simulation yet.

## Slide 5 — Pitfalls to watch

Watch for inventing hierarchy names that are not in the netlist—AttributeError is the signal you mistyped the path. A common trap is forgetting dot value; the handle is not the bit by itself. Another miss is treating a successful resolve as correct stimulus—peek after poke to confirm what the DUT saw. The browser tree is literacy; real fidelity is driving live handles against your simulator’s DUT.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, load the starter and try one missing-path challenge. On paper, explain path walk and dot value in your own words, then sketch one poke and one peek. When you are ready, take the short quiz, then continue to cocotb BinaryValue in the next module.
