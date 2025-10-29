# Adiabatic Processes (Transformations Adiabatiques)

**📖 Reference**: [Lesson 2 Slides - Adiabatic Processes](slides/meteo2_part-01-50.pdf#page=10)

## Why This Matters for Glider Pilots

Understanding adiabatic processes is THE foundation of thermal soaring because:
- **Every thermal you fly** follows adiabatic cooling as it rises
- **Cloud base altitude** is determined by adiabatic cooling rates
- **Thermal strength** changes at the condensation level due to different lapse rates
- **Temperature calculations** let you predict conditions at altitude
- **The -1°C/100m and -0.6°C/100m rates** are the most important numbers in soaring meteorology
- Understanding these processes helps you decide when and where to fly

## What Does "Adiabatic" Mean?

[Adiabatic](https://en.wikipedia.org/wiki/Adiabatic_process) comes from Greek: "a-" (not) + "diabatos" (passable), literally meaning "not passable" or "impassable" - in this context, meaning heat cannot pass through.

**Definition**: An adiabatic process is one where **no heat is exchanged** with the surrounding environment.

**What this means in simple terms**: When a thermal rises, it's like an invisible bubble moving through the atmosphere. Air is a poor conductor of heat, so the bubble doesn't exchange heat with the air around it - it's thermally isolated in its own little world. Any temperature change comes purely from internal expansion or compression, not from heat flowing in or out.

**Analogy**: Think of a thermos bottle. The thermal is like coffee in a thermos - insulated from its surroundings. When you take the thermos up a mountain, the coffee inside doesn't instantly become the same temperature as the cold outside air because the thermos insulates it. Similarly, a rising thermal bubble doesn't exchange heat with the surrounding air. However, unlike the coffee (which stays at constant temperature in a perfect thermos), the thermal DOES change temperature - not from heat exchange, but from the work of expansion as pressure drops.

**Why air is adiabatic**: Air is an excellent insulator. A rising thermal bubble changes temperature so quickly through expansion (within seconds) that there's no time for significant heat to flow in or out. Heat conduction through air is very slow, but the bubble is rising fast!

**Real-world confirmation**: This is why thermals have distinct boundaries. If you've ever flown through the edge of a thermal, you know exactly where it starts and stops - you feel the temperature change on your face and see it on your instruments. If heat exchanged rapidly with surroundings, thermals would blend into the surrounding air and have fuzzy edges. But they don't - they maintain their identity as they rise, which proves they're adiabatic.

## The Two Key Processes

### 1. Adiabatic Expansion (Détente Adiabatique)

**What happens when air rises**:

1. **Altitude increases** → atmospheric pressure decreases (there's less air "weight" pressing down from above)
2. **Lower external pressure** → air parcel expands (like releasing a compressed spring or letting a balloon expand)
3. **Expansion requires energy** → the air molecules use their own kinetic (motion) energy to push outward and expand
4. **Internal energy decreases** → since molecules are moving slower, **temperature drops**

**Result**: Rising air cools, even though no heat is removed! This seems counterintuitive at first - how can something cool down without losing heat? The key is that the energy isn't "lost" - it's converted from kinetic energy (temperature) into work (expansion).

**Intuitive explanation**: Imagine a can of compressed air (like for cleaning keyboards). When you spray it, the air expands rapidly as it leaves the nozzle, and the can gets cold! The expanding air does "work" pushing against the outside pressure, using up its internal energy, which we measure as temperature. The same thing happens in a rising thermal, just more slowly.

**Rate of cooling**: Depends on whether air is saturated or not (see below)

**Practical implication for pilots**: This is why mountain tops are cold even in summer! It's not just that they're "closer to cold space" - it's because air has expanded and cooled adiabatically as it rose up the mountain slope.

### 2. Adiabatic Compression (Compression Adiabatique)

**What happens when air descends**:

1. **Altitude decreases** → atmospheric pressure increases
2. **Higher external pressure** → air parcel compresses
3. **Compression adds energy** → work converts to internal energy
4. **Internal energy increases** → **temperature rises**

**Result**: Descending air warms, even though no heat is added!

**For pilots**: This is why:
- **Sink between thermals** often feels warmer
- **Föhn winds** descending mountains are hot and dry
- **Air in the lee of mountains** is warmer than on windward side

## The Two Adiabatic Lapse Rates

A "[lapse rate](https://en.wikipedia.org/wiki/Lapse_rate)" (gradient) is the rate at which temperature changes with altitude.

### Dry Adiabatic Lapse Rate (DALR) - Gradient Adiabatique Sec

**Rate**: **-1°C per 100 meters** (-10°C per 1000m)

**MEMORIZE THIS NUMBER!** It's the single most important number in soaring meteorology.

**Applies to**: Unsaturated air (relative humidity < 100%) - basically any air that hasn't formed a cloud yet

**What this means**: An unsaturated air parcel rising 1000m will cool by exactly 10°C through expansion alone. This is remarkably constant and reliable - it doesn't matter if it's summer or winter, humid or dry, as long as the air is unsaturated, it cools at this rate.

**Why exactly -1°C/100m?** This comes from the thermodynamic properties of air (heat capacity, molecular weight) and the rate at which atmospheric pressure decreases with altitude. The math is complex, but the result is beautifully simple and consistent!

**Example**:
- Surface: T = 25°C, RH = 60% (unsaturated - not cloudy yet)
- At 1000m: T = 15°C (cooled 10°C)
- At 2000m: T = 5°C (cooled another 10°C)
- At 3000m: T = -5°C (cooled another 10°C - yes, it can be below freezing at altitude on a hot summer day!)

**For pilots**: This applies to:
- Thermals **below cloud base** (the part where you're circling in clear air)
- "Blue" thermals (no clouds form at all)
- Any air that hasn't reached its dew point
- **Every time you climb in clear air, you're experiencing DALR!**

**Practical experience**: Next time you're thermaling on a blue day, watch your flight computer's temperature display. If you climb 500m, the temperature should drop by about 5°C. This is the DALR in action! If it doesn't drop this much, something else is going on (maybe you drifted into warmer air, or there's an inversion).

### Saturated Adiabatic Lapse Rate (SALR) - Gradient Adiabatique Saturé

**Rate**: **~-0.6°C per 100 meters** (~-6°C per 1000m)

**ALSO MEMORIZE THIS NUMBER!** It's the second most important number in soaring.

*Note: Can vary from -0.4 to -0.9°C/100m depending on temperature and pressure, but -0.6°C/100m is the typical value*

**Applies to**: Saturated air (relative humidity = 100%, condensation actively occurring) - basically, inside a cloud!

**What this means**: A saturated air parcel (inside a cloud) cools more slowly than unsaturated air because condensation continuously releases latent heat (see [Phase Changes and Latent Heat](01_phase_changes_latent_heat.md) for why).

**Why slower? The energy balance**:
- Air still wants to cool from expansion at the normal rate: -1°C/100m
- BUT condensing water vapor releases latent heat at about: +0.4°C/100m
- These two effects work against each other
- Net result: -1 + 0.4 = **-0.6°C/100m**

It's like climbing up a hill while someone is helping push you from behind - you still go up (cool down), but not as fast!

**Example**:
- Cloud base: T = 15°C, RH = 100% (saturated - you just entered the cloud)
- At 1000m above base: T = 9°C (cooled only 6°C instead of 10°C)
- At 2000m above base: T = 3°C (cooled another 6°C)
- **Compare to DALR**: If this had been unsaturated air, it would be at -5°C at 2000m above cloud base. Being 8°C warmer makes the air much more buoyant!

**For pilots**: This applies to:
- Thermals **inside clouds** (cumulus, cumulonimbus)
- Any air where active condensation is occurring (cloud is forming/growing)
- This is why cloud thermals are STRONGER! The extra heat from condensation makes the thermal warmer relative to its surroundings, increasing buoyancy

**Practical experience**: Many pilots report feeling a distinct "kick" or surge when entering cloud base. Your vario might jump from +2 m/s to +3 or +4 m/s. This isn't just psychological - it's the latent heat effect starting to help! The thermal is now cooling slower (SALR vs DALR), so it stays warmer relative to the environment, generating more buoyancy and stronger lift.

**Real-world confirmation**: On a day with cloud base at 2000m, thermal strength below base might be 2-3 m/s, but inside the cloud it might be 4-6 m/s. That's not coincidence - it's the -0.6°C/100m vs -1°C/100m difference creating extra buoyancy!

## Comparison: Dry vs. Saturated

| Aspect | Dry Adiabatic | Saturated Adiabatic |
|--------|---------------|---------------------|
| **Rate** | -1°C/100m | -0.6°C/100m |
| **Applies to** | Below cloud base | Inside clouds |
| **Humidity** | RH < 100% | RH = 100% |
| **Phase change** | None | Condensation occurring |
| **Energy** | Only expansion | Expansion + latent heat |
| **Thermal strength** | Moderate | Strong! |

## The Standard Atmosphere (ISA) Lapse Rate

For comparison, the [International Standard Atmosphere](https://en.wikipedia.org/wiki/International_Standard_Atmosphere) (ISA) uses:

**Rate**: **-0.65°C per 100 meters** (-6.5°C per 1000m)

**What this is**: The average temperature profile of the entire atmosphere (not a parcel!)

**Why different?**: The ISA represents the ambient atmospheric temperature structure, not a rising parcel. It's between the dry and saturated rates because the atmosphere contains a mix of rising and sinking air, with varying humidity levels.

**For pilots**: Compare the actual atmospheric lapse rate to the adiabatic rates to determine stability (covered in next section).

## Practical Temperature Calculations

### Example 1: Dry Thermal to Cloud Base

**Given**:
- Surface temperature: 20°C
- Dew point: 10°C
- Thermal rises to cloud base

**Calculate cloud base**:
- Spread: 20° - 10° = 10°C
- Cloud base: (10 / 0.8) × 100m = **1250m AGL**

**Temperature at cloud base**:
- Cooling rate: -1°C/100m (dry)
- Temperature drop: 1250m × (-1°C/100m) = -12.5°C
- Temperature at base: 20° - 12.5° = **7.5°C**

**Check**: At cloud base, T should equal Td:
- T cooled from 20° to 7.5° at rate of -1°C/100m
- Td cooled from 10° to ~7.5° at rate of -0.2°C/100m ✓

### Example 2: Thermal Continues into Cloud

**Starting at cloud base** (from above):
- Altitude: 1250m AGL
- Temperature: 7.5°C
- Now saturated (in cloud)

**Thermal rises another 1000m**:
- New altitude: 2250m AGL
- Cooling rate: -0.6°C/100m (saturated)
- Temperature drop: 1000m × (-0.6°C/100m) = -6°C
- Temperature at 2250m: 7.5° - 6° = **1.5°C**

**Complete picture**:
- 0m (surface): 20°C, clear
- 1250m (cloud base): 7.5°C, cloud starts
- 2250m (cloud top): 1.5°C, in cloud

### Example 3: Question 12 from Q&A

**Given**:
- Sion airfield: 20°C at ground level
- Air parcel rises to 2000m (unsaturated)
- Conditions are unstable

**Calculate**:
- Rise: 2000m
- Cooling: 2000m × (-1°C/100m) = -20°C
- Final temperature: 20° - 20° = **0°C**

**Answer: C) 0°C**

### Example 4: Question 13 from Q&A

**Given**:
- Sion airfield: 20°C at ground level
- Air reaches dew point at 1000m
- Continues to 2000m

**Calculate**:
- **0 to 1000m** (dry): 1000m × (-1°C/100m) = -10°C
  - Temperature at 1000m: 20° - 10° = **10°C**
- **1000 to 2000m** (saturated): 1000m × (-0.6°C/100m) = -6°C
  - Temperature at 2000m: 10° - 6° = **4°C**

**Answer: A) 4°C**

## Why This Creates Stronger Thermals in Clouds

**Below cloud base** (dry adiabatic):
- Thermal cools at -1°C/100m
- Surrounding air might cool at -0.65°C/100m (ISA)
- Temperature difference small → moderate lift

**In cloud** (saturated adiabatic):
- Thermal cools at -0.6°C/100m (latent heat released!)
- Surrounding air still cools at -0.65°C/100m or more
- Thermal is now WARMER than surroundings → stronger lift!

**The transition at cloud base**:
- Below: thermal cooling faster than environment
- At cloud base: condensation starts, thermal gets boost
- Above: thermal cooling slower than environment
- Result: Often feel a "kick" of stronger lift at cloud base!

---

## Questions & Answers

### Q8: Expliquer ce qu'est la détente
**English**: Explain what expansion (détente) is.

**Réponse (FR)**: La détente est l'augmentation de volume d'une parcelle d'air qui s'élève, sous l'effet de la baisse de pression atmosphérique en altitude.

**Answer (EN)**: Expansion is the increase in volume of an air parcel that rises, due to the decrease in atmospheric pressure with altitude.

**Explanation**: Think of a helium balloon released at sea level - as it rises, external pressure decreases, and the balloon expands. The same happens with thermal bubbles! This expansion is what causes the temperature to drop (the air does "work" expanding against external pressure, using internal energy, which appears as cooling).

---

### Q9: Expliquer ce que signifie « adiabatique »
**English**: Explain what "adiabatic" means.

**Réponse (FR)**: Adiabatique signifie sans échange de chaleur avec le milieu environnant.

**Answer (EN)**: Adiabatic means without heat exchange with the surrounding environment.

**Explanation**: When a thermal rises, it changes temperature purely due to expansion/compression, NOT because heat flows in or out. Air is a poor heat conductor, and thermals rise quickly, so there's no time for heat transfer with surrounding air. This is why we can use simple formulas (-1°C/100m, -0.6°C/100m) to predict temperatures - the process is purely mechanical (pressure-volume), not thermal (heat flow).

---

### Q10: Donner les valeurs des gradients adiabatiques sec et saturé
**English**: Give the values of the dry and saturated adiabatic gradients.

**Réponse (FR)**:
- Gradient adiabatique sec: **-1°C / 100 m**
- Gradient adiabatique saturé: **-0,6°C / 100 m**

**Answer (EN)**:
- Dry adiabatic gradient: **-1°C / 100 m**
- Saturated adiabatic gradient: **-0.6°C / 100 m**

**Explanation**: These are the two most important numbers in soaring meteorology!
- **-1°C/100m**: Memorize this! Any unsaturated air rising or sinking changes temperature at this rate.
- **-0.6°C/100m**: Applies inside clouds where condensation releases latent heat, slowing the cooling.

The 0.4°C/100m difference is due to latent heat release during condensation. This seemingly small difference has huge effects - it makes cloud thermals significantly stronger than blue thermals!

---

### Q12: Sur l'aérodrome de Sion, il fait 20 °C au sol. En supposant que les conditions sont instables, quelle sera la température d'une parcelle d'air non saturée qui s'élève jusqu'à environ 2000 m de hauteur sol?
**English**: At Sion airfield, it's 20°C at ground level. Assuming unstable conditions, what will be the temperature of an unsaturated air parcel that rises to about 2000m above ground?

A) 6 °C
B) 8 °C
C) **0 °C** ✓
D) on ne peut pas répondre sans connaître le profil de température de l'atmosphère

