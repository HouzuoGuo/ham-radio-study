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

## A.3 Electrical, electro-magnetism, and radio theory - 4 questions

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

My answer: Electrolytic capacitor - B.

Correct!

## A.5 Transceivers - 4 questions

### 17. Determine the bandwidth characteristics of SSB transmission

- SSB uses about half the bandwidth of AM transmission, eliminating A.
- For voice transmission SSB does not significantly add to or remove from the fidelity of the audio, eliminating B.

My answer: SSB occupies about half the bandwidth of AM transmission - D.

Correct!

### 18. What does the sensitivity of a receiver refer to?

My answer: Its ability to receive weak signals - C.

Correct!

### 19. Identify a component in SSB transmitter circuit.

I don't actually recall how SSB transmitter circuit gets rid of the carrier. But in any case speech input is often fed to a modulator.

My answer: balanced modulator - B.

Correct!

### 20. Determine bandwidth characteristics of FM transmission.

Bandwidth of an FM transmission is twice its deviation. FM transmission has fixed bandwidth and it is independent from audio frequency, eliminating A and B.

My answer: twice the deviation frequency - D.

Correct answer: twice the sum of deviation frequency and audio frequency - B

#### What went wrong?

Verified on SDR: FM transmission bandwidth is *not* independent from audio frequency, the higher the audio frequency the higher the bandwidth!

## A.6 Antennas and transmission lines - 4 questions

### 21. The characteristic impedance of coax cable?

My answer: 50 ohms - B.

Correct!

### 22. Which type of feed line is appropriate for when antenna feeder must pass near conductive objects?

Twisted pair (is it the same thing as twisted lead?) let both wires share the same noise and it's commonly used in ethernet cables.

Individual wires without shielding are susceptible to electronic interference.

My answer: coaxial cable - D.

Correct!

### 23. Determine the characteristics of ERP for an antenna.

ERP is effective radiating power.

My answer: directly proportion to antenna's gain - A.

Correct!

### 24. What's the impedance of a shorted transmission line?

Remember the "open - short - load" calibration method of NanoVNA?

My answer: zero - A.

Correct answer: very high - D

#### What went wrong?

No clue, ask folks from the radio club.

TODO FIXME

## A.7 RF propagation - 4 questions

### 25. Determine the propagation characteristics of the 160m band.

Clues:

- The 160m band propagates over the ground rather than being reflected by ionosphere.
- The 160m band is considered by some as being in the "medium wave" band.
- The higher the frequency, the higher its likelihood of penetrating all ionosphere layers.
  * RF signals of higher frequencies are also susceptible to being absorbed by atmospheric conditions such as rain.
- The ionosphere layers are, from lowest to highest: D, E, F1, F2.

My answer: RF signal is absorbed by the D layer - B.

Correct!

### 26. What is least likely to influence the distance of a single hop in HF transmission?

- Frequency is definitely a factor, e.g. "band is open/closed".
- Mode of transmission is irrelevant to RF propagation, though some modes are more efficient for certain use cases.
- Angle of radiation is definitely a factor, e.g. near vertical incidence skywave.
  * For NVIS, radiation angle is driven toward up direction when the antenna is placed closer to ground.
- Height of ionosphere is definitely a factor.

My answer: mode of transmission - B.

Correct!

### 27. Determine the propagation characteristics of the 160m band again.

Note the relatively short distance between the two stations.

- Ground wave is how RF signals on the 160m band usually propagate.
- Sporadic E happens for much higher frequencies, often 6m and above.
  * Remember how I received the APRS beacons 500km away?

My answer: ground wave - A.

Correct!

### 28. What's the frequency above which RF penetrates instead of being reflected?

My answer: MUF - B.

Correct answer: critical frequency - A.

#### What went wrong?

Review the concepts of MUF and critical frequency:

- Critical frequency is the one below which RF is reflected and above which RF penetrates through *at vertical incidence*.
  * CritFreq = sqrt(81 x ionisation density).
