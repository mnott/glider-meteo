# 10.3 METAR and SPECI - Detailed Guide

## Overview

**METAR** (METeorological Aerodrome Report) and **SPECI** (Special Reports) are standardized coded weather observation reports from aerodromes. These reports provide current weather conditions essential for flight planning and operations.

**📖 Reference**: [Lesson 3 Part 3 - METAR](slides/meteo3_part-101-133.pdf#page=16) (Page 116-117)

## Why This Matters for Glider Pilots

- **Current conditions** - METAR shows what's ACTUALLY happening right now
- **Every 30 minutes** - frequent updates (Switzerland: :20 and :50 past each hour)
- **Standardized worldwide** - same format at every airport globally
- **Exam critical** - you MUST be able to decode METAR for the exam
- **Flight safety** - tells you if conditions are suitable for takeoff/landing
- **VFR requirements** - cloud base and visibility are key VFR parameters

**Important**: Wind direction in METAR is referenced to **GEOGRAPHIC NORTH** (not magnetic north, unlike ATC communications which use magnetic north).

## METAR vs SPECI

### METAR
- **Routine observation** issued every 30 minutes
- In Switzerland: issued at XX:20 and XX:50 UTC
- Example: At 08:20 UTC, 08:50 UTC, 09:20 UTC, etc.

### SPECI
- **Special observation** issued when significant changes occur between routine METARs
- Triggers include:
  - Wind shift ≥30° and speed ≥10 kt
  - Visibility changes significantly
  - Cloud base changes significantly
  - Weather phenomena begin/end (rain, snow, thunderstorm)
  - Temperature changes rapidly

## Complete METAR Structure

### Example METAR (from slides)
```
METAR LSGG 160650Z AUTO 26009KT 9999 RA FEW010 OVC040 03/02 Q1017 NOSIG=
```

Let's decode each element:

### 1. Message Type
**METAR** or **SPECI**

### 2. Station Identifier (ICAO Code)
- **LSGG** = Geneva (Genève-Cointrin)
- **LSZH** = Zurich
- **LSGS** = Sion
- **LSZB** = Bern-Belp
- **LSZR** = St. Gallen-Altenrhein

**Swiss aerodromes start with LS**

### 3. Date and Time
**Format**: `DDHHMM**Z**`
- **DD**: Day of month (01-31)
- **HH**: Hour (00-23 UTC)
- **MM**: Minute (00-59)
- **Z**: Zulu time (UTC)

**Example**: `160650Z` = 16th day, 06:50 UTC

### 4. AUTO or COR
- **AUTO**: Automated station (no human observer)
- **COR**: Corrected report (replaces earlier erroneous report)
- *(Omitted if human-observed)*

### 5. Wind Information

**Format**: `DDDSSKT` or `DDDSSGSSGKT` or `VRB02KT`

**DDD**: Direction in degrees (true north, rounded to nearest 10°)
- `270` = west wind (FROM 270°)
- `090` = east wind (FROM 090°)
- `360` = north wind (FROM 360°/000°)
- `VRB` = variable direction

**SS**: Speed in knots
**GGG**: Gust speed (if present)
**KT**: Knots

**Examples**:
- `26009KT`: Wind from 260° at 9 knots
- `09015G25KT`: Wind from 090° at 15 kt, gusting to 25 kt
- `VRB01KT`: Variable direction, 1 kt (essentially calm)
- `00000KT`: Calm (0 kt)

**Variable Direction**:
- `VRB` used when wind ≤3 kt (essentially calm)
- If direction varies ≥60° with speed ≥3 kt: `120V180` appended

**Example**: `15008KT 120V180` = Wind 150° at 8 kt, varying between 120° and 180°

### 6. Visibility

**Format**: Meters (or `9999` for 10 km or more)

**Examples**:
- `9999`: 10 km or more
- `8000`: 8000 meters (8 km)
- `5000`: 5000 meters (5 km)
- `1200`: 1200 meters (1.2 km)
- `0400`: 400 meters

**Special Case**: `CAVOK` (see below)

### 7. Weather Phenomena

**Format**: Intensity + Descriptor + Precipitation/Obscuration/Other

**Intensity**:
- `-`: Light (e.g., `-RA` = light rain)
- *(no prefix)*: Moderate
- `+`: Heavy (e.g., `+TSRA` = heavy thunderstorm with rain)

**Common Descriptors**:
- `SH`: Showers (e.g., `SHRA` = rain showers)
- `TS`: Thunderstorm (e.g., `TSRA` = thunderstorm with rain)
- `FZ`: Freezing (e.g., `FZRA` = freezing rain)
- `BL`: Blowing (e.g., `BLSN` = blowing snow)

**Precipitation Types**:
- `RA`: Rain (pluie)
- `SN`: Snow (neige)
- `DZ`: Drizzle (bruine)
- `GR`: Hail (grêle)
- `GS`: Small hail/snow pellets (grésil)

**Obscuration**:
- `FG`: Fog (brouillard) - visibility <1 km
- `BR`: Mist (brume) - visibility 1-5 km
- `HZ`: Haze (brume sèche)
- `FU`: Smoke (fumée)

**Other Phenomena**:
- `TS`: Thunderstorm
- `SQ`: Squall (grain)
- `FC`: Funnel cloud/tornado
- `DS`: Duststorm
- `SS`: Sandstorm

**Examples**:
- `RA`: Moderate rain
- `-SHRA`: Light rain showers
- `+TSRA`: Heavy thunderstorm with rain
- `FZFG`: Freezing fog
- `BLSN`: Blowing snow

### 8. Clouds

**Format**: `AAAHHHH` (Amount + Height in hundreds of feet AGL)

**Amount Codes**:
- **FEW**: Few = 1-2 oktas (1/8-2/8 sky coverage)
- **SCT**: Scattered = 3-4 oktas (3/8-4/8)
- **BKN**: Broken = 5-7 oktas (5/8-7/8)
- **OVC**: Overcast = 8 oktas (full coverage)
- **NSC**: No Significant Cloud (used with AUTO)
- **NCD**: No Cloud Detected (used with AUTO)

**Height**: In hundreds of feet **above aerodrome level (AGL)**
- `010` = 1000 ft AGL
- `025` = 2500 ft AGL
- `040` = 4000 ft AGL
- `100` = 10,000 ft AGL

**Cloud Type** (if significant):
- `CB`: Cumulonimbus
- `TCU`: Towering Cumulus

**Examples**:
- `FEW010`: Few clouds at 1000 ft AGL
- `SCT025`: Scattered clouds at 2500 ft AGL
- `BKN040`: Broken layer at 4000 ft AGL
- `OVC015`: Overcast at 1500 ft AGL
- `FEW020CB`: Few cumulonimbus at 2000 ft AGL
- `SCT030 BKN080`: Scattered at 3000 ft, broken at 8000 ft

**Multiple layers**: Listed in ascending order

**CAVOK** (Ceiling And Visibility OK):
Used instead of visibility + clouds + weather when **ALL** of the following are met:
- Visibility ≥10 km
- No clouds below 5000 ft (1500 m) AGL
- No cumulonimbus at any level
- No significant weather phenomena

### 9. Temperature and Dewpoint

**Format**: `TT/TD` or `MTT/MTD`

- **TT**: Temperature in °C
- **TD**: Dewpoint in °C
- **M**: Prefix for minus (negative)

**Examples**:
- `03/02`: Temperature +3°C, Dewpoint +2°C
- `M01/M02`: Temperature -1°C, Dewpoint -2°C
- `15/10`: Temperature +15°C, Dewpoint +10°C
- `M05/M08`: Temperature -5°C, Dewpoint -8°C

**Temperature-Dewpoint Spread**:
- **Small spread (0-2°C)**: High humidity, fog/low cloud likely
- **Large spread (>5°C)**: Dry air, good visibility

**Dewpoint = Temperature**: Air is saturated, fog/cloud present

### 10. Pressure (QNH)

**Format**: `Qhhhh` (hectopascals/millibars)

**Examples**:
- `Q1013`: QNH 1013 hPa (standard pressure)
- `Q1023`: QNH 1023 hPa (high pressure)
- `Q0995`: QNH 995 hPa (low pressure)

**Note**: Some countries use inches of mercury (e.g., `A2992` = 29.92 inHg)

### 11. Supplementary Information

**NOSIG** (No Significant Change):
- No significant changes expected in next 2 hours

**RMK** (Remarks):
- Additional information (format varies by country)

**Example Complete METAR**:
```
METAR LSGG 160650Z AUTO 26009KT 9999 RA FEW010 OVC040 03/02 Q1017 NOSIG=
```

**Full Decode**:
- **METAR**: Routine observation
- **LSGG**: Geneva airport
- **160650Z**: 16th day, 06:50 UTC
- **AUTO**: Automated observation
- **26009KT**: Wind from 260° (west) at 9 knots
- **9999**: Visibility 10 km or more
- **RA**: Moderate rain
- **FEW010**: Few clouds at 1000 ft AGL
- **OVC040**: Overcast at 4000 ft AGL
- **03/02**: Temperature +3°C, Dewpoint +2°C (spread 1°C = high humidity)
- **Q1017**: QNH 1017 hPa
- **NOSIG**: No significant change expected
- **=**: End of message

## METAR for Exam Practice

### Practice Examples

**Example 1**:
```
LSGS 110620Z AUTO VRB01KT CAVOK M01/M02 Q1023
```

**Decode**:
- LSGS = Sion
- 11th day, 06:20 UTC
- Automated
- Variable wind 1 kt (calm)
- CAVOK (visibility ≥10 km, no significant clouds, no weather)
- Temperature -1°C, Dewpoint -2°C
- QNH 1023 hPa

**Example 2**:
```
LSZH 151620Z 27015G28KT 8000 -SHRA SCT015 BKN025CB 12/09 Q1008 TEMPO TSRA
```

**Decode**:
- LSZH = Zurich
- 15th day, 16:20 UTC
- Wind from 270° at 15 kt, gusting to 28 kt
- Visibility 8000 m (8 km)
- Light rain showers
- Scattered clouds at 1500 ft AGL
- Broken cumulonimbus at 2500 ft AGL
- Temperature +12°C, Dewpoint +9°C
- QNH 1008 hPa (low pressure)
- Temporary thunderstorms with rain expected

### Training Resources

**Online Practice**:
- MétéoSuisse: https://www.meteosuisse.ch - Real METARs for Swiss airports
- AllMetSat: https://fr.allmetsat.com/metar-taf/suisse-italie-nord.php - Global METARs
- OGIMET: https://www.ogimet.com - Worldwide METAR archive

**Exam Tips**:
1. **Practice daily** - Decode 2-3 METARs every day
2. **Focus on cloud base** - Most common exam trap (it's in feet AGL, not MSL!)
3. **Know the codes** - Memorize weather phenomena abbreviations
4. **Check dewpoint spread** - Indicates humidity and fog risk
5. **Wind direction** - Geographic north (not magnetic)
6. **CAVOK conditions** - All three criteria must be met

## Information Sources

**Where to Find METARs**:
- **MeteoSuisse**: Official Swiss weather service - https://www.meteosuisse.ch
- **FlugWetter.de**: German aviation weather portal
- **Sky Briefing Services**: Commercial pre-flight briefing
- **ATIS**: Automated Terminal Information Service (by radio at larger airports)

## Frequency and Validity

**METAR Issuance**:
- **Every 30 minutes** at certified airports
- **Switzerland**: XX:20 and XX:50 UTC
- Example: 06:20, 06:50, 07:20, 07:50, etc.

**SPECI Issuance**:
- **As needed** when significant changes occur
- Can be issued at any time

**Validity**:
- METAR is valid for approximately **1 hour** (until next METAR)
- Conditions can change rapidly - always check latest

---

## Questions & Answers

### Q7: Selon le METAR de l'aérodrome de Sion suivant: LSGS 110620Z AUTO VRB01KT CAVOK M01/M02 Q1023

**Question (FR)**: Selon le METAR de l'aérodrome de Sion suivant: LSGS 110620Z AUTO VRB01KT CAVOK M01/M02 Q1023

**Question (EN)**: According to the following METAR from Sion aerodrome: LSGS 110620Z AUTO VRB01KT CAVOK M01/M02 Q1023

**Options**:
- A) Le vent est calme / The wind is calm
- B) Le vent est d'environ 10 kt à Sion / The wind is about 10 kt at Sion
- C) Il y a des bancs de nuages bas en dessus de la piste / There are patches of low clouds above the runway
- D) Le point de rosée est de -1°C / The dewpoint is -1°C

