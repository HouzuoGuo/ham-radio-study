# References

Based on IRTS course guide: https://www.hamradio.ie/course-guide/intro/course_guide.html

## Mobile station suffixes

- `/M` - land-based mobile, 50W max or 25W max on 70cm.
- `/MM` - maritime mobile, 10W max.

Mandatory location reporting:

- Report location at the beginning and end of a contact with each station. AND
- Every 30 minutes.

## IARU bands and secondary allocations

IARU regions:

- Region 1 - Europe & Russia & Africa.
- Region 2 - North & South America.
- Region 3 - Asia & Australia.

Region 1's band plan (https://www.iaru-r1.org/wp-content/uploads/2021/06/hf_r1_bandplan.pdf)

On HF:

- 160m - 1810 KHz to 2000 KHz - 190KHz
- 80m - 3500 KHz to 3800 KHz - 300KHz
- 60m - 5351.5 KHz to 5366.5 KHz - 15KHz (new since 2015, secondary allocation)
- 40m - 7000 KHz to 7200 KHz - 200KHz
- 30m - 10100 KHz to 10150 KHz - 50KHz (WARC)
- 20m - 14000 KHz to 14350 KHz - 350KHz
- 17m - 18068 KHz to 18168 KHz - 100KHz (WARC)
- 15m - 21000 KHz to 21450 KHz - 450KHz
- 12m - 24890 KHz to 24990 KHz - 100KHz (WARC)
- 10m - 28000 KHz to 29700 KHz - 1700KHz

VHF and above:

- 6m - 50000 KHz to 54000 KHz - 4000 KHz
- 4m - 70000 KHz to 70500 KHz - 500 KHz
- 2m - 144 MHz to 146 MHz - 2 MHz
- 70cm - 430 MHz to 440 MHz - 10 MHz

WARC bands have a total bandwidth of 100KHz or less.

## ITU emission designators

Links:

- https://en.wikipedia.org/wiki/Types_of_radio_emissions
- ITU Emission Designators: https://www.comreg.ie/media/dlm_uploads/2015/12/ComReg0834.pdf

The three letters are:

- The carrier: DSB - A, FM - F, SSB - J, etc.
- Natural of signal: single ch digital - 1, single ch analog - 3, etc.
- Type of information: audio - E, data - D, video - F, etc.

Popular modes:

- Voice on AM: A3E
- Voice on FM: F3E
- Voice on SSB: J3E
- CW: A1A

## Maximum Effective Isotropic Radiated Power (EIRP) of bands

(Amateur station course guide, 2014)

400 watts:

- Lower portion of 160m
- 80m throughout 10m
- 2m
- Upper portion of 70cm

The other frequency ranges have a power limit of 10w or 50w.

## Logbook keeping

Logbook keeping is mandatory, each entry must include:

- Date & time.
- Frequency & mode & power.
- Caller and responder's callsigns.
- Location (if not at base).

## The governing bodies - ITU, IARU, CEPT, ComReg

- ITU - International telecommunication union
- IARU - International amateur radio union
- CEPT - European conference of postal and telecommunication
- ComReg - The Irish commission for communications regulation.

When visiting other CEPT countries, put the destination country's callsign prefix in front of my own, e.g. `OH/EI1234`.

## The composition of a callsign

- 2 character region - Ireland EI, Finland OH, Denmark OZ, etc.
  * Must contain a letter.
- 1 digit - could be region (e.g. OH2 for Uusimaa).
- 1-4 characters.
  * Must end with a letter.

Irish callsigns:

- EI - the mainland.
- EJ - offshore islands.

## Calling procedure

Voice:

- "Is the frequency in use, from MyCallsign."
- CQ CQ + destination station/area (if any) + from MyCallsign.

Morse:

- CQ CQ + destination station/area (if any) + DE MyCallsign.
- K (anyone may reply) or KN (called station should reply).

## Q codes