- Because the critical frequency is measured at vertical incidence, MUF is often much higher.
  * MUF is a prediction ("usable"), first of all.
  * As a rule of thumb, MUF = 3 x critical frequency.
  * MUF = CritFreq / cos(angle of incidence).

## A.8 Measurement - 2 questions

### 29. What is the Y axis on an oscilloscope?

My answer: the signal voltage - D.

Correct!

### 30. Calculate RMS.

For AC, RMS is approximately 70% of peak voltage.

My answer: 7v - C.

Correct!

## Short recap of my result so far

Keep in mind that the pass mark of the section A is 60%.

My result: 23 / 30 = 76%, pass!

## B.1 Phonetic alphabet - 1 question

### 31. Speak NK6GR in phonetic alphabet

My answer: november kilo 6 golf romeo - A.

Correct!

## B.2 Q codes - 3 questions

### 32. Q code of the location?

My answer: QTH - D.

Correct!

### 33. What is QRZ?

My answer: who's calling me - B.

Correct!

### 34. What is QSB?

My answer: signal is fading - D.

Correct!

## Short recap of Q codes

IDs:

- QRA - name
- QRB - distance
- QTH - location

Operational:

- QRP - low power
- QRV - ready
- QRS - slow

Interference:

- QRZ - who's calling?
- QRM - interference
- QRN - static
- QSB - fading

## B.3 In case of emergency - 3 questions

### 35. What's the word for distress?

My answer: Mayday - C.

Correct!

### 36. What's the emergency communication centre of frequency on 80m band?

My guess: 3.750Mhz - B.

Review this later on for all HF and VHF bands.

Correct answer: 3.760Mhz - D

#### What went wrong?

Study HF band plan: https://www.iaru-r1.org/wp-content/uploads/2021/06/hf_r1_bandplan.pdf

### 37. What's the UHF simplex frequency?

My answer: 433.5Mhz - C

Correct answer: 433.775Mhz - D

#### What went wrong?

433.5Mhz is the IARU region 1 (Europe & Africa) simplex calling frequency, it is not the amateur radio emergency network's simplex frequency.

## Short recap of emergency frequencies

References:

- HF band plan: https://www.iaru-r1.org/wp-content/uploads/2021/06/hf_r1_bandplan.pdf
- VHF band plan: https://www.iaru-r1.org/wp-content/uploads/2020/12/VHF-Bandplan.pdf

IARU regions:

- Region 1: Europe and Africa.
- Region 2: Asia and Australia.
- Region 3: North and South America.

General rule of frequency allocation from lowest to highest in each band:

- CW (200 Hz)
  * QRP centre of activity is located toward the higher frequencies.
- Narrow-band and digital modes (500 Hz)
  * Automatic stations are located toward the higher frequencies.
- Beacons (no bandwidth specified)
- All modes - digital, SSB (2700 Hz)
- All modes - SSB (2700Hz)
  * QRP centre of activity is located toward the middle.
  * Emergency and SSTV frequencies are located toward the higher frequencies.

HF emergency frequencies:

- 3760 kHz
- 7110 kHz
- 14300 kHz
- 18160 kHz
- 21360 kHz

# Start over from the beginning

Some time between May and July 2022 the sample example paper at https://www.irts.ie/dnloads/IRTS_Sample_Exam_Paper_2022.pdf changed to a new revision.

Start over with "IRTS HAREC Sample Examination Paper v1.1.6".

## A.1 Safety

### 1. Fuse current for a 500W appliance

My answer: A - 3Amps.

Correct!

### 2. Keep field strength within limits

Keep in mind of the inverse square law.

My answer: C - position the antenna so that affected people are in the far field.

Correct!

### 3. Hazardous voltage on a dipole

A dipole antenna has high voltage at the poles and high current in the centre.

My answer: A - ends of the dipole.

Correct!

### 4. Guy rope as mast support

My answer: B - secured to the ground more than 60% of the mast's height away from the base.

Correct!

### 5. Reduce public RF exposure

My answer: C - the design and location of the antenna.

Correct!

