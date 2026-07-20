# Module 05 — cocotb BinaryValue

**Module id:** module05-cocotb-binary-value
**Lab:** cocotb-binary-value
**Tracks:** A (concept / offline) · B (browser lab)

## Slide 1 — cocotb BinaryValue

Plain Python integers do not carry bit width. cocotb BinaryValue wraps a value with n bits so drive and read match the signal’s width. You construct it with an integer or hex literal and a width, then assign it to dut dot signal dot value. The helper masks to the low bits and prints a bit string with MSB on the left.

## Slide 2 — Width, value, and bit string

n bits sets how many bits are kept—wider input is truncated to the low bits. Starter example: eight-bit hex A five becomes binary one zero one zero zero one zero one, MSB left. Decimal two fifty-five and hex F F mean the same eight-bit pattern. For poke, dut dot data dot value equals BinaryValue with your literal and n bits equals width. To read back, convert the signal value to int when you need a Python number.

## Slide 3 — Browser lab

![Browser lab starter](assets/lab-starter.png)

In the browser lab track, open the cocotb BinaryValue sketch. You will see a challenge panel, width and value fields, and a bit-string readout. Load the starter—eight bits, hex A five, bits one zero one zero zero one zero one—then try a truncate preset so a wide hex value masks down to eight bits. Work a few challenges and use Check when ready. Orient here; do not tour every button.

## Slide 4 — Real cocotb practice

In the real cocotb track, work the bit math on paper before you drive a live signal. Write BinaryValue for hex A five with n bits eight and draw the MSB-left string bit by bit. Try width four with hex F and confirm all ones. Optional: open the lab’s source sketch and read how poke and int peek are commented. This module is width-aware drive literacy—not a full scoreboard yet.

## Slide 5 — Pitfalls to watch

Do not assume Python’s bin of an integer matches cocotb’s MSB-left string without applying the width mask first. A common miss is reading bits MSB-right—cocotb prints index width minus one on the left. Another trap is poking a wider value than the port; truncation happens silently, so know your width. And remember: the browser calculator is literacy; real fidelity is BinaryValue on live simulator handles.

## Slide 6 — Your turn

Complete the checklist for at least one track—preferably both. In the browser, load the starter and predict the bit string before you set value. On paper, convert hex A five to eight bits MSB left without looking. When you are ready, take the short quiz, then continue to the cocotb scoreboard in the next module.
