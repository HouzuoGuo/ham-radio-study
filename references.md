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
- 2m - 144 MHz to 145 MHz - 2 MHz
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

- Bad signal: QRM (interference), QRN (static), QSB (fade).
- Power: QRP (low), QRO (high).
- Calls: QRZ (who's calling?), QRZ (please ack). QTH (location).

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

TODO - Section B, resonance and tuned circuits.