## A.2 Interference

### 6. Transmitter interferes with a PC

Sounds like improper equipment grounding or the presence of common mode current.

This is probably unrelated to grounding as the Q does not mention hazardous voltage's presence on the equipment.

My answer: D - fit a ferrite ring on computer's cables.

Correct answer: C - use a low-pass filter.

Actually, I don't understand the correct answer of this Q.

### 7. Receiver intermodulation

My answer: A - mixing of two frequencies somewhere in the receiver (that's the very definition of intermodulation).

Correct!

### 8. What's a band pass filter?

My answer: C - passes signals between two frequencies

Correct!

### 9. Neighbour's audio system is causing interference

My answer: B - put a ferrite ring on the audio system's speaker cables.

Correct!

## A.3 Radio theory

### 10. Ohm's law applied to power calculation

P = I^2 x R

My answer: D - 500W

Correct!

### 11. What kind of circuit has current leading the voltage?

Remember how I charged up the ultracapacitor?

My answer: C - a capacitive circuit.

Correct!

### 12. Digital processing of signal in the time and frequency domains

My answer: B - fast fourier transformation.

Correct!

### 13. SSB transmission characteristics

My answer: D - upper side band.

Correct!

## A.4 Circuitry

### 14. Identify circuit's purpose

My answer: B - current is impeded at resonant frequency.

Correct!

### 15. Apply ohm's law

27 + 33 = 60, total current over both resistors = 100mA.

My answer: D - 100mA.

Correct!

### 16. Amplifier gain in dB

Power doubles roughly every 3 dB. 7dB - 10W, 4dB - 5w, 1dB - 2.5w.

My answer: C - 2W.

Correct!

### 17. SSB transmission characteristics

My answer: D - uses about half the bandwidth of AM.

Correct!

### 18. Sensitivity of a receiver

My answer: C - ability to receive weak signals.

Correct!

### 19. Identify components of an SSB transmitter

My answer: B - balanced modulator.

Correct!

### 20. FM transmission characteristics

My answer: B - twice of (peak deviation frequency + audio frequency).

Correct!

## A.6 Antennas

### 21. Coax cable

My answer: B - 50 ohm.

Correct!

### 22. Choose a cable for using in the vicinity of conductive objects

My answer: D - coax.

Correct!

### 23. ERP of an antenna

ERP is the effective radiating power.

My answer: A - proportional to the antenna's gain.

Correct!

### 24. Purpose of an ATU

My answer: B - match the impedance of transmission line to that of antenna.

Correct!

## A.7 Propagation

### 25. Atmospheric absorption

Remember the layers, from lowest to highest: D, E, F1, F2.

My answer: B - the signal is absorbed by the D layer.

Correct!

### 26. Factor not contributing to skywave skip distance

My answer: B - mode of the transmission.

Correct!

### 27. Ways of propagation on the 160m band

My answer: A - ground wave.

Correct!

### 28. Critical VS usable frequency

Keep in mind that, the maximum usable frequency is usually 3 x the critical frequency.

My answer: A - the critical frequency.

Correct!

## A.8 Measurements

### 29. Using an oscilloscope

X - time, Y - amplitude.

My answer: D - the signal voltage.

Correct!

### 30. RMS and peak voltage

From highest to lowest: peek-to-peek, peek, RMS, average.

My answer: C - 7.07V.

Correct!

## Section A summary

29/30 = 96%

## B.1 Phonetic alphabet

### 31. Spell a callsign

My answer: A - November Kilo 6 Golf Romeo

Correct!

## B.2 Q-codes

### 32. Location and position in Q code

Keep in mind: QRA - name, QRB - distance, QTH - location.

My answer: D - QTH.

Correct!

### 33. What is QRZ?

Keep in mind: QRZ - who's calling? QSL - please ack.

My answer: B - who's calling?

Correct!

### 34. Q code for interference

Keep in mind: QRM - interference, QRN - static, QSB - fading.

My answer: D - QSB means fading.

Correct!

## B.3 Emergency communication

### 35. Mayday

My answer: C - Mayday

Correct!

### 36. Irish emergency communication centre of activity on the 80m band

Can I possibly remember these frequencies? lol

My answer: C - 3.630

Correct answer: B

### 37. Usage of emergency communication centre of activity frequencies

My answer: C - permitted for use unless there's emergency communication in progress.

Correct!

## B.4 Call signs

### 38. Prefix of Czechia

My answer: C - OK.

Correct!

### 39. Off-shore Irish operation

Keywords - offshore, island (land!).

My answer: B - EJ3PA

Correct!

### 40. Find a valid callsign

My answer: C - 2E6J

Correct!

## B.5 Band plans

### 41. 160m voice segment

Keep in mind: the 160m band spans between 1810 KHZ and 2000 KHZ.

My answer: C - 1853 kHz.

Correct!

### 42. 80m band

Keep in mind: the 80m band spans across 3.5 MHZ and 3.8 MHZ.

My answer: B - CW.

Correct!

### 43. Secondary allocation

Probably one of those WARC bands, including the newly allocated 60m band.

My answer: A - 18.068 - 18.168.

Correct answer: C - 50 MHZ - 52 MHZ.

### 44. 40m band

My answer: D - 7 MHZ - 7.3 MHZ

Correct answer: B - 7MHZ - 7.2 MHZ

## B.6 Code of conduct

### 45. Congested DX

My answer: D - wait for DX station to QRZ.

Correct!

### 46. Call CQ on a newly tuned frequency

My answer: B - "Is this frequency in use, this is XXXXX. (wait and then) CQ from XXXXX."

Correct!

### 47. Identify transmission

My answer: D - At the beginning and the end of the contact, and every 30 minutes.

Correct answer: C - At the beginning and the end of the contact, and frequently at short intervals.

## B.7 Operating procedure

### 48. RS of 35

Remember: readability, signal strength, and CW tone.

My answer: D - readable with difficulty, 5 on the S metre.

Correct!

### 49. CQ to Japan only

My answer: C - CQ DX Japan from EI9ABC.

Correct answer: B - CQ Japan from EI8ABC.

### 50. CQ DE EI9ABC AR in CW

My answer: A - general call for a contact.

Correct!

### 51. Who takes care of international interference?

My answer: B - ComReg.

Correct answer: C - To IARU via IRTS liaison officer.

### 52. Suffix QRP

My answer: C - used for low power operation only.

Correct answer: D - should not be used at all.

## B.8 ITU regulations

### 53. When is the communication between ham stations permitted when stations are in different countries?

My answer: C - the two countries have to be IARU members.

Correct answer: B - permitted by default unless there is unless countries explicitly object.

## 54. ITU designation of J3E

Remember: A - DSB, F - FM, J - SSB. 1 - Digital, 3 - Analogue. E - Voice.

My answer: A - SSB speech.

Correct!

## B.9 CEPT regulations

### 55. CEPT ham license holder privilege

My answer: D - communicate with anyone on the ham radio frequencies.

Correct answer: C - communicate with ham radio stations on ham radio frequencies. TODO FIXME: but what about in case of emergency?!

### 56. Who is M/EI8XYZ?

M is England.

My answer: B - the holder of EI8XYZ, on a visit to England.

Correct!

### 57. Operating in another CEPT country using Irish license

My answer: D - no duration restriction.

Correct answer: A - between one and three months

## B.10 Irish regulations

### 58. Logbook content

Remember: station ID, time and date, mode, power, frequency, my location (if not at base).

My answer: A - power.

Correct!

### 59. Power restriction on the 4m band

Remember: throughout most bands the restriction is 400w, with some notable exceptions such as the 6m and 4m bands.

My answer: C - 50w

Correct answer: D - 25w

### 60. License terms

Review https://www.comreg.ie/?dlm_download=amateur-station-licence-guidelines first - it's only 32 pages long.

My answer: C - licenses once granted are in fact valid for life.

Correct!

## Section 2 summary

20 / 30 = 66%
