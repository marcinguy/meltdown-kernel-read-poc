# meltdown-kernel-read-poc
Read kernel virtual mapping via Meltdown

It is possible to read Kernel Virtual Mapping via Meltdown.

However, exploits available on the Internet/Github are not capable of this. Several few steps had to be made in order this to work.

I did it:

- disable KASLR
- using Kernel Module to calculate task_struct offsets (different accross Kernles)
- used a module to verify Memory allocations
- and finally, reading it via Meltdown (see screenshot below)

![Meltdown Kernel Read PoC](/meltdown-kernel-read-poc.png)


Code will not be published for a while. Still too many unpatched systems out there.
