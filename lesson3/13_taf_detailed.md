# 10.3 TAF - Terminal Aerodrome Forecast (Detailed Guide)

## Overview

**TAF** (Terminal Aerodrome Forecast) is a coded weather forecast for an aerodrome and its vicinity. TAFs provide forecast conditions for the next 9 to 30 hours, depending on the airport.

**📖 Reference**: [Lesson 3 Part 3 - TAF](slides/meteo3_part-101-133.pdf#page=18) (Page 118-119)

## Why This Matters for Glider Pilots

- **Planning tool** - TAF tells you what weather to expect in coming hours
- **Go/No-Go decision** - Helps decide if conditions will be suitable
- **Timing** - Shows when conditions will deteriorate or improve
- **Exam critical** - Must be able to decode TAF structure
- **Cross-country planning** - Forecast conditions along route
- **Safety** - Warns of approaching fronts, thunderstorms, low cloud

**Key difference from METAR**:
- METAR = Current observation (what IS happening)
- TAF = Forecast (what WILL happen)

## TAF Structure and Format

### Basic Format

```
TAF ICAO DDHHMM DDhh/DDhh [Wind] [Visibility] [Weather] [Clouds] [TempForecast] [ChangeGroups]
```

### Example TAF (from slides)

```
TAF LSGG 160525Z 1606/1712 24010KT 9999 -RA FEW010 OVC030
     TX08/1621Z TN03/1606Z TN07/1704Z
     TEMPO 1607/1614 RA
     PROB40 TEMPO 1621/1701 RA=
```

## Complete TAF Elements

### 1. Message Type
**TAF** (sometimes **TAF AMD** for amended forecast)

### 2. Station Identifier
**ICAO code** (same as METAR)
- LSGG = Geneva
- LSZH = Zurich
- LSGS = Sion
- LSZB = Bern
- etc.

### 3. Issue Date/Time
**Format**: `DDHHMM**Z**`
- DD = Day of month
- HH = Hour (UTC)
- MM = Minute (UTC)
- Z = Zulu (UTC)

**Example**: `160525Z` = 16th day, 05:25 UTC

### 4. Validity Period
**Format**: `DDhh/DDhh`
- First `DDhh` = Start day and hour (UTC)
- Second `DDhh` = End day and hour (UTC)

**Examples**:
- `1606/1712` = Valid from 16th 06:00 UTC to 17th 12:00 UTC (30 hours)
- `1106/1115` = Valid from 11th 06:00 UTC to 11th 15:00 UTC (9 hours)

**Validity Periods in Switzerland**:
- **LSZH/LSGG** (major airports): **30 hours**
- **Regional airports**: **9 hours**
- **Military aerodromes**: **9 hours**

### 5. Base Forecast

Following the validity period, the **base forecast** contains the same elements as METAR:

#### Wind
**Format**: `DDDSSKT` or `DDDSSGSSGKT`
- Same as METAR
- Direction in degrees true north
- Speed in knots
- Gusts if applicable

**Example**: `24010KT` = Wind from 240° at 10 kt

#### Visibility
- In meters
- `9999` = 10 km or more
- `CAVOK` if all conditions met

**Example**: `9999` = Visibility 10 km or more

#### Weather Phenomena
- Same codes as METAR
- `-RA` = Light rain
- `TSRA` = Thunderstorm with rain
- `SHRA` = Rain showers
- etc.

#### Clouds
**Format**: `AAAHHHH`
- Same as METAR
- Amount (FEW/SCT/BKN/OVC)
- Height in hundreds of feet AGL

**Example**: `FEW010 OVC030` = Few at 1000 ft, Overcast at 3000 ft

### 6. Temperature Forecast (Optional)

**Format**: `TX##/DDhhZ TN##/DDhhZ`

- **TX**: Maximum temperature
- **TN**: Minimum temperature
- **##**: Temperature in °C (M prefix for minus)
- **/DDhhZ**: Day and hour UTC when expected

**Example**: `TX08/1621Z TN03/1606Z TN07/1704Z`
- Maximum +8°C at 16th 21:00 UTC
- Minimum +3°C at 16th 06:00 UTC
- Minimum +7°C at 17th 04:00 UTC

**Why multiple TN**: Can have multiple minima in a 30-hour forecast (nighttime cooling)

### 7. Change Groups

TAFs use change indicators to show when conditions will differ from the base forecast.

#### BECMG (Becoming)

**Format**: `BECMG DDhh/DDhh [elements]`

**Meaning**: **Gradual change** to new conditions
- Change occurs **during the time period** specified
- New conditions **persist** after the period ends
- Used for **permanent changes** (frontal passage, trend changes)

**Example**:
```
TAF LSGS 110525Z 1106/1115 VRB02KT CAVOK
     BECMG 1108/1110 BKN100
     BECMG 1113/1115 RA
```

**Interpretation**:
- **Base** (06:00-08:00): CAVOK (clear skies)
- **BECMG 08:00-10:00**: Clouds gradually form, reaching BKN at 10,000 ft by 10:00
- **10:00-13:00**: BKN100 persists (from first BECMG)
- **BECMG 13:00-15:00**: Rain develops, reached by 15:00
- **After 15:00** (if TAF extended): Rain continues

**BECMG indicates**: Front approaching, air mass change, synoptic pattern shift

#### TEMPO (Temporary)

**Format**: `TEMPO DDhh/DDhh [elements]`

**Meaning**: **Temporary fluctuations**
- Conditions **occur temporarily** during period
- Each occurrence lasts **< 1 hour**
- Conditions then **return to base forecast**
- Total duration of TEMPO conditions **< 50% of period**

**Example**:
```
TAF ... 1106/1118 SCT040
    TEMPO 1112/1116 BKN020
```

**Interpretation**:
- **Base**: Scattered clouds at 4000 ft
- **Between 12:00-16:00**: Temporarily broken at 2000 ft (then returns to SCT040)
- Broken clouds occur for less than half the time (e.g., occasional periods of 30-45 min)

**TEMPO indicates**: Showers, temporary weather phenomena, intermittent conditions

#### PROB (Probability)

**Format**: `PROB30` or `PROB40` followed by `TEMPO DDhh/DDhh [elements]`

**Meaning**: **Probability** that temporary conditions will occur
- **PROB30**: 30% probability
- **PROB40**: 40% probability
- Always used with TEMPO

**Example**:
```
TAF ... 1606/1712 24010KT 9999
    PROB40 TEMPO 1621/1701 RA
```

**Interpretation**:
- **Base**: 10 kt wind, 10 km visibility
- **Between 21:00(16th)-01:00(17th)**: 40% chance of temporary rain

**PROB indicates**: Uncertain weather (possible showers, possible thunderstorms)

#### FM (From)

**Format**: `FM DDhhmm [complete forecast]`

**Meaning**: **Rapid change** at specific time
- Change occurs **at the specified time**
- Requires **complete new forecast** (wind, vis, weather, clouds)
- Used for **sudden changes** (front passage, squall line)

**Example**:
```
TAF ... 1606/1618 27015KT 9999 SCT025
    FM161200 09025G35KT 5000 TSRA BKN008 OVC015CB
```

**Interpretation**:
- **Before 12:00**: West wind 15 kt, good visibility
- **From 12:00**: East wind 25 kt gusting 35 kt, visibility 5 km, thunderstorms, low clouds with CB
- (This represents a cold front passage)

## TAF Issuance Schedule

### Switzerland

**Major Airports (LSZH, LSGG, Military)**:
- **Every 3 hours**
- **Times**: 00, 03, 06, 09, 12, 15, 18, 21 UTC
- **Validity**: 30 hours

**Regional Airports**:
- **Every 3 hours during daylight**
- **Times**: 06, 09, 12, 15, 18 UTC
- **Validity**: 9 hours

**Military Aerodromes**:
- **Times**: 10, 17 UTC
- **Validity**: 9 hours

## Interpreting TAF for Flight Planning

### Step 1: Check Validity Period
- Does TAF cover your planned flight time?
- Is it recent? (TAFs can be up to 3 hours old)

### Step 2: Analyze Base Forecast
- What are initial conditions?
- Suitable for VFR?

### Step 3: Check Change Groups
- When do conditions deteriorate/improve?
- Any TEMPO weather during your flight?
- Any BECMG indicating front arrival?

### Step 4: Assess Risk
- PROB groups = uncertainty, plan conservatively
- TEMPO TS = possible thunderstorms, avoid
- BECMG to IFR conditions = plan to land before

### Example Decision-Making

**Scenario**: Planning soaring flight 10:00-16:00 local (08:00-14:00 UTC)

**TAF**:
```
TAF LSGS 110525Z 1106/1115 VRB02KT CAVOK
     BECMG 1108/1110 BKN100
     BECMG 1113/1115 RA
```

**Analysis**:
- **06:00-08:00 UTC**: CAVOK (excellent - but before our flight)
- **08:00-10:00 UTC**: Clouds building to BKN at 10,000 ft (still OK for soaring if thermals)
- **10:00-13:00 UTC**: BKN at 10,000 ft persists (acceptable)
- **13:00-15:00 UTC**: Rain develops (not suitable)

**Decision**:
- **GO** for morning flight
- **Plan to land by 13:00 UTC** (15:00 local) before rain
- **Monitor conditions** - if rain arrives early, land immediately

## Common TAF Patterns

### Improving Conditions
```
TAF ... 1606/1618 OVC015 5000 -RA
    BECMG 1610/1612 BKN025
    BECMG 1614/1616 SCT035 9999 NSW
```
(Overcast and rain → Broken clouds → Scattered, no significant weather)

### Deteriorating Conditions
```
TAF ... 1106/1118 SCT030 9999
    BECMG 1112/1114 BKN020
    BECMG 1115/1117 OVC010 3000 -RA
```
(Scattered → Broken → Overcast with rain)

### Diurnal (Daily) Pattern
```
TAF ... 1118/1218
    0600-1000: CAVOK (morning - clear after radiation fog clears)
    1000-1800: SCT035 (day - thermals create Cu)
    1800-0600: NSC (evening/night - Cu dissipate)
```

### Frontal Passage
```
TAF ... 1606/1618 24015KT SCT025
    FM161400 27025G40KT 8000 SHRA BKN015CB
    TEMPO 1414/1418 4000 +TSRA
```
(Pre-frontal → Cold front passage with strong winds, showers, CB → Possible heavy thunderstorms)

## TAF vs METAR - Key Differences

| Aspect | METAR | TAF |
|--------|-------|-----|
| **Type** | Observation | Forecast |
| **Time** | Current (past 10-30 min) | Future (9-30 hours) |
| **Frequency** | Every 30 min | Every 3 hours |
| **Accuracy** | 100% (observed) | Decreases with time |
| **Change groups** | None (use TREND) | BECMG, TEMPO, PROB, FM |
| **Temperature** | Current T/Td | Optional TX/TN forecast |
| **Use** | Current go/no-go | Planning, timing |

## Wind Direction Reference

**CRITICAL**: Like METAR, wind direction in TAF is referenced to **GEOGRAPHIC (TRUE) NORTH**, NOT magnetic north.

## Training and Practice

### Decode This TAF

**Practice Example**:
```
TAF LSZH 151200Z 1512/1618 27012KT 9999 SCT040
     TEMPO 1512/1518 BKN025
     BECMG 1520/1522 31018G30KT
     PROB40 TEMPO 1600/1606 TSRA BKN015CB
```

**Answer**:
- Zurich, issued 15th 12:00 UTC
- Valid 15th 12:00 - 16th 18:00 UTC (30 hours)
- **Base**: Wind 270° at 12 kt, vis 10+ km, scattered at 4000 ft
- **12:00-18:00 UTC**: Temporarily broken at 2500 ft
- **20:00-22:00 UTC**: Becoming wind 310° at 18 kt gusting 30 kt (front passage)
- **00:00-06:00 UTC (16th)**: 40% chance temporary thunderstorms with rain, broken CB at 1500 ft

### Where to Find TAFs

- **MétéoSuisse**: https://www.meteosuisse.ch
- **AllMetSat**: https://fr.allmetsat.com/metar-taf/
- **Aviation Weather**: Various apps (MeteoBlue, Windy, etc.)
- **FlugWetter.de**: German aviation weather portal

---

## Questions & Answers

### Q8: D'après ce TAF émis pour l'aérodrome de Sion: TAF LSGS 110525Z 1106/1115 VRB02KT CAVOK BECMG 1108/1110 BKN100 BECMG 1113/1115 RA

**Question (FR)**: D'après ce TAF émis pour l'aérodrome de Sion:

TAF LSGS 110525Z 1106/1115 VRB02KT CAVOK BECMG 1108/1110 BKN100 BECMG 1113/1115 RA

**Question (EN)**: According to this TAF issued for Sion aerodrome:

TAF LSGS 110525Z 1106/1115 VRB02KT CAVOK BECMG 1108/1110 BKN100 BECMG 1113/1115 RA

**Options**:
- A) Il semble que les conditions s'améliorent pour voler / It seems conditions are improving for flying
- B) Il devrait y avoir de la pluie à partir de l'après-midi / There should be rain starting in the afternoon
- C) Au départ, le ciel est couvert / Initially, the sky is overcast
- D) Le vent devrait forcir à plus de 10 kt sur la période de prévision / Wind should increase to more than 10 kt during the forecast period

