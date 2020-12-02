# Day 43 - Sniffing and Evasion
12/3/20

* [Sniffing and its Types](https://www.greycampus.com/opencampus/ethical-hacking/sniffing-and-its-types)

> "Attackers use sniffers to capture data packets containing sensitive information such as password, account information etc. Sniffers can be hardware or software installed in the system."

Sniffing in the switch would be active sniffing (dependent upon how a switch operates). However, a hub is much more promiscuous; sniffing through a hub is considered passive sniffing.

* [IDS Evasion and Firewall](https://www.youtube.com/watch?v=3cjQCA6qYPc)

You may be asked to evade detection from an IDS on a pentesting type of assignment. One thing you can do is manipulate packets to look a certain way or to spoof IP sources. Another thing is to use PackETH to generate a lot of "bogus" data so you can 'hide in the noise' generated -basically overwhelm sensors and run some scans under cover.

In nmap, you could set the throttle (timing template) to go really really slowly... that means it *may* not rise to a level that triggers an IDS ("low and slow").

You could also fragment packets to disguise in pieces...add decoys into a scan (to go under cover of friendly fire).

You do run the risk of slowing down your work, but this may be the price to pay to hide your activities. However, is your work time-sensitive? You need to plan for that.