**Réponse (FR)**: A) Le vent est calme

**Answer (EN)**: A) The wind is calm

**Explication détaillée**:

Let's decode this METAR step by step:
- **LSGS**: Sion aerodrome
- **110620Z**: 11th day of month, 06:20 UTC
- **AUTO**: Automated observation (no human observer)
- **VRB01KT**: Variable direction, 1 knot wind speed
- **CAVOK**: Ceiling And Visibility OK (visibility ≥10 km, no clouds below 5000 ft, no CB, no significant weather)
- **M01/M02**: Temperature minus 1°C, Dewpoint minus 2°C
- **Q1023**: QNH 1023 hPa

**Why A is correct**: VRB01KT means the wind is variable in direction with a speed of only 1 knot. This is essentially calm wind. VRB (variable) is used when wind speed is ≤3 kt because the direction is meaningless at such low speeds.

**Why B is wrong**: The wind is 1 kt, not 10 kt. If it were 10 kt, it would read VRB10KT or have a specific direction like 27010KT.

**Why C is wrong**: CAVOK means there are NO clouds below 5000 feet AGL and no cumulonimbus at any altitude. There are no low clouds above the runway.

**Why D is wrong**: The dewpoint is **M02**, which means -2°C (not -1°C). The temperature is M01 = -1°C. The temperature-dewpoint spread is only 1°C, indicating high humidity.

