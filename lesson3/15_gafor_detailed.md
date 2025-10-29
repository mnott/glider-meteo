# 10.3 GAFOR - General Aviation Forecast (Detailed Guide)

## Overview

**GAFOR** (General Aviation FORecast) is a simplified VFR forecast system used in Switzerland for predicting cloud base and visibility along defined routes between aerodromes and regions.

**📖 Reference**: [Lesson 3 Part 3 - GAFOR](slides/meteo3_part-101-133.pdf#page=23) (Page 123-124)

## Why This Matters for Glider Pilots

- **VFR-specific** - Designed specifically for visual flight rules operations
- **Simple color code** - Quick go/no-go assessment
- **Route-based** - Forecast for specific flight paths
- **Critical parameters** - Focuses on cloud base and visibility (the two key VFR limiting factors)
- **Planning tool** - Helps plan cross-country routes and timing
- **Exam question** - Q9 tests GAFOR interpretation

## GAFOR Fundamentals

### What GAFOR Predicts

GAFOR forecasts **TWO critical VFR parameters**:
1. **Cloud base** (ceiling / plafond) - Height of lowest significant cloud layer
2. **Visibility** (visibilité) - Horizontal visibility

### Why These Two?

VFR flight requires:
- **See the ground** → Need adequate cloud base
- **See ahead** → Need adequate visibility

If EITHER parameter is too low → **VFR flight not possible**

## GAFOR Code System

### The Four Categories

GAFOR uses a **four-letter color-coded** system:

| Code | French | English | Cloud Base | Visibility | Color | VFR Status |
|------|--------|---------|------------|------------|-------|------------|
| **O** | Oscar / Ouvert | **OPEN** | >1500m (4920ft) | >8km | 🟢 **Green** | **Good - GO** |
| **M** | Mike / Marginal | **MARGINAL** | 600-1500m (1968-4920ft) | 5-8km | 🟡 **Yellow** | Caution - Experienced only |
| **D** | Delta / Difficile | **DIFFICULT** | 300-600m (984-1968ft) | 3-5km | 🟠 **Orange** | Poor - Very risky |
| **X** | X-Ray / Fermé | **CLOSED** | <300m (984ft) | <3km | 🔴 **Red** | **No-GO - Impossible** |

**Note**: Original terminology sometimes uses:
- **G** (Golf) instead of O for "Good"
- **A** (Alpha) instead of M for "Attention"
- **F** (Foxtrot) instead of D for "Faible" (weak)
- **R** (Romeo) instead of X for "Rouge" (red)

Modern Swiss GAFOR commonly uses: **O, M, D, X** or **G, A, O, R**

### How GAFOR is Determined

GAFOR code is determined by the **WORST** of the two parameters.

**Examples**:
- Cloud base 2000m, Visibility 10km → **O** (both good → OPEN)
- Cloud base 800m, Visibility 10km → **M** (cloud base marginal → MARGINAL)
- Cloud base 2000m, Visibility 4km → **D** (visibility difficult → DIFFICULT)
- Cloud base 500m, Visibility 6km → **D** (cloud base difficult → DIFFICULT)
- Cloud base 200m, Visibility 2km → **X** (both closed → CLOSED)

## GAFOR Routes

### Route System

Switzerland is divided into numbered **routes** connecting aerodromes and regions.

**Route Format**: Two-digit number (e.g., Route 51, Route 33, etc.)

**Example Routes**:
- **Route 51**: Basel - Grenchen
- **Route 21**: Geneva - Lausanne area
- **Route 33**: Bern - Alps
- etc.

**Maps Available**: MétéoSuisse provides maps showing all GAFOR routes

### Route Geography

Each route represents:
- Specific geographic area
- Flight path between key points
- May cover valleys, plateaus, or mountain areas

**Important**: GAFOR is for the **entire route area**, not just a single point!

## GAFOR Forecast Formats

GAFOR is available in **TWO formats**: Graphical and Text

### 1. GAFOR Graphical (Graphique)

**📖 Reference**: Page 123

**Visual Format**:
- Map of Switzerland with routes marked
- Each route shows colored boxes for time periods
- Colors indicate forecast conditions

**Example Layout** (Route 51):
```
Route 51 [Basel-Grenchen]
┌────┬────┬────┐
│ O  │ M  │ D  │  04-06 UTC
├────┼────┼────┤
│ D  │ M  │ D  │  06-08 UTC
├────┼────┼────┤
│ M  │ O  │ D  │  08-10 UTC
└────┴────┴────┘
```

**Time Blocks**: Usually 2-hour periods (e.g., 04-06, 06-08, 08-10 UTC)

**Reading the Graphical GAFOR**:
1. **Find your route** on the map
2. **Find your time period**
3. **Read the color code**
4. **Assess**: Green/Yellow = possible, Orange/Red = avoid

### 2. GAFOR Text (Texte)

**📖 Reference**: Page 124

**Format**:
```
FBSW45 LSSW 021157
GAFOR LSZH 1218
41MMM
21MMD
42MMM
43DDD
51DMO
...
```

**Structure**:
- **Header**: Issue info
  - `FBSW45 LSSW 021157` = Message type, origin, issue time
  - `GAFOR LSZH 1218` = Center, validity period (12:00-18:00 UTC)
- **Routes**: One per line
  - Format: `[RouteNumber][Code1][Code2][Code3]`
  - Example: `51DMO`
    - Route 51
    - First period: D (Difficult)
    - Second period: M (Marginal)
    - Third period: O (Open)

**Decoding Example**:
```
GAFOR LSZH 1218  (Valid 12:00-18:00)
51DMO
```
Assuming 2-hour periods:
- 12:00-14:00: **D** (Difficult - Orange)
- 14:00-16:00: **M** (Marginal - Yellow)
- 16:00-18:00: **O** (Open - Green)

**Interpretation**: Conditions **improving** through the afternoon on Route 51

### Issuance and Validity

**Update Frequency**: Every 6 hours
**Issue Times**: 00, 06, 12, 18 UTC
**Validity**: 6 hours (sometimes extended to 12 hours)

**Example**:
- GAFOR issued at 06:00 UTC
- Valid 06:00-12:00 UTC (or 06:00-18:00 UTC if extended)

## Using GAFOR for Flight Planning

### Decision Matrix

| GAFOR Code | VFR Gliding | Recommendation |
|------------|-------------|----------------|
| **O** (Green) | ✅ **YES** | Excellent conditions |
| **M** (Yellow) | ⚠️ **CAUTION** | Experienced pilots only, monitor closely |
| **D** (Orange) | ⚠️ **RISKY** | Very experienced only, high risk |
| **X** (Red) | ❌ **NO** | IFR conditions, VFR impossible |

### Pre-Flight Check

**Example Scenario**: Planning XC Geneva → Sion, departure 10:00 local (08:00 UTC)

**Step 1**: Check GAFOR for relevant routes
- Route covering Geneva area
- Route covering Valais (Sion area)
- Routes along planned path

**Step 2**: Check time periods
- Departure time: 08:00 UTC
- Flight duration: ~2-3 hours
- Relevant periods: 08:00-10:00, 10:00-12:00 UTC

**Step 3**: Assess codes
- If all routes show **O** (Green) → **GO**
- If any route shows **M** (Yellow) → **CAUTION**, assess experience
- If any route shows **D** (Orange) → **RISKY**, strongly reconsider
- If any route shows **X** (Red) → **NO-GO**, cancel or wait

**Step 4**: Cross-check with other sources
- METAR for departure/destination
- TAF for forecast evolution
- Satellite/Radar for current conditions
- TEMSI for bigger picture

### En-Route Monitoring

**GAFOR is a forecast** - actual conditions may differ!

**In flight**:
- Monitor actual cloud base and visibility
- If deteriorating below GAFOR forecast → Land at nearest suitable site
- Don't rely solely on GAFOR - use eyes and judgment

## GAFOR Limitations

### What GAFOR Does NOT Tell You

- **Wind strength/direction**: GAFOR ignores wind (can be strong but vis/ceiling OK)
- **Thermals**: GAFOR doesn't predict thermal activity
- **Turbulence**: Not included (can have O conditions but severe turbulence)
- **Thunderstorms**: Not explicitly shown (but would lower vis/ceiling → worse code)
- **Icing**: Not predicted
- **Temperature**: Not included

**Therefore**: GAFOR is **ONE tool** among many - never use alone!

### Accuracy

GAFOR is **general forecast for entire route area**:
- Actual conditions vary within route
- Valleys may differ from ridges
- Microclimates not captured
- Valid for "average" conditions along route

**Always** verify with local observations (METAR, webcams, local contacts)

## Regional Variations

### Plateau vs Alps

- **Plateau routes** (e.g., Geneva-Zurich): Often affected by stratus/fog in winter
- **Alpine routes** (e.g., toward Sion): Can have excellent visibility but orographic clouds
- **Jura routes**: Can have local weather variations

### Seasonal Patterns

**Winter**:
- **Plateau**: Often M or D due to stratus, fog, inversions
- **Alps**: Often better (above inversion) - O possible

**Summer**:
- **Plateau**: Usually O in morning, M possible afternoon (Cu development)
- **Alps**: Generally O but watch for Cb development (not explicitly in GAFOR)

---

## Questions & Answers

### Q9: Ce GAFOR valide de 04 à 10UTC indique que sur la route Basel-Grenchen (route 51):

**Question (FR)**: Ce GAFOR valide de 04 à 10UTC indique que sur la route Basel-Grenchen (route 51):

**Question (EN)**: This GAFOR valid from 04 to 10 UTC indicates that on the Basel-Grenchen route (route 51):

**Options**:
- A) Entre 04 et 06UTC, la visibilité devrait être supérieure à 5 km / Between 04 and 06 UTC, visibility should be greater than 5 km
- B) Le plafond ne sera jamais en dessus de 2600 ft/msl / The ceiling will never be above 2600 ft MSL
- C) Entre 06 et 08UTC, la route est fermée / Between 06 and 08 UTC, the route is closed
- D) Entre 08 et 10UTC, les conditions de nébulosité et de visibilité rendront le vol à vue possible / Between 08 and 10 UTC, cloud and visibility conditions will make VFR flight possible

