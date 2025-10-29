# Altimetry (Altimétrie)

**📖 Reference**: [Lesson 1 Slides - Altimetry](slides/meteo1_part-01-50.pdf#page=13)

## Why This Matters for Glider Pilots

Altimetry is **CRITICAL FOR SAFETY**:
- **Terrain clearance** - know your height above obstacles!
- **Airspace compliance** - enter controlled airspace only at correct altitude
- **Communication** - Air Traffic Control (ATC) needs accurate altitude reports
- **Circuit patterns** - correct pattern altitude for safe operations
- **Wrong altimeter setting** can lead to:
  - Controlled flight into terrain (CFIT)
  - Airspace violations
  - Collision risk with other traffic
- Understanding QNH/QFE/FL is **essential** for exam and practical flying

## The Altimeter

An **[altimeter](https://en.wikipedia.org/wiki/Altimeter)** is essentially an **aneroid barometer** calibrated to show altitude instead of pressure.

**Principle**: As you climb, atmospheric pressure decreases, and the altimeter converts this pressure change into altitude using the ISA standard atmosphere relationship.

**What this means**: Your altimeter doesn't directly measure altitude - it measures pressure and calculates altitude based on that pressure. This is why the altimeter setting is crucial!

## Altimeter Settings (Calages)

The altimeter must be "set" to a reference pressure to display meaningful altitude information.

### Three Main Settings:

## 1. [QFE](https://en.wikipedia.org/wiki/Altimeter_setting#QFE) - Field Elevation

**QFE** = **Q**-code for **F**ield **E**levation = **Pressure measured at airfield level**

**When set to QFE, the altimeter shows:**
- **Height above the airfield** (hauteur par rapport au sol)
- **0 feet when on the ground** at that airfield
- **Relative height** - changes if you fly to different airfield!

**Use**: Circuit work, knowing height above runway

**Advantages**:
- Immediately know your height above the runway - useful for circuit flying
- No mental math required for pattern altitude

**Disadvantages**:
- Changes from airfield to airfield
- Doesn't tell you terrain clearance when away from the field
- Not standard for cross-country flying

**Example**: At Bex, set QFE (960 hPa). Altimeter shows 0 ft on ground. At 1000 ft, you're 1000 ft above Bex runway.

---

## 2. [QNH](https://en.wikipedia.org/wiki/Altimeter_setting#QNH) - Regional Pressure Setting

**QNH** = **Q**-code for **N**autical **H**eight = **Pressure corrected to sea level using ISA conditions**

**When set to QNH, the altimeter shows:**
- **Altitude above mean sea level (AMSL)** - altitude au-dessus du niveau moyen de la mer
- **Field elevation when on the ground**
- Corresponds to elevation on topographic maps!

**Use**:
- **Navigation** (terrain clearance from maps)
- **Below transition altitude** (typically FL100-130 in Switzerland)
- **Standard setting for Visual Flight Rules (VFR) flight**
- Cross-country flying

**Advantages**:
- Shows altitude matching topographic maps - excellent for terrain clearance
- Same reading for all aircraft in the region
- Standard for VFR (Visual Flight Rules) operations

**Disadvantages**:
- Doesn't directly show height above ground
- Changes regionally as pressure systems move
- Must be updated during flight (get from Automatic Terminal Information Service (ATIS), tower, or nearby stations)

**Example**: At Bex (elevation 400m), QNH = 1025 hPa. On ground, altimeter shows 400m. At FL (altimeter showing) 2400m, you're 2000m above the field, but 2400m above sea level.

**Critical safety note**: Always use QNH for terrain clearance! Your charts show elevations AMSL.

---

## 3. Standard Setting (1013.25 hPa) - Flight Levels

**When set to 1013.25 hPa ([Standard Pressure](https://en.wikipedia.org/wiki/Flight_level)), the altimeter shows:**
- **Flight Level (FL)** - height above the 1013.25 hPa pressure surface
- **NOT altitude above sea level!**
- **NOT height above ground!**

**[Flight Levels](https://en.wikipedia.org/wiki/Flight_level)**:
- FL = altitude in hundreds of feet with altimeter set to 1013.25 hPa
- **FL 100** = 10,000 feet above 1013.25 hPa pressure surface
- **FL 050** = 5,000 feet above 1013.25 hPa surface
- Sometimes written as "F100" or "FL100"

**Use**:
- **Above transition altitude** (Switzerland: typically FL100)
- Ensures all aircraft use same reference pressure
- Separates traffic safely - everyone reads the same thing!
- Standard worldwide above certain altitudes

**Advantages**:
- All aircraft on same reference - no regional QNH variations
- Safer traffic separation
- Simpler - no need to update pressure setting

**Disadvantages**:
- Doesn't show terrain clearance
- Your true altitude varies with actual QNH
- Must transition to QNH when descending below transition altitude

**Example**: Flying at FL 100 in Switzerland:
- If QNH = 1013 hPa: You're at ~10,000 ft AMSL (3000m)
- If QNH = 1025 hPa: You're at ~10,336 ft AMSL (~3100m) - higher than FL indicates!
- If QNH = 1000 hPa: You're at ~9,632 ft AMSL (~2900m) - lower than FL indicates!

**Remember**: "High to low, look out below!" - when flying from high pressure to low pressure area, you're lower than your altimeter shows.

---

## QFF vs QNH

- **[QFF](https://en.wikipedia.org/wiki/Altimeter_setting#QFF)**: Pressure corrected to sea level using **actual** temperature
- **QNH**: Pressure corrected to sea level using **ISA** temperature
- **Usually very similar**, QNH is standard in aviation
- QFF is used by meteorologists for weather maps
- QNH is used by pilots for altimetry

**What this means**: You'll see QFF on weather charts, but always use QNH for your altimeter! They're close enough that it doesn't usually matter, but QNH is the aviation standard.

---

## Pressure Corrections

### Rule: **~8.5 meters (or 28 feet) per hPa**

When actual pressure differs from altimeter setting:
- **Higher actual pressure**: You're **lower** than altimeter shows
- **Lower actual pressure**: You're **higher** than altimeter shows

**Example**: You set 1013 hPa but actual QNH is 1025 hPa (12 hPa difference)
- Difference: 12 hPa × 8.5 m/hPa = 102 meters
- You're 102m LOWER than your altimeter indicates!
- **Danger**: Terrain clearance reduced!

### Temperature Effects

**If warmer than ISA**:
- Air is less dense (expanded vertically)
- Pressure levels are higher than ISA predicts
- You're **HIGHER** than altimeter indicates
- QFF < QNH (small difference)

**If colder than ISA**:
- Air is more dense (contracted vertically)
- Pressure levels are lower than ISA predicts
- You're **LOWER** than altimeter indicates
- QFF > QNH (small difference)

**Critical Safety Rule**: **"From hot to cold, look out below!"**
→ Flying from warm air to cold air, you'll be LOWER than your altimeter shows.
→ **Especially dangerous in mountainous terrain in winter!**

**Example**: Flying from warm valley (ISA+10) to cold mountain region (ISA-10):
- Temperature effect can easily be 200-300m altitude error
- Always add safety margin in cold conditions
- This effect is ADDITIONAL to pressure corrections!

**Real-world scenario**: Imagine departing from a warm valley on a winter day at 15°C (ISA+10 at that altitude). You're flying toward mountains where the temperature is -5°C (ISA-10). Your altimeter is calibrated for ISA conditions, so in the cold mountain air, the pressure levels are compressed (more dense air). If your altimeter shows 2500m above sea level, you might actually be at only 2300m! If you're planning to cross a 2400m ridge, you could find yourself in a very dangerous situation, thinking you have 100m clearance when you actually have none. This is why mountain pilots always add a generous safety margin in cold weather and never fly close to minimum safe altitudes.

---

## Flight Level Example

**Situation**: Flying at FL 120 (altimeter set to 1013.25)
- Over Zurich: QNH = 1025 hPa
- Over Munich: QNH = 1005 hPa

**What happens to your true altitude?**
- The FL 120 surface follows the 1013 hPa isobar
- As pressure drops (Zurich→Munich), the 1013 hPa surface gets lower
- **Your true altitude decreases** even though FL stays constant!

---

## Questions & Answers

### Q6: Quel calage choisir pour que l'altimètre indique:
**English**: Which setting to choose so the altimeter indicates:

**1) altitude par rapport au niveau moyen de la mer?**
**English**: altitude relative to mean sea level?

**Réponse (FR)**: QNH

**Answer (EN)**: QNH

---

**2) hauteur par rapport à l'aérodrome de départ?**
**English**: height relative to departure aerodrome?

**Réponse (FR)**: QFE

**Answer (EN)**: QFE

---

**3) hauteur par rapport à l'isobare 1013,25 hPa?**
**English**: height relative to the 1013.25 hPa isobar?

**Réponse (FR)**: 1013,25 hPa

**Answer (EN)**: 1013.25 hPa

---

### Q7: QNH 1025 à Bex. Au sol, qu'indique l'altimètre si vous le calez à 1025?
**English**: QNH 1025 at Bex. On the ground, what does the altimeter show if you set it to 1025?

**Réponse (FR)**: L'altitude du terrain, soit environ 400 m

**Answer (EN)**: The field elevation, approximately 400 m

**Explanation**: When set to QNH, the altimeter always shows altitude above mean sea level (AMSL). On the ground, it therefore shows the airfield's elevation, which is approximately 400 meters for Bex.

---

### Q8: [Diagram question with QFE=960, QNH=1010, elevation 700ft, flying at 1000ft above ground]

**Calculate altitude at standard setting (1013.25)**

**Réponse (FR)**: 1000 + 700 + 3×28 = 1784 ft

**Answer (EN)**: 1000 + 700 + 3×28 = 1784 ft

**Explanation**:
- Height above ground: 1000 ft
- Ground elevation: 700 ft
- Difference between 1013.25 and QNH (1010): 3 hPa
- 3 hPa × 28 ft/hPa = 84 ft additional
- Total: 1000 + 700 + 84 = 1784 ft

---

### Q9: Nous sommes à Bex, altitude 400m, QNH=1005. Qu'indique l'altimètre calé sur QNH au sol?
**English**: We are at Bex, altitude 400m, QNH=1005. What does the altimeter set to QNH show on the ground?

**Réponse (FR)**: L'altimètre calé sur le QNH indique l'altitude par rapport au niveau de la mer, soit 400 m tant que l'on n'a pas décollé (ou 1000 ft selon les unités)

**Answer (EN)**: The altimeter set to QNH shows altitude relative to sea level, so 400 m as long as we haven't taken off (or 1000 ft depending on units)

---

### Q10: Même situation, qu'indique l'altimètre calé sur QFE au sol?
**English**: Same situation, what does the altimeter set to QFE show on the ground?

**Réponse (FR)**: L'altimètre calé sur le QFE indique la hauteur par rapport au sol, soit 0 ft tant que l'on n'a pas décollé

**Answer (EN)**: The altimeter set to QFE shows height above ground, so 0 ft as long as we haven't taken off

---

### Q11: Même situation, en vol à 2000 ft au-dessus du sol. Qu'indiquent QNH et QFE?
**English**: Same situation, flying at 2000 ft above ground. What do QNH and QFE show?

**Réponse (FR)**:
- QNH: 3000 ft (1000 + 2000)
- QFE: 2000 ft

**Answer (EN)**:
- QNH: 3000 ft (field elevation 1000 + height 2000)
- QFE: 2000 ft (height above field)

**Explanation**: QNH adds the field elevation to your height above ground, while QFE only shows height above the departure airfield.

---

*Related topics*: [Pressure](03_pressure.md), [ISA Standard Atmosphere](05_isa_standard_atmosphere.md)
