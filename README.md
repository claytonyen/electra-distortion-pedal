# Electra Distortion Pedal
The electra distortion pedal consists of a common emitter gain stage using a NPN BJT into a diode clipping stage, and it
sounds quite good for its simplicity. 

I used this pedal schematic I found off of the r/diypedals reddit thread as a reference:

![](images/electra_distortion_schematic.png)

### First Attempt Using 3 1N1418 Diode Clipping Stage
Some changes I made to the schematic include adding a very small ceramic capacitor in parallel with the feedback resistor  to increase negative feedback at high frequencies, 
reducing high-frequency gain to get rid of some harsh treble fizz. The diode clipping stage in the reference schematic uses a 1N4148 and a 1N34A diode. While the 1N4148 is a 
standard silicon diode with a 0.6 - 0.7 V voltage drop, the 1N34A is a germanium diode with a smaller voltage drop, roughly 0.2 - 0.3 V, meaning the signal is clipped 
asymmetrically. Asymmetrical clipping introduces even-order harmonics to the signal as well as reduces overall compression, creating a warm and responsive tone. I did not 
have a 1N34A diode on hand, so in an attempt to emulate the reference clipping stage, my asymmetrical clipping configuration consists of three 1N4148 silicon diodes in a 
2+1 parallel arrangement. Since the forward voltage of the 1N4148 is a bit high, the circuit struggled to reach an obvious clipping of the signal. This is something I will 
try to modify in subsequent iterations of this distortion circuit.