**Réponse (FR)**: B) Il devrait y avoir de la pluie à partir de l'après-midi

**Answer (EN)**: B) There should be rain starting in the afternoon

**Explication détaillée**:

Let's decode this TAF completely:

**Header**:
- **TAF LSGS**: Forecast for Sion aerodrome
- **110525Z**: Issued on 11th day at 05:25 UTC
- **1106/1115**: Valid from 11th 06:00 UTC to 11th 15:00 UTC (9 hours)

**Base Forecast** (06:00-08:00 UTC):
- **VRB02KT**: Variable wind at 2 knots (essentially calm)
- **CAVOK**: Ceiling And Visibility OK
  - Visibility ≥ 10 km
  - No clouds below 5000 ft
  - No CB
  - No significant weather
  - **Perfect VFR conditions!**

**First Change** (BECMG 1108/1110):
- **BECMG**: Becoming (gradual change)
- **1108/1110**: Between 08:00 and 10:00 UTC
- **BKN100**: Broken clouds at 10,000 ft
- **Interpretation**: Clouds gradually develop during late morning, reaching broken layer at 10,000 ft by 10:00 UTC. Still VFR but no longer CAVOK.

**Second Change** (BECMG 1113/1115):
- **BECMG**: Becoming (gradual change)
- **1113/1115**: Between 13:00 and 15:00 UTC
- **RA**: Rain (moderate rain)
- **Interpretation**: Rain develops during early afternoon, established by 15:00 UTC