**Réponse (FR)**: C) 0 °C

**Answer (EN)**: C) 0 °C

**Calculation**:
- Starting temperature: 20°C
- Rise: 2000m
- Air is unsaturated → use dry adiabatic rate
- Cooling: 2000m × (-1°C/100m) = -20°C
- Final temperature: 20° - 20° = **0°C**

**Explanation**: Since the air is unsaturated (hasn't reached its dew point), it cools at the dry adiabatic rate of -1°C/100m throughout its ascent. After rising 2000m, it has cooled by 20°C. Note that we DON'T need to know the environmental temperature profile - that's the beauty of adiabatic processes! The parcel's temperature change depends only on how much it rises/falls, not on the surrounding air temperature.

---

### Q13: Sur l'aérodrome de Sion, il fait 20 °C au sol. En supposant que les conditions sont instables, quelle sera la température d'une parcelle d'air qui s'élève jusqu'à environ 2000 m de hauteur sol et qui atteint son point de rosée à 1000 m sol?
**English**: At Sion airfield, it's 20°C at ground level. Assuming unstable conditions, what will be the temperature of an air parcel that rises to about 2000m above ground and reaches its dew point at 1000m above ground?

A) **4 °C** ✓
B) 8 °C
C) 0 °C
D) on ne peut pas répondre sans connaître le profil de température de l'atmosphère

