# Day 11 - Network Packet Analysis
10/19/20

* [Using Wireshark to steal passwords](https://blog.packet-foo.com/2016/07/how-to-use-wireshark-to-steal-passwords/)
* [Wireshark Basics](https://www.youtube.com/watch?v=jvuiI1Leg6w)

> "If you want to tell your network card “hey, accept everything! Forget the destination thing filtering, I want it all!” you need to enable a special mode on the network card. That mode is called “Promiscuous Mode”, and Wireshark does it automatically by default."

If you want to intercept packets on a network other than your own, you need to be in the right place at the right time, *and*...

* physical connection to the network they’re using
* physical connection to the  network they're accessing (which is unlikely, unless you work there)
* physical connection to any network in between those two (the person's Internet Service Provider)
* or the ability to capture plain text wireless packets while sitting close to someone you want to steal credentials from, e.g. in an unencrypted WiFi of a coffee shop (this is actually the best chance you get I guess).

With one of these access points, you could intercept data in one of the following scenarios:

1. the network protocol transporting the packets is unencrypted
2. the network protocol is encrypted, and we do not have the encryption keys
3. the network protocol is encrypted, but we have the encryption keys

However, you're *most likely* not going to be able to both gain access and decrypt anything - which is GOOD news (because you don't want anyone doing this to ***your*** private data).

Wireshark can show you what's going on in MULTIPLE layers of packet transport. You can also track and examine HTTP and TCP congestion.

Seems like the narrator ***could not be more excited*** to talk about Wireshark.




### Additional Resources
* [Advanced analysis challenges](https://www.malware-traffic-analysis.net/)