- General: QRA (name), QRB (distance), QTE (bearing).
- Bad signal: QRM (interference), QRN (static), QSB (fade).
- Power: QRP (low), QRO (high).
- Calls: QRZ (who's calling?), QSL (please ack). QTH (location).

## RST - readability, strength, and tone

"59" - perfect readability, S9.

## Construction of common filters

- Low pass filters - R in series, C in parallel.
  * More current flows through R when C's reactance is high (i.e. low frequency).
- High pass filters - R in parallel, C in series.
  * More current flows through R when C's reactance is low (i.e. high frequency).
- Band pass filter - combo of C in parallel & C in series.
  * The parallel C performs low pass and the series C performs high pass.

Common usage:

- Use low pass filters on HF.
- Use band pass filters on VHF and above.

## Dealing with undesirable common mode current

Common mode current is "portion of conductor currents that are unmatched with the exactly opposite and equal magnitude currents".

If it flows on the braid of shielded cables, try looping the cable in ferrite chokes.

## Regarding safety practices and antenna tower

- Typical resistance from hand to foot: 500 ohms.
- Eyes can be damaged through heating by RF! Handle active waveguides with extra care.

For an antenna tower:

- On a dipole, high voltage is present at the tips, and high current at the feed point in the centre.
- Guy rope - 70% of the mast height out from the base.
- Mast - twice their own height from power lines and nearby properties.
- Ground all legs with a separate rod - each rod being >2 metres long and >1CM in diametre.
  * Bond all rods together.
- Fit static dischargers in antenna feeders.

## Impedance and capacitance

Impedance is the combination of reactance and resistance: Z = Sqrt(R^2 + X^2)

- In the absence of resistance, Z = X.
- In the absence of reactance, Z = R.
- Capacitance introduces a downward slope to impedance, inductance introduces an upward slope.

When reactance and resistance are in parallel (instead of series): Z = (R x X) / Sqrt(R^2 + X^2)

Capacitors:

- Capacitance = K (dialetric constant) x A (area) / d (distance)
- Capacitance in series: Total = 1 / (1 / C1 + 1 / C2 + ...)
- Capacitance in parallel: Total = C1 + C2 + ...
- Reactance: X = 1 / (2 x pi x f x C)

Inductors:

- Inductor in series: Total = L1 + L2 + ...
- Inductor in parallel: Total = 1 / (1 / L1 + 1 / L2 + ...)
- Reactance: X = 2 x pi x f x L
  * Like inverse capacitance.

Tuned circuit:

- L & C in series: low impedance at resonant frequency.
- L & C in parallel: high impedance at resonant frequency.
- High Q: narrow bandwidth, and low Q means wide bandwidth.
- Typical bandwidth measurement: "half-power bandwidth", which is at -3dB, when voltage drops to ~0.7 of the voltage at resonance.
- Quartz crystal is similar to a tuned circuit and can be modelled as R + L + C in series plus a C in parallel.
  * Low impedance at resonant frequency.
  * Capacitance prevails below the resonant frequency (high impedance).
  * Inductance prevails above the resonant frequency (high impedance) up till a certain point (parallel resonant frequency).
  * Beyond parallel resonant frequency the impedance lowers once again.
    - Parallel L & C prevail, which exhibits low impedance at higher frequency.

## Diode

Conventional current flow:

- Conventional current flow departs from positive (anode) and drains into negative (cathode).
- Diode marking goes like: anode (conventional positive) - `I>|` - cathode (conventional negative)
  * The conventional negative side is often marked with a bar.

Characteristics:

- Silicon diode: forward drop 0.6v, significantly reduces reverse current.
  * Block reverse current at slow switching speed.
- Germanium diode: forward drop 0.3v, responds to forward and reverse current with similar linearity.
  * Symmetrical current response in both directions.
  * Sometimes used as an AM detector.
- Zener diode: forward drop 0.6v, rapidly responds to current demand at breakdown voltages in the reverse direction; low ripple under varying load.
  * Useful for clamping voltage in reverse.
  * Useful for providing stable voltage at varying load.
- Schottky diode: forward drop 0.3v.
  * Block reverse current at fast switching speed. Also saves power due to the lower drop.
  
Common configuration:

- Silicone diodes in series: simple voltage divider regardless of load current.
  * Also increases peak inverse voltage rating.
  * Use a large parallel resister to better balance voltage.
  * Use a tiny capacitor to protect against transient voltage.
- Diodes in parallel: improve forward current rating.
  * Use a tiny resister in series to balance currents.

## Designing power supply

Rectify - convert AC to DC:

- Half wave: use a transformer to obtain the desired voltage, and then connect a diode in series.
- Full wave: use a transformer to obtain the desired voltage, tap to the middle of the winding, then use two diodes in series.
- Full wave bridge rectifier: use 4 diodes.

### Further optimisation

High voltage power supply:

- Consider the full wave rectifier design.
- Smooth output voltage with a small capacitor.
- Connect a bleeder resistor across the capacitor to bleed off potentially dangerously high voltage.
- Further smooth output voltage with an inductor.

Low voltage power supply:

- Consider the half wave rectifier design in combination with a zener diode.
  * Zener diode provides comparably more stable voltage at varying load.
- Smooth output voltage with a large capacitor.

## Amplify a signal

Amplifier classes:

- Class A - the conductor amplifies 360 degrees (100%) of the input signal, theoretically 50% efficient.
- Class B - each conductor amplifies 180 degrees (50%) of the input signal, about 65% efficient.
- Class AB - some of the conductor (collector) current flows in the inactive case, about 50% efficient.
  * A practical Class AB amplifier requires two transistors - each conducting 180% degree of the input signal.
  * Pre-biasing transistors forward using diodes and resistors: Vcc - R - D - D - R - G.
- Class C - the conductor only amplifies 90 degrees (25%) of the input signal, about 90% efficient.
  * Not suitable for audio applications, but useful for FM transmitter.

Use a tank circuit (parallel resonant) to complete the missing cycle in an amplifier. (TODO: how?)

Transistor configuration:

- Common emitter - higher output impedance
  * Collector: large V.
  * Base: input signal.
  * Emitter: grounded, with a parallel decoupling capacitor.
  * Output: between collector (large V) and ground (0).
- Common collector - lower output impedance
  * Collector: large V (signal ground).
  * Base: input signal.
  * Emitter: grounded, with a serial capacitor.
    - The emitter and base have identical signal voltage.
  * Output: between emitter's serial capacitor and ground.
- Common base - higher output impedance
  * Input goes to emitter.
  * Output comes from collector.

### Components

- NPM transistor: when base is switched on, conventional current flows from collector to base and emitter. Arrow shows the current direction.
- PNP transistor: when base is switched off, conventional current flows from emitter to collector.
- Junction field effect transistors: magnify current from source to drain (N-channel) by a small increase of gate voltage.
- Valves (vacuum tubes): heated cathode (conventional negative) to emit electrons toward anode (conventional positive), grid voltage controls the gain.

Simple audio amplifier (common-emitter with higher output impedance):

- Connect a single NPN diode across power supply.
- Connect input to gate, through larger resistors.
  * Larger compared to the resisters on the collector's side.
- Filter the output between collector and emitter through a low-pass filter (capacitor + resister in parallel).

Simple radio frequency amplifier:

- Use a junction field effect transistor.
  * And I barely if at all understand rest of the schematics.

## Power and signal processing

Ireland mains electricity supply:

- 230VAC RMS - peek at 330V, peek-to-peek at 660V.
- 50Hz at period of 20ms.

The decibel scale of signal amplification:

- 0dB - no gain, no loss.
- -3dB - half.
- 3dB - double.
- 6dB - quadruple.
- 10dB - 10 times.
- 20dB - 100 times.

The decibel scale of signal strength:

- 10dBm - 10mW.
- 20dBm - 100mW.
- 30dBm - 1W.
- 40dBm - 10W.

Digital signal processing:

- Analogue filter for the input.
- Analogue to digital conversion.
  * The sample rate needs to be at least 2x the highest signal frequency.
- Digital processing logic.
- Digital to analogue conversion.
- Analogue filter for the output.

To create an oscillator (sine wave generator):

- Resonant (tuned) circuit acting as filter.
- Amplify.
- Feed back to the input.

## ComReg license terms

Link: https://www.comreg.ie/?dlm_download=amateur-station-licence-guidelines

Key takeaways:

- Keep ComReg updated with the license details.
- The license lasts a lifetime.
- There are two license classes: class 1 requires morse skills, class 2 does not.
  * Class 1 call-signs are shorter ("EI9AB").
- Repeaters are "automatic stations" and are only granted to club license holders.
  * APRS relays are exempt.
  * Repeater call-signs follow a strict convention - e.g. EI2TRR - 2m, Three Rock, voice.
- Land base station - ID myself at the beginning, the end, and every 30 minutes.
- Marine station - ID myself + position reporting every 30 minutes.

## Memorise the band plan

Special digits: 8, 2, 3, 7, 4-5-6.

- 160m: 1810 - 2000
- 80m: 3500 - 3800
- 40m - 7000 - 7200
- 20m - 14000 - 14350
  * 15m - 21000 - 21450
- 10m - 28000 - 29700
- 6m - 50000 - 54000
- 4m - 70000 - 70500
- 2m - 144000 - 146000
- 70cm - 432000 - 440000

## Memorise the power limit

General rules:

- General power limit: 400 watts.
  * Special - mobile: 50w
  * Special - marine: 10w.
- Special - 160m: first 40khz 400w, next 10w.
- 80m: 400w
- 40m: 400w
- 20m: 400w
  * 15m: 400w
- 10m: 400w
- Special - 6m (secondary allocation): first 2mhz 100w, next 50w.
- 4m (secondary allocation): 50w
  * Special - mobile: 25w
- 2m: 400w
- 70cm: 400w