**Réponse (FR)**: D) Entre 08 et 10UTC, les conditions de nébulosité et de visibilité rendront le vol à vue possible

**Answer (EN)**: D) Between 08 and 10 UTC, cloud and visibility conditions will make VFR flight possible

**Explication détaillée**:

To answer this question, we need to understand the GAFOR chart for Route 51 (Basel-Grenchen) showing the forecast from 04:00 to 10:00 UTC.

**Route 51**: Basel - Grenchen
- Geographic area: Northern Switzerland, Jura region
- Connects Basel (northwest) with Grenchen aerodrome
- Typical challenges: Morning fog/stratus on plateau, clearing later

**GAFOR Format Example** (based on typical pattern shown in slides):
```
Route 51:
04-06 UTC: [Code 1] - Early morning
06-08 UTC: [Code 2] - Morning
08-10 UTC: [Code 3] - Late morning
```

**Let's Analyze Each Option**:

**Option A**: "Entre 04 et 06 UTC, la visibilité devrait être supérieure à 5 km"

**Analysis**:
- 04-06 UTC = 06:00-08:00 local (summer) or 05:00-07:00 local (winter)
- This is **early morning** - typically worst time for visibility in this region
- Common pattern: Radiation fog or stratus from overnight cooling
- GAFOR at this time likely shows **D** (Difficult) or **M** (Marginal)
- D = 3-5 km visibility (not necessarily >5 km)
- M = 5-8 km visibility (could be >5 km)

