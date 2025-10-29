# Meteorological Information (Information météorologique)

## Overview
Access to current and forecast weather information is essential for safe flight operations. Switzerland and Europe have extensive observation networks and standardized reporting formats that pilots must understand.

**📖 Reference**: [Lesson 3 Slides - Weather Information](slides/meteo3_part-051-100.pdf#page=47)

## Why This Matters for Glider Pilots

- **VFR flight requires good weather** - you need accurate information
- **Weather changes** - current observations show what's actually happening
- **Forecasts** help plan flights and identify hazards
- **Standard formats** (METAR, TAF) used worldwide
- **Graphical products** show big picture patterns
- **Multiple sources** provide cross-validation

**Critical**: Pilots are legally required to obtain weather information before flight. But more importantly, good weather information saves lives.

## Observation Network (Slide 99-100)

### Ground Stations (Stations de mesure au sol)
**MétéoSuisse Network:**
- 160+ automatic stations across Switzerland
- Measure: temperature, pressure, wind, humidity, precipitation, sunshine
- Reports every 10 minutes
- Dense coverage - high resolution

**Airport Stations:**
- METAR observations from all certified airports
- Human observers at major airports
- Automated (AUTO) at smaller fields
- Every 30 minutes (Switzerland: :20 and :50 past hour)

### Upper Air Observations (Radiosondage)

**Payerne Station:**
- Balloon-sonde launched twice daily (00 and 12 UTC)
- Measures temperature, pressure, humidity, wind up to 30+ km altitude
- Provides vertical profile of atmosphere
- Critical for forecasting

### Radar Network (Radars météorologiques)

**Five Radars in Switzerland:**
- Detect precipitation (location and intensity)
- Update every 5 minutes
- Cover entire country
- Can see developing thunderstorms

### Webcams
- Visual confirmation of conditions
- Cloud cover, visibility
- Available online for many locations

## METAR - Aviation Weather Report

### Format and Meaning

**METAR** = Meteorological Aerodrome Report (current observation)

**Example from Slide 100:**
```
LSGS 110620Z AUTO VRB01KT CAVOK M01/M02 Q1023
```

**Decode:**
- **LSGS**: Sion airport
- **110620Z**: 11th day, 06:20 UTC
- **AUTO**: Automated station (no human observer)
- **VRB01KT**: Variable direction, 1 knot wind
- **CAVOK**: Ceiling And Visibility OK (vis ≥10km, no clouds <1500m/5000ft, no significant weather)
- **M01/M02**: Temperature -1°C, Dewpoint -2°C (M = minus)
- **Q1023**: QNH 1023 hPa

### Wind Reporting

**Format**: `DDDSSKT` or `DDDSSGSKT`
- **DDD**: Direction (magnetic, rounded to nearest 10°)
- **SS**: Speed in knots
- **G**: Gust (if present)
- **KT**: Knots

**Examples:**
- `27015KT`: Wind 270° at 15 kt
- `VRB02KT`: Variable direction (calm), 2 kt
- `09008G18KT`: Wind 090° at 8 kt gusting to 18 kt

**VRB** (variable): Used when:
- Wind ≤ 3 kt (essentially calm), or
- Direction varying and speed ≥ 3 kt: shows as `VRB05KT`, or
- Direction varying ≥60° with speed ≥3 kt: shows as `120V180`

### Cloud Reporting

**Format**: `AAAHHHH`
- **AAA**: Amount (FEW/SCT/BKN/OVC)
- **HHH**: Height in hundreds of feet AGL

**Amount Codes:**
- **FEW**: Few (1-2 oktas, 1/8-2/8 coverage)
- **SCT**: Scattered (3-4 oktas, 3/8-4/8)
- **BKN**: Broken (5-7 oktas, 5/8-7/8)
- **OVC**: Overcast (8 oktas, full coverage)

**CAVOK**: Used when ALL of:
- Visibility ≥ 10 km
- No clouds below 1500m (5000ft) AGL
- No CB
- No significant weather

**Examples:**
- `SCT025 BKN040`: Scattered clouds at 2500 ft, Broken at 4000 ft
- `FEW010 OVC020`: Few at 1000 ft, Overcast at 2000 ft

### Visibility

- Reported in meters if < 10 km
- **CAVOK** if ≥ 10 km (and other criteria met)

**Examples:**
- `9999`: 10 km or more (but not CAVOK due to other factors)
- `5000`: 5 km visibility
- `0800`: 800 m visibility

### Weather Phenomena

**Common Codes:**
- **RA**: Rain
- **SN**: Snow
- **FG**: Fog (visibility < 1 km)
- **BR**: Mist (visibility 1-5 km)
- **TS**: Thunderstorm
- **SH**: Showers

**Intensity:**
- **-**: Light (e.g., `-RA` = light rain)
- No prefix: Moderate
- **+**: Heavy (e.g., `+TSRA` = heavy thunderstorm with rain)

### Temperature and Dewpoint

**Format**: `TT/TD` or `MTT/MTD`
- **TT**: Temperature in °C
- **TD**: Dewpoint in °C
- **M**: Prefix for minus (negative temperature)

**Example**: `M01/M02`
- Temperature: -1°C
- Dewpoint: -2°C
- Spread: 1°C (small spread = high humidity)

**What this means**: Small temperature-dewpoint spread indicates air near saturation - fog/low cloud likely if temperature drops.

## TAF - Terminal Aerodrome Forecast

### Format and Meaning

**TAF** = Aerodrome Forecast (prediction for next 9-30 hours)

**Example from Slide 100:**
```
TAF LSGS 110525Z 1106/1115 VRB02KT CAVOK
     BECMG 1108/1110 BKN100
     BECMG 1113/1115 RA
```

**Decode:**
- **TAF LSGS**: Forecast for Sion
- **110525Z**: Issued 11th day, 05:25 UTC
- **1106/1115**: Valid from 11th 06:00Z to 11th 15:00Z (9 hours)
- **VRB02KT CAVOK**: Initial conditions - calm, CAVOK
- **BECMG 1108/1110**: Becoming (gradual change) between 08:00-10:00Z
- **BKN100**: Broken clouds at 10,000 ft
- **BECMG 1113/1115**: Becoming between 13:00-15:00Z
- **RA**: Rain

**Interpretation**: Starts nice (CAVOK), clouds move in mid-morning, rain by afternoon.

### Change Indicators

**BECMG** (becoming):
- Gradual change over the time period specified
- End state reached by end of period

**TEMPO** (temporary):
- Temporary fluctuations
- Conditions last < 1 hour each occurrence
- Occur during specified period

**Example:**
```
TAF ... 1106/1118 SCT040
    TEMPO 1112/1116 BKN020
```
- Base forecast: Scattered at 4000 ft
- Between 12:00-16:00Z: Temporary broken at 2000 ft (then returns to SCT040)

### Frequency (Slide 100 table)

**METAR:**
- Every 30 minutes
- Switzerland: :20 and :50 past each hour

**TAF:**
- Every 3 hours at major airports (LSZH, LSGG)
- 00/03/06/09/12/15/18/21 UTC
- Regional airports: 06/09/12/15/18 UTC
- Military: 10/17 UTC

## GAFOR - Swiss VFR Area Forecast

**GAFOR** = General Aviation Forecast for Organized Routes

**Purpose**: Simplified forecast for VFR flight between Swiss regions

**Routes**: Numbered routes between major airports/areas (Slide 10 - route 51: Basel-Grenchen shown as example)

**Code Format**: Three letters indicating cloud base and visibility

**Color Code:**
- **Green (G)**: GOOD - Base >1500m AGL, Vis >8 km
- **Yellow (A)**: ATTENTION - Base 600-1500m, Vis 5-8 km
- **Orange (O)**: RISKY - Base 300-600m, Vis 3-5 km
- **Red (R)**: IMPOSSIBLE - Base <300m or Vis <3 km

**Time Blocks**: Usually 2-hour periods

### Example (Q9 from QA):

**Route 51 (Basel-Grenchen) valid 04-10 UTC:**
- 04-06 UTC: Shows conditions
- 06-08 UTC: Different conditions (possibly RED = route closed)
- 08-10 UTC: Improved to allow VFR

**Q9 Answer**: D) Between 08-10 UTC, cloud and visibility conditions will make VFR flight possible

