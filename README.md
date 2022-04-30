# Howard's ham radio exam prep

References:

- IRTS sample exam paper 2022 "Amateur Radio Licence Exam In Accordance with ECC/REC/T/R 61-02 HAREC Standard"
  * https://www.irts.ie/dnloads/IRTS_Sample_Exam_Paper_2022.pdf

## A.1 Safety - 5 questions

### 1. What's the appropriate rating for a fuse used in a circuit consuming 500w from mains power?

Ireland's AC outlet voltage is about 220 volts, that's about 170v RMS.

Power = V x I, I = 2.9A

My answer: A - 3A

Correct!

### 2. For a valve power amplifier, the smoothing capacitor in its high voltage supply requires ...

Valve refers to vacuum tubes. Capacitors don't usually generate heat.

My answer: A - Large value resistors to discharge the capacitors when switched off.

Correct!

### 3. Consideration for keeping high voltage away from possible human contact when installing a resonant half-wave dipole

I'm fairly certain hazardous voltage can appear throughout the entire length of dipole, however I am unsure what a low pass filter does to a transmitting dipole.

My answer: D - All are equally important; the voltages are the same at all points.

Correct answer: A - the location of the ends of the dipole

#### What went wrong?

Check out the wikipedia article on dipole antenna. The highest of voltages show up at the end of a half-wave dipole antenna:

https://upload.wikimedia.org/wikipedia/commons/d/dd/Dipole_receiving_antenna_animation_6_800x394x150ms.gif

How half-wave dipole works on receive:

- The incoming RF wave pushes electrons back and forth.
  * Consequently, the ends of the dipole are charged.
- The electrical field induces a standing wave of voltage.
- The oscillating current flows down the transmission line and to the receiver.

### 4. Consideration for using a guy role to help supporting a mast

No idea what a guy rope is, assuming it's just a regular rope.

My answer: D - secure it so that the mast falls away from nearby structures when the rope fails.

Correct answer: B - Secured to the ground, more than 60% of mast's height away from the base.

#### What went wrong?

"Guy rope" is a tensioned cable, adding stability to a free standing structure.

Secure the rope to the ground more than 60% of mast's height away from the base adds to the leverage.

At a distance the mast and rope together will look like a short triangle.

### 5. What's the most important factor to consider to ensure ham radio station is compliant with radiation exposure limits?

The design of the final amplifier is likely more concerned about efficiency than the leakage.

Filtering at the output stages helps to eliminate undesirable interference but not hugely relevant to radiation exposure.

"Parasitic oscillations" is not relevant to radaition exposure.

The design and location of antenna sounds most appropriate.

My answer: C - the design and location of antenna.

Correct!

## A.2 Interference and immunity - 4 questions

### 6. A 70-Mhz transmitter is causing harmonic interference to TV receiver at 210-Mhz, how to tweak the antenna to eliminate the interference?

I suppose the objective is to make the antenna less efficient radiating RF at 210-Mhz.

The installation of a coaxial stub gives the choice of quarter wavelength at 70 or 210 Mhz, open or closed circuit.

Clues:

- Microwave wave guides are not closed circuit.
- Subject of wave guide is 210 Mhz RF.

My answer: C - open circuit coaxial stub at quarter-wave of 210 Mhz.

Correct!

### 7. What's a likely cause of intermodulation in a receiver?

My answer: A - mixing frequencies in some part of the receiver circuit.

Correct!

### 8. What does a band pass filter do?

My answer: C - passes signals within a frequency range

Correct!

### 9. Neighbour's hi-fi system emits harmful RF, find a remedy.

Placing a capacitor in series with the transmitter output simply adds another phase in between the output voltage and current, it does nothing for interference.

Clue: ferrite rings are often seen on DC power supply cables.

Putting a ferrite ring on the hi-fi ssytem's loudspeaker (output) cables probably can help.

Placing a ferrite ring on the transmitter output cable probably won't help.

No idea what an open-wire feeder is, study it later.

My answer: B - putting a ferrite ring on the hi-fi system's loudspeaker output cable.

Correct!

## A.3 Electrical, electro-magnet, and radio theory - 4 questions

### 10. Identify the circuit.

There are two parallel capacitors and an inductor in between.

Capacitors introduce a phase between output voltage and current by introducing a lag in voltage.

Capacitor reactance (opposing AC current) decreases with frequency and capacity.

Inductor let DC (low frequency) pass.

My answer: B - low pass filter.

Correct!

### 11. Alternating current leads the voltage in...

Keep in mind:

- Current leads voltage in a capacitive circuit.
  * That's why it takes me hours to charge up a super capacitor using AA batteries.
- Voltage leads current in an inductive circuit.

So for current to lead voltage in an AC circuit, the circuit needs to be capacitive.

My answer: C - capacitive circuit.

Correct!

