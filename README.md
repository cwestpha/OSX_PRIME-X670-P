# OSX_PRIME-X670-P
Mac OS on the Asus PRIME-X670-P

AMD Ryzen 9 7900X 12-core
Asus PRIME-X670-P
AMD 6900XT 16 GB Graphics Card
Samsung Evo 970 2TB SSD

OpenCore Base
Mac OS Ventura
Firmware 1616 release

Other OSs:
Endeavor OS (arch rolling) [This is primary OS for this system]
Windows 11 22H2

*******************************

What Works:
Most power states and basic functions
Intel AX 211 Wifi
Full USB Map
Everything not mentioned bellow

What doesnt work:
Intel Bluetooth
built-in ethernet (I have it disabled since I want my Aquantia 10GBe to be Eth0)

What I have given up on:
Fingerprint sensor (stupid Apple)

********************************

-to do-

Get Intel Bluetooth nice and sorted out
Get everything nicely labled
Work on enabling more hardware to get everything figured out.

---
xXxXxXxXx
---

-Geekbench 6 comparison-
remember Geek bench is a crappy benchmark and is poorly documented and optimized. Its kind of just a yolo thing so dont take it to seriously.

this setup:
https://browser.geekbench.com/v6/cpu/1812750

older setup /w iGPU only under Linux: [to show how poorly optimized the MacOS tests are]
https://browser.geekbench.com/v6/cpu/382368

this setup vs M2 Max [to show the natural competition for the R9/i9 1:1 SKU]
https://browser.geekbench.com/v6/cpu/compare/1812750?baseline=1831055
{note how the main victories of the M2 are using the ai/ml cores or updated libraries for the M# vs the 3+ year old code paths in modern CPUs like Zen4, makes me wonder what updated/optimized OS+libraries that support the AVX512 and scheduler for x86_64v4+ would be like}

this setup vs M2 Ultra [because this is what Apple likes to show off even though the competition would actually be a full Xeon/ThreadRipper setup]
https://browser.geekbench.com/v6/cpu/compare/1812750?baseline=1829859
{goes to show you how hard real benchmarking is. Optimizations, libraries, choices by the OS schedule, etc can make significantly more difference then anything inherent to the hardware. This throws efficency out the windows for raw clock rates and the Ultra does a good job in raw compute but shows plenty of rough edges while better being able to compete. Still we are talking about what you can build for under 1,500 USD for something that could easily run you 3k. Apple really isnt a hardware company, its a money printing factory first and formost. I miss mid 2010s Apple.}

xXxXxXxXx

This system compute:
https://browser.geekbench.com/v6/compute/635457

Comparison to real M1 Pro mac I use:
https://browser.geekbench.com/v6/compute/146223

This system compute vs a M2 Ultra almost maxed out in metal API:
https://browser.geekbench.com/v6/compute/compare/635457?baseline=641391
{I like how an old 6900XT you could get on firesale a few weeks ago can compeltely school a M2 Ultra. The M# series really is a tale of two cities. Some enlightened truely interesting results right next to weak 'why did they do this' decisions. Its really hard to decode what is happening, but the AI/ML/etc functions in modern GPUs/CPUs in X86_64 never truely go head to head with the best in aarm64. After all soon we will have some x86_64 CPUs with gigabytes of L4 cache taking up the space savings big almost L4 like lpddr5 on-package advantage Apple has. Stuff is about to get real crazy in End User Computing land and its funny to watch how everyone is trying to PR their way out of these changes.}