## Weather Charts

### Low-Level Significant Weather Chart (Low-level SWC)

**Purpose**: Shows significant weather for low-level flight (surface to FL150/200)

**Information Depicted** (Slides 12-13, Q11):
- Fronts (cold, warm, occluded)
- Cloud areas with bases/tops
- Precipitation areas
- Icing levels and intensity
- Freezing level
- Visibility restrictions
- Wind arrows

**Q11 Example Elements:**
- Icing zones: e.g., "MOD ICE FL060-FL170" = Moderate icing FL060 to FL170
- Freezing level: Altitude where temperature = 0°C
- Cloud layers: Base and top altitudes
- Weather symbols: Rain, snow, fog, etc.

**Q11 Answers:**
- **B) Moderate icing FL060-FL170 over Swiss Plateau** ✓

### TEMSI Charts (Temperature and Significant Weather)

**TEMSI EUROC** (European Coverage) - Slide 14-15, Q12

**Elements Shown:**
- Pressure patterns (H/L)
- Fronts
- Jet streams (wind barbs)
- Cloud layers (coverage, type, FL)
- Precipitation areas
- Turbulence zones
- Icing areas

**Q12 Answer**: A) Cirrus layer FL220-FL350 covering 5-7 oktas from Pyrenees to Central Germany ✓