### Q10: En Suisse, la base des nuages dans un METAR est indiquée en

**Question (FR)**: En Suisse, la base des nuages dans un METAR est indiquée en

**Question (EN)**: In Switzerland, cloud base in a METAR is indicated in

**Options**:
- A) mètres au-dessus du niveau de l'aérodrome / meters above aerodrome level
- B) pieds au-dessus du niveau de l'aérodrome / feet above aerodrome level
- C) pieds au-dessus du niveau de la mer / feet above sea level
- D) mètres au-dessus du niveau de la mer / meters above sea level

**Réponse (FR)**: B) pieds au-dessus du niveau de l'aérodrome

**Answer (EN)**: B) feet above aerodrome level

**Explication détaillée**:

This is a critical point that many students get wrong on the exam!

**METAR cloud heights are ALWAYS reported in**:
- **Feet** (NOT meters)
- **Above Ground Level (AGL)** = Above aerodrome elevation (NOT MSL = above sea level)
- **Hundreds of feet** (the number is divided by 100)

**Examples**:
- `BKN025` = Broken layer at **2500 feet above the airport elevation**
- `OVC040` = Overcast at **4000 feet above the airport elevation**
- `SCT015` = Scattered at **1500 feet above the airport elevation**

**Why this matters**:
- **Sion airport** elevation: 482 m (1581 ft) MSL
- If METAR shows `BKN025` (2500 ft AGL):
  - Cloud base above airport: 2500 ft
  - Cloud base MSL: 1581 + 2500 = 4081 ft MSL
  - Cloud base in meters AGL: 2500 × 0.3048 = 762 m AGL

**For glider pilots**: You need to know the airport elevation to calculate cloud base MSL for cross-country planning. Cloud base AGL tells you clearance from runway, but cloud base MSL tells you working altitude.

**International standard**: This is not just Switzerland - it's the **worldwide ICAO standard**. All countries report METAR cloud heights in feet AGL.

**Common exam trap**: Students often confuse this with:
- Flight levels (which ARE above sea level)
- Altimeter settings (which reference sea level)
- But METAR clouds are AGL!

---

*Related topics*: [TAF](13_taf_detailed.md), [Weather Charts](14_weather_charts.md), [Visibility](06_visibility.md)