### 12. What input power is required to obtain 20 watts of output after an amplification of 10 dB?

Power doubles every ~3 dB.

20 - 10 - 5 - 2.5.

My answer: C - 2 watts.

Correct!

### 13. Describe the characteristic of the current in the circuit.

There's a capacitor (C) in parallel with an inductor (L).

Capacitors exhibit prominent capacitance below a resonant frequency and exhibit prominent inductance above a resonant frequency.

Inductors let DC (low frequency) pass.

My answer: A - current at the resonant frequency and below will be unaffected.

Correct answer: B

#### What went wrong?

Resources to study:

- https://www.electronics-tutorials.ws/category/accircuits
- https://article.murata.com/en-eu/article/impedance-esr-frequency-characteristics-in-capacitors

Regarding impedance of resistors, inductors, and capacitors:

- Impedance to AC is like resistance to DC. Impedance (Z) is the result of both resistance (R) and reactive (X) components.
  * Reactance (X) is always 90 degrees out of phase with resistance (R).
    - The higher the reactance, the more out of phase current is.
  * Reactance (X) can be either inductive or capacitive.
  * Impedance (Z) squared = resistance (R) squared + reactance (X) squared
- The impedance of a resistor-inductor circuit increases with higher frequency and higher inductance.
  * Reactance (X) of a inductor = 2 x pi x frequency x inductance (L)
    - Inductors let DC through and impede AC.
    - The higher the frequency, the higher the reactance.
- The impedance of a resistor-capacitor circuit increases with lower frequency and lower capacitance.
  * Reactance (X) of a capacitor =  1 / (2 x pi x frequency x capacitance C)
    - Capacitors let AC through and impede DC.
    - The higher the frequency, the lower the reactance.
- The impedance of a resistor-inductor-capacitor circuit???????????
  * The impedance "triangle" of an inductor has a positive slope. The impedance "triangle" of a capacitor has a negative slope.
  * Reactance (X) = inductive reactance - capacitive reactance

Regarding the correction of power factor:

- Improve AC circuit efficiency = reduce current = reduce the reactance.
- In an inductive AC circuit, inductors cause current to lag behind voltage.
- Add capacitors to slope the impedance "triangle" downward.

Regarding the frequency characteristics of capacitors:

- The impedance (Z) of an ideal capacitor equals to the reactance (X).
  * Recap: Reactance = 1 / (2 x pi x frequency x capacitance C)
  * The impedance increases with lower frequency and lower capacitance.
- Realistic capacitors have equivalent series resistance and inductance.
  * After a certain frequency, the inductance causes the overall impedance to increase.

All about components in series and in parallel:

- Resistors
  * Series: R = R1 + R2 ...
  * Parallel: R = 1 / (1 / R1 + 1 / R2 ...)
- Inductors
  * Series: L = L1 + L2 ...
  * Parallel: L = 1 / (1 / L1 + 1 / L2 ...)
- Capacitors
  * Series: C = 1 / (1 / C1 + 1 / C2 ...)
  * Parallel: C = C1 + C2 ...
- Impedance
  * Phew, too complicated.

Revisit the question:

- The circuit has an inductor and capacitor in parallel.
  * Similar to resistance in parallel, reactance = R1 x R2 / (R1 + R2)
- Looking at a couple of extreme examples:
  * DC flows through the inductor alone, bypassing the capacitor entirely, exhibiting minimal loss.
  * High frequency AC flows through the capacitor alone, bypassing the inductor entirely, exhibiting minimal loss.
  * In between, the parallel reactance (hence impedance) peaks at the resonant frequency. Therefore the answer is B - the current will be impeded at the resonant frequency.

## A.4 Components in a circuit - 3 questions

### 14. Determine the capacitance of the circuit.

My answer:

There are 10 nF and 5 nF of capacitance in series. 1 / (1 / 10 + 1 / 5) = 1 / (0.1 + 0.2) = approximately 3.3 nF, answering A.

Correct!

### 15. Determine the current flowing through a resistor.

My answer:

- The upper side of the parallel circuit has a total resistance of 60 ohm.
- The equivalent resistance is 1 / (1 / 60 + 1 / 120) =  40 ohm.
- The current flowing through the battery is I = V / R = 6 / 40 = 0.15 amps.
- The ratio of current flowing between the upper and lower side of the circuit is 2 : 1.
- The current flowing through the upper side of the circuit is 0.1 amps.
- The ratio of current flowing through the two resistors is 33 : 27.
- The current flowing through the left resistor is 0.1 / (33 + 27) * 33 = 0.055 amps.
- The closest choice is C - 60 mA.

Correct answer: D

#### What went wrong?

Resistors in serial divide voltage instead of current. I should have stopped at where I calculated the current flowing through the upper side of the circuit.

### 16. What component can be used to regular power supply output voltage?

My answer: Electrolytic capacitor - B

Correct!