**Reading Tips:**
- Fronts: Same symbols as surface charts (blue=cold, red=warm, purple=occluded)
- Cloud coverage in oktas shown by shading
- Wind barbs show speed/direction at altitude

## Online Resources

**MétéoSuisse**: [www.meteosuisse.ch](https://www.meteosuisse.ch)
- Official forecasts
- Radar, satellite
- METAR/TAF
- Charts (SWC, TEMSI)

**MeteoBlue**: Detailed forecasts, soundings

**GAFOR**: Available through MétéoSuisse and briefing services

**Webcams**: Various providers (RoundShot, etc.)

## Pre-Flight Briefing Sequence

**Recommended Order:**

1. **Big Picture** - Synoptic charts
   - Pressure patterns
   - Fronts
   - General situation

2. **Regional Forecast** - Area forecasts
   - MétéoSuisse text forecast
   - GAFOR for your route

3. **Current Observations**
   - METAR for departure, destination, alternates
   - Radar (precipitation)
   - Webcams (visual confirmation)

4. **Detailed Forecast**
   - TAF for airports
   - Winds aloft
   - Charts (SWC, TEMSI)

5. **Special Hazards**
   - SIGMETs (significant meteorology)
   - AIRMETs (airmen's meteorological information)
   - NOTAMs for weather-related closures

## Decision Making

**Go/No-Go Factors:**
- Current weather suitable?
- Forecast for flight duration acceptable?
- Alternate options if weather deteriorates?
- Hazards (Cb, icing, low visibility) forecast?
- Personal minimums met? (Don't just fly to legal minimums!)

**During Flight:**
- Monitor weather changes
- Compare actual to forecast
- Have abort plan if conditions worsen

## Summary

**Key Principles:**
- Multiple information sources - use them all
- METAR = current, TAF = forecast
- GAFOR simplifies VFR route planning
- Charts show big picture
- Cloud base in METAR: feet AGL (Switzerland: use B answer for Q10)
- Understand the codes - they're standardized worldwide
- Weather information is free and readily available - use it!

---

## Questions & Answers

### Q7: Selon le METAR de l'aérodrome de Sion suivant: LSGS 110620Z AUTO VRB01KT CAVOK M01/M02 Q1023

**A) Le vent est calme** ✓ - The wind is calm
**B) Le vent est d'environ 10 kt à Sion** - Wind is about 10 kt
**C) Il y a des bancs de nuages bas en dessus de la piste** - Patches of low clouds above runway
**D) Le point de rosée est de -1°C** - Dewpoint is -1°C