**Timeline**:
- **06:00-08:00 UTC** (08:00-10:00 local): CAVOK - Excellent
- **08:00-10:00 UTC** (10:00-12:00 local): Clouds building
- **10:00-13:00 UTC** (12:00-15:00 local): BKN at 10,000 ft - Acceptable but deteriorating
- **13:00-15:00 UTC** (15:00-17:00 local): Rain developing - **Afternoon**
- **After 15:00 UTC** (17:00 local): Rain established

**Why B is correct**: The TAF clearly shows rain (RA) developing between 13:00-15:00 UTC. In Switzerland (UTC+1 winter, UTC+2 summer), 13:00-15:00 UTC = 15:00-17:00 local time in summer, which is definitely the afternoon. The French "à partir de l'après-midi" = "starting in the afternoon" perfectly describes this.

**Why A is wrong**: Conditions **deteriorate**, not improve! The forecast goes from CAVOK (perfect) → clouds → rain. This is worsening conditions.

**Why C is wrong**: Initially (at 06:00 UTC), the sky is **CAVOK**, which means **NO clouds below 5000 ft**. The sky is NOT overcast initially. Overcast would be "OVC" not "CAVOK".

**Why D is wrong**: The wind remains **VRB02KT** throughout the entire forecast. There is NO mention of wind increasing. If wind were to increase, it would be shown in a change group (e.g., "BECMG 1110/1112 27015KT"). The 2 kt wind stays constant, never reaching 10 kt.

**Flight Planning Implication**:
- **Morning flight (08:00-12:00 local)**: Good conditions, CAVOK then some high clouds
- **Afternoon flight (after 13:00 local)**: Not recommended - rain developing
- **Decision**: Fly morning only, plan to land before 13:00 UTC (15:00 local)

**Meteorological Context**: This TAF pattern is typical of:
- Warm front approaching from west
- Morning starts clear (behind previous system)
- High clouds arrive mid-morning (Ci/Cs from approaching warm front)
- Rain arrives afternoon (Ns from warm front)
- Classic pre-frontal deterioration

---

*Related topics*: [METAR/SPECI](12_metar_speci_detailed.md), [Weather Charts](14_weather_charts.md), [Fronts](02_fronts.md)
