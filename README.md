A collection of board layouts, licensed under CC-BY-SA-NC 3.0 (commercial license available on request, see LICENSE file).

I am not an electronics engineer, so take these layouts with a grain of salt.

# opa1622-breakout/

A simple breakout board to fit VSON10 op amps (like the OPA1622) into a DIP-8 socket.
Pin 1 is rectangular, the others are round.
Please be aware, the OPA1622 has 2 additional pins:

1. GND, which also connects to the board GND plane and which should be connected to a clean GND.
   If you use a virtual GND, I can not say if that's good for you.
   The IC GND pin is routed to the via next to the DIP pin 1.
   
2. The ENable pin is used to turn the IC on/off by switching it to V+.
   It is routed to the via next to DIP pin 5.
   Per default, it is always connected with a bottom line to V+, going from the via to DIP pin 5.
   If you want to control it via an external signal, cut that line and connect the via to your controller.
   
The OPA1622 datasheet suggests adding two decoupling capacitors from V+ and V- to GND. If you want to add them, there are SMD pads for those (0805 in).
  
**This board is not yet tested!** I'll do a fab run once I have more boards for a panel, and publish a note here on how to get any spares (costs will be just those I had, but feel free to tip).
