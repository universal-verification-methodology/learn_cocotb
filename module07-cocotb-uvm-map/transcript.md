# Module 07 — cocotb ↔ UVM roles

**Module id:** module07-cocotb-uvm-map
**Lab:** cocotb-uvm-map
**Tracks:** A (concept / offline) · B (browser lab)

## Slide 1 — cocotb ↔ UVM roles

Plain cocotb is Python driving a simulator with async triggers and DUT handles. pyuvm adds UVM-shaped components on top. SystemVerilog UVM is the same job in another language—tests, drivers, agents, and scoreboards. This module maps roles, not APIs: when someone says virtual interface, you know the cocotb side is dut dot signal.

## Slide 2 — Six role pairs

Six pairs bridge the worlds. Test entry: cocotb test decorator and Makefile module versus UVM test plus test name plusarg. Time: await RisingEdge or Timer versus posedge and delay. DUT access: dut handle versus virtual interface. Drive: Python pin assigns versus driver through vif. Structure: pyuvm agent versus uvm agent. Check: assert or scoreboard versus predict and observe scoreboard. Same verification jobs—different packaging.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the cocotb versus UVM map. You will see a challenge panel, role cards on both sides, and a mapped checklist. Load the starter—DUT handle paired with virtual interface already mapped—then select another pair and mark it mapped to build the bridge. Work a few challenges and use Check when ready. Orient here; do not tour every button.

## Slide 4 — Real cocotb practice

In the real cocotb track, restate the map on paper before you open a Makefile or UVM tree. Pick three pairs—test, await, and check—and write the cocotb side in one column and the UVM side in the other. Optional: open the lab’s source sketch and read the comment header—it lists the rough map in one place. This module is role literacy—not choosing pyuvm versus plain cocotb for your project yet.

## Slide 5 — Pitfalls to watch

Do not treat the map as one-to-one syntax—APIs differ even when roles match. A common miss is assuming pyuvm is required for every cocotb bench; plain cocotb with asserts is valid. Another trap is mapping driver to raw Python assigns when you already built a pyuvm agent. And remember: the browser cards are literacy; real fidelity is reading both a cocotb test and a UVM test for the same DUT.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, load the starter and name what dut maps to on the UVM side. On paper, fill in test and await for both columns without looking. When you are ready, take the short quiz, then continue to the self-check pattern in the next module.