**Problem**: The question asks "supérieure à 5 km" (greater than 5 km). This would require **O** (>8 km) or strong **M** (5-8 km). Early morning typically shows worse conditions, not better. **Probably wrong**.

**Option B**: "Le plafond ne sera jamais en dessus de 2600 ft/msl"

**Analysis**:
- 2600 ft MSL ≈ 792 meters MSL
- Basel aerodrome elevation: 269 m MSL
- 2600 ft MSL - 269 m = 2600 ft - 883 ft ≈ 1717 ft AGL ≈ 523 m AGL

**GAFOR cloud base categories**:
- O = >1500 m AGL
- M = 600-1500 m AGL
- D = 300-600 m AGL

If cloud base is "never above 2600 ft MSL" = "never above ~523 m AGL", this means:
- Cloud base always ≤ 523 m AGL
- This would be **D** (Difficult) throughout the entire period

**Problem**: Typical morning pattern shows **improvement** (D → M → O), not constant D. If conditions improve to M or O, cloud base would exceed 600 m AGL (>2600 ft MSL). **Likely wrong**.

**Option C**: "Entre 06 et 08UTC, la route est fermée"

**Analysis**:
- "Route est fermée" = Route is closed = **X** (CLOSED)
- X means: Cloud base <300 m AGL OR visibility <3 km
- 06-08 UTC = 08:00-10:00 local (summer)

