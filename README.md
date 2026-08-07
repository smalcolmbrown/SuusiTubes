SuusiTubes

A better Thermionic Valve Model for LTspice simulations 

Building the wonderful work of Scott Reynalds, W. Marshall Leach Jr, Charles Rydel, Norman Koren, Stefano Perugini, Mike Holmes, and sage advice from Derk Reefman.

I converted Norman Koren's pspice tube libruary to work with LTspice and have been maintaining and extending it through 25 versions. BUT I was all too well aware of its limitations. and its development history. Its development path was through the classic tride model and Scott Reynolds pentode model. The Koren Triode model fixed the worst of the errors on the classic triode model but did not treat the control grid as a thermionic diode when driven positive with respect to the cathode. It simulated it it with a semiconductor diode and a resistor. This same problem extended to the Pentode tube model
Norman Koren actually developed three Pentode / Beam Tetrode nodels which were a big improvement on Scott Reynolds' model. But He did use the same flawed model for screen grid. Arguing that theer was insufficient data available to to make moddling it practical. In amplifier applications this was not a problem. But for Multivibrator and Logic applications this threw a big spanner into the works.
Then I found W Marshall Leach's 6L6 model which introduced the concept of a space charge AKA Cathode current. Which then made Screen current = Cathode current - Anode (plate) current. This started my ideas of building that into Norman Korens work.

It then dawned on me to use the Control grid method from Charles Rydel on Norman Koren's work.

Somewhere along the way I reasoned that I could adapt the Koren Pentode model to work as a Hexode and Heptode thus creating the first Hexode and Heptode tube model. (Derk Reefman introduced the second)

Anyroads this all ruminated in my head for a decade until June 2025 when I pulled my finger out and got on with it. I ripped apart the Koren Pentode model to properly understand how it works and then adapt it work with the Space charge concept that Marshall Leach had introduced. Once done I then intergrated the control grid as a thermionic diode as per Charles Rydels models.

All Diodes are modled using Stefano Perugini's second improvement on the classic Diode model.

All voltage regulators are modled by the use and abuse of Analog Spicemans neon model.

I find myself walking in the shadows of giants…

Hybridisation by Suusi Malcolm-Brown June 2025 - July 2026

PLEASE NOTE: SuusiTubes_V1.net is for LTspice only. I have tested it as much as I can. No doubt someone will find an error.  If you do please tell me about it so that I can fix it.
Version History
SuusiTubes_RC1.net	2025/10/08
SuusiTubes_RC2.net	2025/01/04
SuusiTubes_RC3.net	2025/06/15
SuusiTubes_V1.net	2026/07/23