**Answer**: A) Wind is calm (VRB01KT = variable 1 kt, essentially calm)

**Explanation**:
- VRB = variable direction (used when wind ≤3 kt or direction varying)
- 01KT = 1 knot (very light, essentially calm)
- CAVOK means no clouds below 5000 ft (not C)
- Dewpoint is M02 = -2°C (not -1°C, so D is wrong)

### Q8: D'après ce TAF émis pour l'aérodrome de Sion: TAF LSGS 110525Z 1106/1115 VRB02KT CAVOK BECMG 1108/1110 BKN100 BECMG 1113/1115 RA

**A) Il semble que les conditions s'améliorent pour voler** - Conditions seem to be improving
**B) Il devrait y avoir de la pluie à partir de l'après-midi** ✓ - Rain expected from afternoon
**C) Au départ, le ciel est couvert** - Initially sky is overcast
**D) Le vent devrait forcir à plus de 10 kt** - Wind should increase to >10 kt

**Answer**: B) Rain expected from afternoon (BECMG 1113/1115 RA means rain between 13:00-15:00 UTC = afternoon)

**Explanation**:
- TAF valid 06:00-15:00Z (1106/1115)
- Initial: CAVOK (not overcast, so C wrong)
- 08:00-10:00Z: Clouds move in (BKN100)
- 13:00-15:00Z: Rain (RA) - this is afternoon
- Wind remains VRB02KT throughout (not >10kt, so D wrong)
- Conditions deteriorate (not improve, so A wrong)

### Q9: Ce GAFOR valide de 04 à 10UTC indique que sur la route Basel-Grenchen (route 51):

**D) Entre 08 et 10UTC, les conditions de nébulosité et de visibilité rendront le vol à vue possible** ✓

**Answer**: D) Between 08-10 UTC, cloud and visibility conditions will make VFR flight possible

**Explanation**: Looking at the GAFOR chart for route 51 between Basel and Grenchen in the 08-10 UTC timeframe, conditions improve to allow VFR operations (likely showing green or yellow code indicating adequate cloud base and visibility for VFR flight).

### Q10: En Suisse, la base des nuages dans un METAR est indiquée en

**B) pieds au-dessus du niveau de l'aérodrome** ✓ - Feet above aerodrome level

**Answer**: B) Feet above aerodrome level (AGL - Above Ground Level)

**Explanation**: METAR cloud heights are ALWAYS reported in feet AGL (above ground level of the airport), never MSL (above sea level) and never in meters. This is the international standard. So BKN025 = broken layer at 2500 feet above the airport elevation.

### Q11: D'après la carte Low-level SWC ci-dessous:

**B) Il y a du givrage modéré entre le FL060 et le FL170 sur le Plateau suisse** ✓

**Answer**: B) There is moderate icing between FL060 and FL170 over the Swiss Plateau

**Explanation**: The Low-level SWC chart shows icing zones with their intensity and altitude ranges. The notation would show something like "MOD ICE 060/170" indicating moderate icing between those flight levels over the specified area.

### Q12: Ce TEMSI EUROC indique que:

**A) qu'une couche de cirrus entre FL220 et FL350 couvre 5 à 7/8 du ciel sur une zone s'étendant des Pyrénées au centre de l'Allemagne** ✓

**Answer**: A) A layer of cirrus between FL220 and FL350 covers 5-7 oktas of sky over area from Pyrenees to Central Germany

**Explanation**: TEMSI charts show cloud layers with their type, altitude range, and coverage in oktas. The shaded area on the chart indicates the geographic extent, and the notation gives the cloud details.

---

*Related topics*: [Alpine Weather](05_alpine_weather_situations.md), [Thunderstorms](10_thunderstorms.md), [Visibility](06_visibility.md)