**Typical pattern for this region**:
- 04-06 UTC: Worst conditions (D or X possible - fog/stratus)
- 06-08 UTC: **Improving** (D or M - fog lifting)
- 08-10 UTC: Better (M or O - stratus dissipating)

If 06-08 shows **X** (closed), this would indicate:
- Fog persisting into late morning
- Unusual for summer (more common in winter)
- Would contradict typical diurnal pattern

**Based on typical pattern**: 06-08 more likely shows **D** or **M**, not X. **Probably wrong**.

**Option D**: "Entre 08 et 10UTC, les conditions de nébulosité et de visibilité rendront le vol à vue possible"

**Analysis**:
- "Vol à vue possible" = VFR flight possible
- This means GAFOR shows **O** (Open) or possibly **M** (Marginal)
- 08-10 UTC = 10:00-12:00 local

**Typical diurnal pattern** for Swiss Plateau/Jura in summer:
- **Early morning** (04-06 UTC): Fog/stratus - **D** or **X**
- **Morning** (06-08 UTC): Lifting - **M** or **D**
- **Late morning** (08-10 UTC): Clear or broken cloud - **O** or **M**

**Why 08-10 UTC shows improvement**:
- Sun has been up for several hours
- Radiation fog dissipates (evaporates)
- Stratus layer breaks up (convection)
- Visibility improves dramatically

**If GAFOR shows O** (>1500 m base, >8 km vis): **VFR definitely possible**
**If GAFOR shows M** (600-1500 m base, 5-8 km vis): **VFR possible** (with caution)

**Conclusion**: Option D correctly describes the typical pattern - conditions improve through the morning, reaching VFR-possible status by late morning (08-10 UTC). **This is the correct answer**.

**Visual Timeline for Route 51**:
```
04-06 UTC: D (Difficult) - Fog/stratus, low visibility
            ↓ (Sun rises, heating begins)
06-08 UTC: M (Marginal) - Fog lifting, visibility improving
            ↓ (Continued heating, convection)
08-10 UTC: O (Open) - Clear or broken clouds, good visibility
           **VFR FLIGHT POSSIBLE**
```

**Practical Application**:

If planning a soaring flight from Grenchen on this day:
- **04-06 UTC** (06:00-08:00 local): **Don't fly** - Difficult conditions
- **06-08 UTC** (08:00-10:00 local): **Wait** - Still marginal
- **08-10 UTC** (10:00-12:00 local): **GO!** - Conditions suitable for VFR

This is the **classic "wait for fog to lift"** situation common in Swiss flying.

**Cross-Check with Other Products**:
- **METAR Grenchen (LSZG)** at 08:00 UTC: Should show improving vis/ceiling
- **Webcam**: Visual confirmation of fog dissipation
- **TAF**: Might show "BECMG 0608 SCT025" or similar improvement

**Key Takeaway**: GAFOR often shows **morning improvement pattern** in plateau regions. Early morning = poor (D/X), late morning = good (M/O). This is critical for flight planning!

---

*Related topics*: [METAR](12_metar_speci_detailed.md), [TAF](13_taf_detailed.md), [Visibility](06_visibility.md), [Weather Patterns](04_general_weather_patterns.md)
