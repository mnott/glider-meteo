# ISA - ICAO Standard Atmosphere

**📖 Reference**: [Lesson 1 Slides - ISA](slides/meteo1_part-01-50.pdf#page=11)

## What is ISA?

**ISA** = **I**CAO **S**tandard **A**tmosphere ([International Standard Atmosphere](https://en.wikipedia.org/wiki/International_Standard_Atmosphere))
(Atmosphère standard OACI)

A standardized reference atmosphere defined by the [International Civil Aviation Organization (ICAO)](https://en.wikipedia.org/wiki/International_Civil_Aviation_Organization) and used worldwide in aviation for:
- Aircraft performance calculations
- Altimeter calibration
- Comparing actual conditions to "normal"
- Flight planning
- Consistent communication between pilots worldwide

## Why This Matters for Glider Pilots

ISA is your reference point for everything:
- **Performance calculations** - all aircraft specs assume ISA conditions
- **Altimeter settings** - understanding 1013.25 hPa standard setting
- **Weather deviation** - "ISA +10" tells you conditions are warmer than standard
- **Exam questions** - many theory questions use ISA as reference
- **Common language** - pilots worldwide use ISA to communicate atmospheric conditions
- When someone says "cold day," they mean "colder than ISA for this altitude"

## ISA Sea Level Conditions

At **mean sea level (MSL)**, ISA defines:

| Parameter | Value |
|-----------|-------|
| **Pressure (P)** | 1013.25 hPa |
| **Temperature (T)** | 15°C (or 288.15 K) |
| **Humidity** | 0% (dry air) |
| **Density (ρ)** | 1.225 kg/m³ |

**What this means**: These are the "standard" conditions that aircraft performance is based on. Real conditions are almost never exactly ISA! But ISA gives us a common reference point.

**Memorize these values!** They appear constantly in exams and calculations:
- **1013.25 hPa** (or 1013 hPa, or QNE) - the standard pressure
- **15°C** (or 288 K) - the standard temperature
- Often rounded to **1013 hPa** and **15°C** for simplicity

## Temperature Variation with Altitude

In the **troposphere** (0 to ~11 km):

**Temperature decreases at -0.65°C per 100 meters**
or
**-1.98°C per 1000 feet** (~-2°C/1000 ft)

This is called the [environmental lapse rate](https://en.wikipedia.org/wiki/Lapse_rate) in ISA conditions.

### Temperature at Altitude Formula:
**T = 15 - 0.65 × (altitude in hundreds of meters)**

or in feet:
**T = 15 - 2 × (altitude in thousands of feet)**

### Examples:
- **At 1000m**: T = 15 - (0.65 × 10) = 15 - 6.5 = **8.5°C**
- **At 2000m**: T = 15 - (0.65 × 20) = 15 - 13 = **2°C**
- **At 3000m**: T = 15 - (0.65 × 30) = **-4.5°C** (good soaring altitude!)
- **At 5000 ft**: T = 15 - (2 × 5) = **5°C**

**What this means**: For every 1000 meters you climb, temperature drops about 6.5°C. This is important for understanding why it gets cold at altitude and predicting cloud formation levels.

### Tropopause (11 km):
- Temperature: **-56.5°C** (or 216.5 K)
- Pressure: ~226 hPa
- Above this, temperature remains constant in lower stratosphere (isothermal layer)

**What this means**: The tropopause is where temperature stops decreasing. This temperature inversion creates stability - the "lid" that stops clouds and thermals from developing higher.

## Pressure Variation with Altitude

**Pressure halves approximately every 5500 meters**

### Typical ISA Pressure Levels:

| Altitude | Pressure |
|----------|----------|
| Sea level | 1013 hPa |
| ~1500 m | 850 hPa |
| ~3000 m | 700 hPa |
| ~5500 m | 500 hPa |

### Near-Surface Rule:
**Pressure decreases ~1 hPa per 8.5 meters** (or 28 feet)

## Deviations from ISA

Actual atmosphere rarely matches ISA - and that's important to recognize!

### ISA + or ISA -
- **ISA +10**: Actual temperature 10°C **warmer** than ISA
  - Example: At 2000m, ISA = 2°C, but actual = 12°C
  - **Hot day** - summer conditions

- **ISA -5**: Actual temperature 5°C **cooler** than ISA
  - Example: At 2000m, ISA = 2°C, but actual = -3°C
  - **Cold day** - winter conditions

**What this means**: This notation gives you instant understanding of atmospheric conditions. Weather forecasts and METARs often include ISA deviation.

### Effects on Aircraft:
- **Warmer than ISA** (ISA+):
  - Lower density → reduced performance
  - Longer takeoff roll
  - Reduced climb rate
  - Higher density altitude
  - **Thermals may be stronger** (more surface heating!)

- **Cooler than ISA** (ISA-):
  - Higher density → better performance
  - Shorter takeoff roll
  - Better climb rate
  - **But thermals may be weaker** (less surface heating)

**Practical example**: On a summer day at Bex (400m):
- ISA temperature: 15 - (0.65 × 4) = 12.4°C
- Actual temperature: 28°C
- Deviation: **ISA +15.6** - very warm!
- Expect: longer takeoff, reduced climb, but strong thermals later

---

## Questions & Answers

### Q5: En ISA - Valeurs P, T et humidité en surface?
**English**: In ISA - What are the values of P, T and humidity at the surface?

**Réponse (FR)**:
- P = 1013,25 hPa
- T = 15°C
- HR = 0%

**Answer (EN)**:
- P = 1013.25 hPa
- T = 15°C
- RH = 0%

**Explanation**: The ISA standard atmosphere defines specific reference conditions at sea level: pressure of 1013.25 hPa, temperature of 15°C, and 0% humidity (completely dry air).

---

### Q5.2: Quelle est la température à 2000 m d'altitude?
**English**: What is the temperature at 2000m altitude?

**Réponse (FR)**: 15 - 6,5×2 = 15 - 13 = 2°C

**Answer (EN)**: 15 - 6.5×2 = 15 - 13 = 2°C

**Explanation**: Using the ISA temperature lapse rate of -0.65°C per 100m (or -6.5°C per 1000m), at 2000m altitude: T = 15 - (6.5 × 2) = 2°C.

---

### Q5.3: Quelle est la pression à environ 5000 m d'altitude?
**English**: What is the pressure at approximately 5000m altitude?

**Réponse (FR)**: Divisée /2 soit environ 500 hPa

**Answer (EN)**: Divided by 2, so approximately 500 hPa

**Explanation**: Atmospheric pressure halves approximately every 5500 meters. Since 5000m is close to 5500m, the pressure is roughly half of the sea level pressure: 1013 / 2 ≈ 500 hPa.

---

*Related topics*: [Temperature](02_temperature.md), [Pressure](03_pressure.md), [Density](04_density.md), [Altimetry](06_altimetry.md)