**Réponse (FR)**: A) 4 °C

**Answer (EN)**: A) 4 °C

**Calculation**:
- **Phase 1 (0 to 1000m) - Unsaturated**:
  - Cooling: 1000m × (-1°C/100m) = -10°C
  - Temperature at 1000m: 20° - 10° = 10°C
- **Phase 2 (1000m to 2000m) - Saturated** (cloud!):
  - Cooling: 1000m × (-0.6°C/100m) = -6°C
  - Temperature at 2000m: 10° - 6° = **4°C**

**Explanation**: This is a two-phase problem:
1. Below 1000m: air is dry → cools at -1°C/100m → loses 10°C
2. Above 1000m: air is saturated (condensation, cloud!) → cools at -0.6°C/100m → loses 6°C

Total cooling: 10° + 6° = 16°C (compare to 20°C if it stayed dry the whole way!)

This demonstrates why cloud base matters - the cooling rate changes there, affecting thermal strength and temperature at altitude.

---

## Abbreviations and Key Terms {#abbreviations}

**Adiabatic Abbreviations**:
- **DALR**: Dry Adiabatic Lapse Rate - Rate at which unsaturated air cools when rising (-1°C/100m)
- **SALR**: Saturated Adiabatic Lapse Rate - Rate at which saturated air cools when rising (~-0.6°C/100m)
- **ISA**: International Standard Atmosphere - Standard reference atmosphere
  - Temperature: 15°C at sea level
  - Pressure: 1013.25 hPa at sea level
  - Lapse rate: -0.65°C/100m (average for whole atmosphere)
