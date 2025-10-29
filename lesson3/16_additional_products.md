# 10.2-10.4 Additional Meteorological Products

## Overview

Beyond the main products (METAR, TAF, GAFOR, charts), several additional meteorological products provide valuable information for flight planning and operations.

**📖 Reference**: [Lesson 3 Part 3 - Additional Products](slides/meteo3_part-101-133.pdf#page=1) (Pages 101, 121-130)

## Why This Matters for Glider Pilots

- **PIREP** - Real-time reports from other pilots (conditions actually encountered)
- **SIGMET/AIRMET** - Urgent warnings of significant weather hazards
- **Soundings** - Vertical atmospheric profiles (critical for wave/thermal forecasting)
- **Météogrammes** - Time-series forecasts for specific locations
- **Gradient maps** - Special wind situations (föhn, bise) prediction
- **Specialized tools** - AlpTherm, TopTherm for soaring-specific forecasts

## 10.2 PIREP - Pilot Reports (Informations de pilotes)

**📖 Reference**: Page 101

### What is PIREP?

**PIREP** = PIlot REPort (Rapport de pilote)

**Definition**: Weather observation report issued by a pilot describing atmospheric conditions encountered **during flight** or **after landing**.

### Purpose

- **Real-time ground truth** - Actual conditions, not forecast
- **Hazard alerts** - Turbulence, icing, CB locations pilots encounter
- **Verification** - Compare forecast to reality
- **Community support** - Help other pilots with current info

### How PIREP Works

**Process**:
1. **Pilot** encounters significant weather (good or bad)
2. **Transmits** report via radio to nearest **ATC** (Air Traffic Control)
3. **ATC** codes the message and sends it via communication networks
4. **Available** to other pilots, flight planners, and meteorological services

### PIREPs in Plain Language

Unlike METAR/TAF, PIREPs are transmitted in **clear language** (langage clair), not coded format.

**Example PIREP**:
"Geneva Control, HB-XYZ, position 20 km south of LSGG at FL095, encountering moderate turbulence, temperature minus 2, light icing."

**ATC would code this and disseminate** to other aircraft and Met services.

### What to Report

**Routine PIREPs**:
- Cloud bases and tops
- Visibility
- Temperature
- Wind (direction/speed at altitude)
- Icing (if any)

**Urgent PIREPs** (Special Air Report - AIREP):
- **Severe turbulence**
- **Moderate or severe icing**
- **Cumulonimbus** (CB) locations
- **Wind shear**
- **Volcanic ash**
- **Mountain wave** (severe)
- **Other hazards** affecting safety

### Direction Reference - CRITICAL

**All direction information given by air traffic control is referenced to MAGNETIC NORTH**, not true north.

**Example**: "Wind 270 magnetic at 30 knots" = From magnetic west (not true west)

### AIREP Example (from slides)

**📖 Reference**: Page 122

```
UAIY63 LIIB 241528
AIREP SPECIAL: A320 REPORTED MOD TURB AT FL360 OVER ORSOM AT 1526=
```

**Decode**:
- **UAIY63 LIIB**: Message routing header
- **241528**: 24th day, 15:28 UTC
- **AIREP SPECIAL**: Special pilot report (urgent)
- **A320**: Aircraft type (Airbus 320)
- **REPORTED**: Past tense - condition encountered
- **MOD TURB**: Moderate turbulence
- **AT FL360**: At flight level 360 (36,000 ft)
- **OVER ORSOM**: At waypoint ORSOM (navigation fix)
- **AT 1526**: At time 15:26 UTC

**Interpretation**: An Airbus A320 encountered moderate turbulence at 36,000 feet over waypoint ORSOM at 15:26 UTC.

**For gliders**: This particular report is at very high altitude (not relevant for gliding), but shows the format. Glider PIREPs would report lower altitudes and soaring-relevant conditions.

## SIGMET and AIRMET

**📖 Reference**: Page 121

### SIGMET - Significant Meteorological Information

**Purpose**: Warns of **hazardous weather** affecting aircraft safety

**Coverage**:
- **Altitude**: Surface to FL250 (for most phenomena)
- **Area**: FIR (Flight Information Region) or part thereof
- **Time**: Valid up to 4 hours

**Phenomena Covered by SIGMET**:
- **Thunderstorms** (TS)
  - Embedded CB
  - Frequent/severe TS
  - Squall lines (lignes de grains)
- **Tropical cyclones** (cyclones tropicaux)
- **Severe turbulence** (turbulence forte) - MOD or SEV
- **Severe icing** (givrage fort) - MOD or SEV
- **Severe mountain wave** (ondes orographiques fortes)
- **Widespread dust** or sand storm (tempête de poussière/sable)
- **Volcanic ash** (cendres volcaniques)
- **Radioactive cloud** (nuage radioactif)

**Format**: Coded message (example from slides)

**Example SIGMET**:
```
271
WSGR31 LGAT 021430
LGGG SIGMET 9 VALID 021430/021630 LGAT-
LGGG ATHINAI FIR/UIR EMBD TS OBS E OF E02600 AND N OF N3600 AND S OF
N3800 AND W OF E02740 STNR NC=
```

**Decode**:
- **LGGG**: Athens FIR (Greece)
- **SIGMET 9**: Ninth SIGMET of the day
- **VALID 021430/021630**: Valid 2nd day 14:30-16:30 UTC (2 hours)
- **EMBD TS**: Embedded thunderstorms
- **OBS**: Observed (currently happening)
- **Geographic area**: East of E02600, North of N3600, South of N3800, West of E02740
- **STNR NC**: Stationary, No Change expected

**Interpretation**: Embedded thunderstorms observed in specified area of Athens FIR, stationary, no change expected.

### AIRMET - Airmen's Meteorological Information

**Purpose**: Warns of **moderate weather** affecting **small aircraft**

**Coverage**:
- **Altitude**: Below FL100 (low-level operations)
- **Area**: FIR or UIR (Upper Information Region)
- **Time**: Valid up to 4 hours

**Phenomena Covered by AIRMET**:
- **Moderate turbulence** (below FL100)
- **Moderate icing** (below FL100)
- **Moderate mountain wave** (below FL100)
- **Visibility** < 5 km (for large areas)
- **Extensive low cloud** (cloud base < 300m / ceiling < 1000 ft over large area)

**SIGMET vs AIRMET**:

| Aspect | SIGMET | AIRMET |
|--------|--------|--------|
| **Severity** | Severe/dangerous | Moderate |
| **Aircraft** | All aircraft | Light aircraft, GA |
| **Altitude** | All altitudes (SFC-FL450) | Low level (SFC-FL100) |
| **Priority** | High (urgent) | Moderate |

**Example SIGMET** (from slides):
```
329
WSRS31 RUMA 021449
UUWV SIGMET 6 VALID 021500/021800 UUWV-
UUWV MOSCOW FIR SEV ICE (FZRA) FCST NW OF LINE N5017 E04200 - N5000
E03755 AND SE OF
LINE N5330 E04228 - N5200 E03405 SFC/FL100 MOV NE 30KMH NC=
```

**Decode**: Severe icing (freezing rain) forecast northwest of line... surface to FL100, moving northeast at 30 km/h, no change in intensity expected.

### How to Use SIGMET/AIRMET

**Pre-flight**:
- Check for active SIGMETs in your route area
- **ANY SIGMET → Seriously reconsider flight or avoid area**
- AIRMET → Assess based on experience level

**In-flight**:
- Monitor ATC for updates
- Avoid areas mentioned in SIGMETs
- Report if you encounter unreported hazards

**Where to Find**:
- MétéoSuisse website
- Aviation weather briefing services
- ATC radio broadcasts (ATIS, VOLMET)
- FlugWetter.de

## Soundings and Emagrammes

**📖 Reference**: Page 125

### What is a Sounding?

**Sounding** (Sondage/Radiosondage) = Vertical profile of atmosphere

**Measured by**:
- **Weather balloon** (ballon-sonde) carrying radiosonde instrument
- Launched twice daily (00 and 12 UTC) from ground stations
- Ascends to 30+ km altitude (to stratosphere)
- Measures: Temperature, pressure, humidity, wind at all altitudes

### Switzerland's Main Station

**Payerne** (46.8°N, 6.9°E, 491 m elevation)
- Switzerland's only regular upper-air station
- Launches at **00 UTC** and **12 UTC** daily (midnight and noon UTC)
- Data available ~1-2 hours after launch
- Critical for forecasting

### Emagram (Émagramme)

**Emagram** = Graphical representation of atmospheric sounding

**Axes**:
- **X-axis**: Temperature (°C)
- **Y-axis**: Pressure (hPa) or Altitude (m)

**Lines Plotted**:
- **Temperature profile** (red line): Actual temperature at each altitude
- **Dewpoint profile** (blue line): Actual dewpoint at each altitude
- **Dry adiabats**: Lines showing cooling rate for unsaturated rising air (-1°C/100m)
- **Moist adiabats**: Lines showing cooling rate for saturated rising air (~-0.6°C/100m)

**What Emagram Shows**:
- **Stability**: Steep temperature profile = stable, shallow = unstable
- **Inversions**: Temperature increasing with altitude (layer of warm air over cold)
- **Cloud base**: Where temperature line meets dewpoint line
- **Humidity**: Gap between temperature and dewpoint (small gap = humid)
- **Freezing level**: Where temperature crosses 0°C
- **Thermal index** (TI): Potential thermal strength
- **Lifted condensation level** (LCL): Altitude where Cu base forms
- **Level of free convection** (LFC): Altitude where thermals become self-sustaining

**Uses for Gliding**:
- **Thermal forecasting**: Predict thermal strength and tops
- **Cloud base prediction**: Estimate cumulus base altitude
- **Wave potential**: Identify stable layers for wave flying
- **Inversion heights**: Know where thermals stop
- **Icing risk**: Check temperature profile for 0°C to -20°C zone in clouds

**Where to Find**:
- University of Wyoming: http://weather.uwyo.edu/upperair/sounding.html
- MeteoBlue: https://www.meteoble.com
- TopTherm software (Java application for glider pilots)

## Météogramme

**📖 Reference**: Page 126

### What is a Météogramme?

**Météogramme** = Time-series graph showing forecast evolution at a specific location

**Time Axis**: Usually 3-7 days ahead (hourly or 3-hourly intervals)

**Parameters Shown** (stacked graphs):
- **Cloud cover** (top panel): Cloud layers at different altitudes, shaded by type
- **Wind barbs**: Direction and speed at 10m (or at altitude)
- **Temperature** and **dewpoint**: Curves showing evolution
- **Pressure**: QNH trend (rising/falling pressure)
- **Precipitation**: Amount and type (rain/snow/mixed)
- **Weather symbols**: Sun, clouds, rain, snow, thunderstorms

**Example Reading**:
```
Date: Wed 02 Feb → Thu 03 Feb → Fri 04 Feb

[Cloud panel]: Shows overcast Wed morning → breaking Thu → clear Fri

[Wind]: Light west Wed → increasing southwest Thu → strong west Fri

[Temp/Td]: 0°C Wed → warming to 8°C Thu → cooling to 4°C Fri
           Small spread Wed (humid) → larger spread Fri (dry)

[Pressure]: 1000 hPa Wed → 1010 hPa Fri (rising = improving)

[Precip]: Rain Wed morning → no rain Thu-Fri
```

**Interpretation**: Frontal passage Wednesday (rain, low clouds), high pressure building Thursday-Friday (improving conditions).

**Uses for Gliding**:
- **Day-to-day planning**: When to fly (next 3-7 days)
- **Timing**: Best hours of the day for thermals
- **Weather window**: Between frontal systems
- **Temperature trends**: Warm = good thermals, cold = weak
- **Humidity**: Dewpoint spread indicates cu-nimb risk

**Where to Find**:
- MeteoBlue
- Windy.com
- MétéoFrance (Meteogramme)
- DWD (Germany)

## Pressure Gradient Maps

**📖 Reference**: Pages 127-128

### Purpose

Monitor **pressure difference** between two stations to predict **special wind situations** in Switzerland.

### Gradient Types

#### 1. West/Bise Gradient (Geneva - Güttingen)

**📖 Reference**: Page 127

**Stations**:
- **Geneva** (Genève): West end of Plateau
- **Güttingen**: East end of Plateau (Lake Constance area)

**Gradient**: Pressure difference between Geneva and Güttingen

**Indicates**:
- **Positive gradient** (Geneva higher pressure): **Bise** (northeast wind on Plateau)
- **Negative gradient** (Güttingen higher): **Southwest wind**
- **Zero gradient**: Weak pressure gradient

**Bise Conditions**:
- Pressure difference ≥ 4-5 hPa
- Cold, dry northeast wind on Swiss Plateau
- Often brings clear skies but also cold temps and strong winds
- Can last several days

**Chart Shows**: Time series (days) vs pressure gradient (hPa)

#### 2. Föhn Gradient (Zurich - Lugano)

**📖 Reference**: Page 128

**Stations**:
- **Zurich**: North of Alps
- **Lugano**: South of Alps (Ticino)

**Gradient**: Pressure difference between north and south of Alps

**Indicates**:
- **North föhn**: Lugano pressure > Zurich pressure (≥4 hPa) → North föhn (wind from north)
- **South föhn**: Zurich pressure > Lugano pressure (≥4 hPa) → **South föhn** (wind from south)
- **Zero gradient**: No föhn

**South Föhn Conditions** (most common):
- Pressure difference ≥ 4 hPa (Zurich > Lugano)
- Strong, warm, dry wind descending north side of Alps
- Clear skies north of Alps, cloudy/rainy south of Alps
- Wave conditions possible
- Can reach hurricane strength in valleys

**Chart Shows**: Time series vs pressure gradient, with zones marked:
- **Südföhn zone** (positive, Zurich higher)
- **Nordföhn zone** (negative, Lugano higher)

**Where to Find**: Meteocentrale.ch (Swiss specialized site)

## Specialized Soaring Products

### AlpTherm

**📖 Reference**: Page 129

**Purpose**: Thermal and soaring forecast map for **Alps region**

**Coverage**: Switzerland, southern Germany, Austria, northern Italy

**Information Shown**:
- **Thermal strength**: Color-coded areas (red/orange = strong, blue/green = weak)
- **Cloud base**: Estimated cumulus base altitude
- **Overdevelopment risk**: Areas where Cu may develop to Cb
- **Wind**: Upper-level wind affecting soaring

**Color Coding** (example):
- Red: Excellent thermals (>3 m/s)
- Orange: Good thermals (2-3 m/s)
- Yellow: Moderate thermals (1-2 m/s)
- Green: Weak thermals (<1 m/s)
- Blue: No thermals or sink

**Where to Find**:
- FlugWetter.de: https://www.flugwetter.de (AlpTherm section)
- Updated daily (morning)

### TopTherm (Logiciel Java)

**📖 Reference**: Page 130

**Purpose**: Detailed soaring forecast **software for PC/Mac**

**Features**:
- **Vertical profile**: Temperature, wind, humidity by altitude
- **Thermal forecast**: Strength and timing
- **Cloud forecast**: Type, base, tops
- **Météogramme**: Time evolution
- **Location-specific**: Choose exact coordinates
- **Up to 5 days**: Advance forecast

**Data Source**: Numerical weather models (GFS, ECMWF, etc.)

**Cost**: Payant (paid software) - subscription required

**Where to Get**: TopMeteo / TopTherm website

**Use**: Professional cross-country planning, competition flying

---

## Summary Table: Meteorological Products Overview

| Product | Type | Update | Validity | Use |
|---------|------|--------|----------|-----|
| **METAR** | Observation | 30 min | ~1 hour | Current conditions |
| **TAF** | Forecast | 3 hours | 9-30 hours | Local forecast |
| **GAFOR** | Forecast | 6 hours | 6-12 hours | VFR route planning |
| **Surface Chart** | Analysis | 6 hours | Current | Synoptic pattern |
| **Satellite** | Observation | 15 min | Current | Cloud location |
| **Radar** | Observation | 5 min | Current | Precipitation |
| **TEMSI** | Forecast | 6 hours | Up to 24h | Aviation hazards |
| **LLSWC** | Forecast | 6 hours | Up to 12h | Alpine aviation |
| **SIGMET** | Warning | As needed | Up to 4h | Severe hazards |
| **AIRMET** | Warning | As needed | Up to 4h | Moderate hazards |
| **PIREP** | Observation | As reported | Current | Pilot reports |
| **Sounding** | Observation | 12 hours | Current | Vertical profile |
| **Météogramme** | Forecast | 6-12 hours | 3-7 days | Time evolution |
| **Gradients** | Observation | Continuous | Current | Föhn/Bise |
| **AlpTherm** | Forecast | Daily | 1 day | Soaring forecast |
| **TopTherm** | Forecast | 6 hours | 5 days | Detailed soaring |

---

*Related topics*: [METAR](12_metar_speci_detailed.md), [TAF](13_taf_detailed.md), [Weather Charts](14_weather_charts.md), [GAFOR](15_gafor_detailed.md), [Thunderstorms](10_thunderstorms.md)
