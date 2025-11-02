# Atmospheric Pressure (Pression atmosphérique)

**📖 Reference**: [Lesson 1 Slides - Pressure](slides/meteo1_part-01-50.pdf#page=7)

## What is Atmospheric Pressure?

[Atmospheric pressure](https://en.wikipedia.org/wiki/Atmospheric_pressure) is the weight of the column of air above a given point. Air molecules have mass, and gravity pulls them downward, creating pressure on surfaces below.

**Pressure = Weight of atmospheric column above**

**What this means**: At sea level, you have roughly 10 km of air above you! All those air molecules pressing down create pressure. As you climb, there's less air above you, so pressure decreases.

## Why This Matters for Glider Pilots

Pressure understanding is critical because:
- **Altimeters are pressure instruments** - they convert pressure to altitude
- **Pressure changes affect altimeter readings** - you must set QNH correctly
- **Pressure systems drive weather** - highs bring good weather, lows bring bad weather
- **Pressure gradients create wind** - wind flows from high to low pressure
- **Weather forecasting** relies heavily on pressure patterns
- **Understanding QNH/QFE/FL** is essential for safe flight and communication

## Pressure Units

### [Hectopascal](https://en.wikipedia.org/wiki/Pascal_(unit)) (hPa) - Standard in Aviation
- **1 hPa = 1 millibar (mbar)** = 100 Pascal (Pa)
- Most commonly used in meteorology and aviation
- **Sea level standard**: 1013.25 hPa

**What this means**: The hectopascal is the standard unit you'll see in METARs, TAFs, and weather charts. It replaced the millibar but they're numerically identical (1 hPa = 1 mbar).

### Millimeters of Mercury (mmHg)
- Used in some countries and medical applications
- **Sea level standard**: 760 mmHg
- Based on barometric mercury column height
- Also called "Torr"

### Conversion
- **1013.25 hPa = 1013.25 mbar = 760 mmHg**
- Quick rule: **4 hPa ≈ 3 mmHg**

## Pressure Measurement

### [Barometer](https://en.wikipedia.org/wiki/Barometer) (Baromètre)
- Instrument that measures atmospheric pressure
- Invented by Evangelista Torricelli in 1643

### [Aneroid Barometer](https://en.wikipedia.org/wiki/Barometer#Aneroid_barometers) (Baromètre anéroïde)
- Contains sealed metal chambers (almost evacuated)
- External air pressure compresses or expands chambers
- Mechanical linkage shows pressure on dial
- **Used in aircraft altimeters!**
- [Here](https://www.youtube.com/watch?v=0xkNFN5j6Wo) is a Youtube Video explaining how it works.

**What this means**: Your glider's altimeter is essentially an aneroid barometer that's been calibrated to show altitude instead of pressure. Understanding this helps you understand why altimeter settings matter.

## Pressure Variation with Altitude

**Key principle**: Pressure **decreases exponentially** with increasing altitude

**Why?** As you climb, there's less air above you, so less weight pressing down. The relationship is exponential, not linear - pressure decreases faster at lower altitudes.

### Pressure Halves Every ~5500m
- **Sea level**: ~1013 hPa
- **~5500m (FL180)**: ~500 hPa (halved)
- **~11000m**: ~250 hPa (halved again)

**What this means**: This "halving rule" is a quick mental check. At typical gliding altitudes (up to 3000m), pressure drops to roughly 700 hPa.

### Typical Pressure-Altitude Relationships (ISA)
| Pressure | Approximate Altitude |
|----------|---------------------|
| 1013 hPa | Sea level |
| 850 hPa  | 1500 m (typical cloud base) |
| 700 hPa  | 3000 m (good soaring altitude) |
| 500 hPa  | 5500 m (wave soaring territory) |

### Rate of Decrease Near Surface
- **~1 hPa per 8.5 meters** altitude gain (or **~12 hPa per 100m**)
- **~1 hPa per 28 feet** altitude gain

**What this means**: This is the critical rule for altimetry! If QNH is 1025 hPa and you set 1013 hPa, you're "off" by 12 hPa × 8.5 m/hPa ≈ 100 meters. Your altimeter will read 100m higher than your true altitude.

## Pressure Systems


### Here are some links to understand the Coriolis Force

- [Video on the Coriolis Effect](https://www.youtube.com/watch?v=kCbMKSZZO9w)
- [Video on the Coriolis Effect with Drones](https://www.youtube.com/watch?v=okaxKzoyMK0) - a very nice demonstration on a merry go-around
- [Video with a good water jet demonstration](https://www.youtube.com/watch?v=w0Rr6UJGhS4) and [a similar video](https://www.youtube.com/watch?v=6L5UD240mCQ) with a ceiling camera
- [Very short video which bridges to the spin direction](https://www.youtube.com/watch?v=HIyBpi7B-dE)
- [Epic Flight Academy](https://www.youtube.com/watch?v=N_-Fjfl-abc) has a great set of videos out there, but fell short (for me anyway) in explaining the Anticyclone
- [This](https://youtu.be/1Y1Qi821n-s?t=147) Video explained it best for me
- So in summary, I'd suggest to watch [this video](https://www.youtube.com/watch?v=il5TPcxrjKQ) all the way to the end; it explains all three force elements (pressure gradient, coriolis force and friction) very well.

### [High Pressure / Anticyclone](https://en.wikipedia.org/wiki/High-pressure_area) (Anticyclone - A)
- Pressure higher than surrounding areas
- Air **descends** (subsidence)
- Air flows **outward** from center (divergence)
- Generally **good weather**: clear skies, light winds
- **Clockwise rotation** in Northern Hemisphere

**What this means for gliding**:
- **Excellent soaring weather!** Clear skies allow strong surface heating
- Descending air creates stability, but surface heating overcomes this during the day
- Expect good thermals on sunny days under high pressure
- Light winds = less mechanical turbulence

### [Low Pressure / Depression](https://en.wikipedia.org/wiki/Low-pressure_area) (Dépression - D)
- Pressure lower than surrounding areas
- Air **rises** (ascendance)
- Air flows **inward** toward center (convergence)
- Generally **poor weather**: clouds, precipitation, stronger winds
- **Counter-clockwise rotation** in Northern Hemisphere

**What this means for gliding**:
- **Poor soaring conditions** - clouds block solar heating
- Rising air sounds good, but it's widespread and weak, not concentrated like thermals
- Precipitation and low cloud bases limit operations
- Stronger winds = more turbulence and difficult conditions

### Other Pressure Features
- **[Ridge](https://en.wikipedia.org/wiki/Ridge_(meteorology)) (Dorsale)**: Extension of high pressure - often brings temporary improvement
- **[Trough](https://en.wikipedia.org/wiki/Trough_(meteorology)) (Talweg)**: Extension of low pressure - brings deteriorating conditions
- **[Col](https://en.wikipedia.org/wiki/Col_(meteorology)) (Marais barométrique)**: Saddle point between systems - light, variable winds

## Pressure Charts

Pressure is shown on weather maps using **[isobars](https://en.wikipedia.org/wiki/Contour_line#Isobars)** (lignes isobares):
- Lines connecting points of equal pressure (like elevation contours on a topographic map)
- Typically drawn every 5 hPa (1000, 1005, 1010, 1015...)
- **Closely spaced isobars** = strong [pressure gradient](https://en.wikipedia.org/wiki/Pressure_gradient) = **strong winds**
- **Widely spaced isobars** = weak pressure gradient = **light winds**

**What this means**: Reading a surface pressure chart is like reading a topographic map!
- Isobars close together = "steep slope" in pressure = strong winds
- Isobars far apart = "gentle slope" in pressure = light winds
- Wind flows roughly parallel to isobars (due to Coriolis effect)
- This helps you predict wind speed and direction for flight planning

**More Explanations** 

- [Here](https://www.youtube.com/watch?v=aUk4uRuqdRA) is a youtube video explaining Wind (horizontal movement of air) along
	- Pressure gradients, so Pressure Gradient Force (PGF),
	- Coriolis Force (CF), so with the spinning of the earth
	- Frictional Force (FF), working opposite e.g. PGF
- The spacing of isobars indicates the pressure gradient.
- The closer the spacing of isobars, the steeper the pressure gradient, the stronger the winds.
- The spacing is typically 4 mbar or 8 mbar

![](pgf.png)

![](isobars.png)




---

## Questions & Answers

### Q3: Unité de la pression atmosphérique?
**English**: What is the unit of atmospheric pressure?

**Réponse (FR)**: hPa

**Answer (EN)**: hPa (hectopascal)

**Explanation**: The hectopascal (hPa) is the standard unit for atmospheric pressure in aviation and meteorology. It is identical to the millibar (mbar). The standard sea level pressure is 1013.25 hPa.

---

*Related topics*: [Density](04_density.md), [Altimetry](06_altimetry.md), [ISA](05_isa_standard_atmosphere.md), [Wind](07_wind_basics.md)