- **ELR**: Environmental Lapse Rate - Actual temperature profile of atmosphere (varies)

**Temperature and Altitude**:
- **°C/100m**: Degrees Celsius per 100 meters - Standard unit for lapse rates
- **°C/1000m**: Degrees Celsius per 1000 meters - Sometimes used for larger scale
  - DALR: -10°C/1000m
  - SALR: -6°C/1000m
- **ft**: Feet - Imperial unit (1000 ft ≈ 305m)
- **fpm**: Feet per minute - Vertical velocity (1 m/s ≈ 196 fpm)

**Process Terms**:
- **Adiabatic**: No heat exchange with surroundings (from Greek "not passable")
- **Détente**: Expansion (French term often used)
- **Compression**: Reduction in volume (descending air)
- **Expansion**: Increase in volume (rising air)

**Cloud/Thermal Terms**:
- **LCL**: Lifting Condensation Level - Altitude where cloud base forms (same as cloud base)
- **Cloud Base**: Bottom of clouds - Where T = Td (temperature equals dew point)
- **Thermal**: Rising column of warm air (updraft)
- **Blue Thermal**: Thermal without cloud (air doesn't reach saturation)

**Meteorological Concepts**:
- **Parcel**: An imaginary "bubble" of air tracked as it rises/falls
- **Environment**: The surrounding atmosphere (as opposed to the parcel)
- **Buoyancy**: Upward force when air parcel is warmer (less dense) than surroundings
- **Latent Heat**: Energy released during condensation (warms rising saturated air)

**Aviation References**:
- **Sion**: Example Swiss airport (elevation ~482m MSL)
- **AGL**: Above Ground Level - Height above terrain
- **MSL**: Mean Sea Level - Standard altitude reference

---

*Related topics*: [Latent Heat](01_phase_changes_latent_heat.md), [Humidity](02_humidity.md), [Stability](04_atmospheric_stability.md), [Convection](05_convection_thermals.md)
