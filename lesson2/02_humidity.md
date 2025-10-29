# Humidity (Humidité)

**📖 Reference**: [Lesson 2 Slides - Humidity](slides/meteo2_part-01-50.pdf#page=5)

## Why This Matters for Glider Pilots

Understanding humidity is critical for thermal soaring because:
- **Cloud base height** is directly determined by humidity (dew point)
- **Thermal strength** changes dramatically at the condensation level
- **Predicting soaring conditions** requires understanding humidity patterns
- **Blue days vs. cu days** depend on air humidity levels
- **Cross-country planning** needs accurate cloud base predictions
- Low humidity = high cloud base (or no clouds), high humidity = low cloud base

## Absolute Humidity (Humidité Absolue)

[Absolute humidity](https://en.wikipedia.org/wiki/Humidity#Absolute_humidity) is the **actual mass of water vapor per unit volume of air**.

**Unit**: grams of water vapor per cubic meter of dry air (g/m³)

**What this means in simple terms**: This tells you how many water molecules are actually floating around in the air, regardless of temperature. Think of it as counting the number of water vapor "passengers" in your air parcel.

**Real-world example**: Imagine you have a cubic meter box (about 3 feet on each side). On a humid summer day, that box might contain 20-30 grams of invisible water vapor - about the same weight as 20-30 sugar cubes! On a dry winter day, it might only contain 2-5 grams. The key point is that this measurement doesn't change with temperature - it's the actual amount of water present.

### Temperature Capacity Relationship

**Crucial concept**: **Warm air can hold MUCH more water vapor than cold air!**

Imagine air as a sponge:
- **Hot air** = Big sponge (can absorb lots of water)
- **Cold air** = Small sponge (can only hold a little water)

Example maximum capacity at different temperatures (this is critically important!):
- **30°C**: Can hold ~30 g/m³ (hot summer day)
- **20°C**: Can hold ~17 g/m³ (comfortable spring day)
- **10°C**: Can hold ~9 g/m³ (cool autumn day)
- **0°C**: Can hold ~5 g/m³ (freezing)
- **-10°C**: Can hold ~2 g/m³ (high altitude or winter)

**Notice**: The capacity at 30°C is 6 times larger than at 0°C! This dramatic difference is fundamental to cloud formation.

**This is why clouds form when air rises and cools!** When a thermal rises and cools, its capacity to hold water vapor shrinks. Eventually, the "sponge" is full (saturated) and can't hold any more. At that point, the excess water vapor must condense into visible droplets - and you have a cloud!

**Practical anecdote**: This is also why your car windows fog up on a cold morning. The warm, humid air from your breath hits the cold window, its temperature drops, its capacity shrinks, and the excess moisture condenses on the glass. The exact same physics creates clouds in the sky!

## Relative Humidity (Humidité Relative)

[Relative humidity](https://en.wikipedia.org/wiki/Humidity#Relative_humidity) (RH or HR) is the **ratio of actual water vapor to maximum possible water vapor** at a given temperature.

**Formula**:

```
Relative Humidity (%) = (Actual water vapor / Maximum water vapor at this temperature) × 100
```

**Unit**: Percentage (%)

### Understanding Relative Humidity

**RH = 50%** means the air contains **half** the water vapor it could hold at that temperature.

**RH = 100%** means the air is **saturated** - it holds the maximum possible water vapor. Any additional cooling will cause condensation (clouds/fog).

**RH = 0%** means completely dry air (extremely rare in nature).

### Why "Relative"?

The term "relative" is key - **humidity is relative to temperature!**

**Critical insight**: You can change relative humidity in TWO ways:
1. **Change the amount of water vapor** (add or remove moisture)
2. **Change the temperature** (affects maximum capacity)

## Dew Point Temperature (Point de Rosée - Td)

The [dew point](https://en.wikipedia.org/wiki/Dew_point) (Td) is **the temperature to which air must be cooled to reach 100% humidity (saturation)**.

**What this means in simple terms**: The dew point is the temperature at which invisible water vapor starts condensing into visible water droplets. It's the "magic number" where the air's capacity perfectly matches the amount of water it contains.

**Why "dew point"?** The name comes from morning dew on grass. As the ground cools overnight, the air temperature near the surface drops until it reaches the dew point. At that moment, water vapor condenses on the cool grass blades, forming dew. Same principle causes fog, clouds, and condensation on your cold drink glass!

### Key Properties of Dew Point

1. **Dew point never exceeds air temperature** - it's always ≤ current temperature
2. **The closer Td is to T, the more humid the air**:
   - T = 20°C, Td = 18°C → Very humid (90% RH)
   - T = 20°C, Td = 10°C → Moderately humid (52% RH)
   - T = 20°C, Td = 0°C → Dry (30% RH)
3. **When T = Td**, you're at 100% humidity → clouds or fog form!

### Dew Point and Cloud Base

**This is THE most important concept for predicting cloud base height!** Understanding this relationship is one of the most powerful skills a glider pilot can have.

A rising thermal cools at -1°C/100m (the dry adiabatic lapse rate - see [Adiabatic Processes](03_adiabatic_processes.md)) until it reaches its dew point temperature. At that precise altitude, the air becomes saturated and condensation begins = **cloud base**.

**Simple formula** (memorize this!):
```
Cloud base height (m AGL) = [(T surface - Td surface) / 0.8] × 100
```

Where:
- **T surface** = current air temperature at ground level (from METAR or weather station)
- **Td surface** = current dew point at ground level (from METAR or weather station)
- **0.8°C/100m** is an average convergence rate (temperature drops faster than dew point as air rises)
- **AGL** = Above Ground Level (height above the terrain beneath you, not sea level)

**Example calculation**:
- Surface temperature: 25°C (nice warm day)
- Surface dew point: 9°C (moderate humidity)
- Temperature difference (T-Td spread): 16°C
- Cloud base: (16 / 0.8) × 100 = **2000m AGL** (about 6,500 feet)

**Practical insight**: Check surface T and Td in the morning - you can predict cloud base for the entire day! This works because dew point stays relatively constant throughout the day (unlike temperature, which changes dramatically). So even in the morning when it's only 15°C, if Td is 9°C, you know that when afternoon heating pushes T up to 25°C, you'll have clouds at 2000m!

**Real-world pilot story**: Experienced cross-country pilots check the morning METAR, calculate the expected cloud base, and use this to plan their route. Flying under a 2000m cloud base is very different from a 1000m base (you have to work harder, turn tighter) or a 3000m base (you can relax more, cruise faster between thermals).

## Reaching Saturation - Two Methods

For clouds or fog to form, air must reach **100% relative humidity**. This happens through:

### 1. Isobaric Cooling (Refroidissement Isobare)

**"Isobaric" = constant pressure** - air cools without changing altitude.

**Mechanisms**:
- **Radiative cooling**: Ground cools at night, cools air above it → morning fog
- **Advection cooling**: Warm, moist air moves over cold surface → sea fog
- **Mixing**: Warm and cool air masses mix

**What this means**: This process creates fog and low stratus clouds. Happens at night or when warm air flows over cold surfaces (lakes, snow).

**For pilots**: Isobaric cooling creates stable conditions with low stratus - poor soaring weather!

### 2. Cooling by Expansion - Adiabatic (Refroidissement par Détente)

**"Adiabatic" = no heat exchange** - air cools purely from expansion as pressure decreases with altitude.

When air rises:
- Atmospheric pressure decreases
- Air parcel expands
- Expansion requires energy → temperature drops
- Eventually reaches dew point → clouds form

**Rate**: -1°C/100m for unsaturated air (dry adiabatic lapse rate)

**What this means**: This is how convective clouds (cumulus) form! Rising thermals cool adiabatically until they hit their dew point.

**For pilots**: This creates our soaring clouds - cumulus at the condensation level!

## How Relative Humidity Changes

### Example 1: Temperature Increases, Water Vapor Constant

**Morning**:
- T = 10°C, Td = 10°C
- RH = 100% (saturated - fog!)
- Air holds 9 g/m³, capacity is 9 g/m³

**Afternoon** (sun heats the air):
- T = 20°C, Td still = 10°C
- Same amount of water vapor (9 g/m³)
- But now capacity is 17 g/m³
- RH = (9/17) × 100 = **53%**

**What happened**: Temperature rose, so the "sponge" got bigger, but we didn't add more water. Result: RH dropped, fog burned off!

**For pilots**: This is why morning fog disappears and why thermal days often start with low clouds that burn off.

### Example 2: Air Rises and Cools

**At surface**:
- T = 20°C, Td = 10°C
- Actual water vapor: 9 g/m³
- Capacity: 17 g/m³
- RH = 60%

**At 1000m altitude** (air cooled -10°C):
- T = 10°C, Td = 10°C (dew point changes slower)
- Same water vapor: 9 g/m³
- New capacity: 9 g/m³
- RH = 100% → **Cloud forms!**

**What happened**: As the air rose and cooled, its capacity to hold water decreased until it matched the actual amount → saturation → cloud.

**For pilots**: This is your cloud base! The altitude where T drops to Td.

## Practical Applications for Glider Pilots

### Predicting Cloud Base

**Method 1 - Using T and Td spread**:
1. Get surface temperature (T) and dew point (Td) from [METAR](#abbreviations)/weather station
   - **[METAR](#abbreviations)** = Meteorological Aerodrome Report, a standardized weather observation format used worldwide at airports
   - Example METAR: "LSZS 121350Z 36005KT 9999 FEW040 **22/12** Q1015" - the 22/12 means T=22°C, Td=12°C
2. Calculate spread: T - Td
3. Estimate cloud base: spread × 125m per degree (rough rule of thumb)
4. Example: T=24°C, Td=12°C → spread=12° → base at ~1500m AGL

**How to get METAR data**: Visit aviation weather websites (aviationweather.gov, windy.com, etc.) or your national weather service. Most gliding apps also show METAR data automatically.

**Method 2 - Using convergence**:
- Temperature drops at ~1°C/100m
- Dew point drops at ~0.2°C/100m
- They converge at ~0.8°C/100m
- Cloud base = [(T-Td)/0.8] × 100m

### Blue Day or Cu Day?

The T-Td spread tells you what kind of soaring day to expect:

**Low humidity** (large T-Td spread, e.g., T=28°C, Td=8°C, spread=20°C):
- High cloud base (maybe 2500m) or no clouds at all
- "Blue" thermal day - thermals exist but aren't marked by clouds
- Need to mark thermals by other means (birds, dust devils, terrain features, instrument readings)
- Often stronger surface heating (no cloud shadows)
- **Challenge**: Finding thermals is harder, requires good technique and thermal sense
- **Advantage**: Can often fly higher without clouds limiting altitude, and no risk of overdevelopment

**High humidity** (small T-Td spread, e.g., T=22°C, Td=18°C, spread=4°C):
- Low cloud base (maybe 500m!)
- Good [cumulus (Cu)](#abbreviations) cloud development
- Easy to find thermals - just fly under the clouds!
- **Challenge**: May overcast if too humid, shading kills thermals
- **Advantage**: Navigation is easy, you can see where the lift is

Imagine a day when the cumulus clouds are forming so low that their bases are only 500 meters above your airfield. This happens when there's very high humidity (small T-Td spread). On one hand, it makes finding thermals incredibly easy - every cloud marks a thermal, and you can plan your route from cloud to cloud like stepping stones. On the other hand, if humidity is TOO high, those individual cumulus clouds might spread and merge into a complete overcast layer, blocking the sun and killing your thermals entirely. It's a delicate balance - you want enough humidity for clouds to mark the thermals, but not so much that it over-develops into instrument meteorological conditions (IMC)!

**Practical decision-making**:
- Spread > 15°C: Expect blue day, bring extra water, focus on thermal technique
- Spread 8-15°C: Ideal conditions! High enough for good climbs, clear enough to prevent overdevelopment
- Spread 3-8°C: Good cu day, easy soaring
- Spread < 3°C: Watch for low clouds or overdevelopment, may be marginal conditions

**Real anecdote**: I once launched on a day with T=25°C and Td=22°C (spread of only 3°C). Predicted cloud base was under 400m AGL! Sure enough, we had a "carpet" of very low stratocumulus that made soaring nearly impossible. The lesson: too much humidity can be as bad as too little!

### Morning Weather Check

Check the **T-Td spread** in morning weather reports:

- **Spread <3°C**: Risk of low clouds/fog - may not burn off
- **Spread 3-8°C**: Perfect! Good cu development expected
- **Spread 8-15°C**: Blue thermals or high cloud base
- **Spread >15°C**: Very dry - likely blue day

### During Flight

**Entering cloud base**:
- You've reached the altitude where T = Td
- Expect thermal to strengthen (latent heat release)
- This is where -1°C/100m changes to -0.6°C/100m

**Flying between cumulus**:
- Air has been in thermals, reached cloud base, then sank
- Usually drier (water condensed out)
- May need to fly lower to find next working thermal

---

## Questions & Answers

### Q4: Par une température de 10 °C, une masse d'air a une humidité relative de 60 %. Comment cette dernière variera-t-elle si la température monte à 20 °C?
**English**: At a temperature of 10°C, an air mass has a relative humidity of 60%. How will it change if the temperature rises to 20°C?

A) elle augmentera de 50 %
B) **elle baissera** ✓
C) elle restera constante
D) elle augmentera de 60 %

**Réponse (FR)**: B) Elle baissera

**Answer (EN)**: B) It will decrease

**Explanation**: When temperature increases but the amount of water vapor stays the same, relative humidity **decreases**. Why? Because warm air can hold more water vapor, so the same amount of vapor represents a smaller percentage of the maximum capacity. This is why morning fog (100% RH) burns off as the day warms - the RH drops below 100% as temperature rises, even though the amount of water vapor hasn't changed.

---

### Q5.1: Deux masses d'air contiennent la même quantité de vapeur d'eau par unité de volume (même humidité absolue). M1 est plus chaude que M2. Laquelle des deux peut contenir le plus de vapeur d'eau?
**English**: Two air masses contain the same quantity of water vapor per unit volume (same absolute humidity). M1 is warmer than M2. Which one can contain more water vapor?

**Réponse (FR)**: M1 (la masse d'air plus chaude)

**Answer (EN)**: M1 (the warmer air mass)

**Explanation**: Warm air can hold significantly more water vapor than cold air. This is why:
- Tropical air can be very humid (warm = large capacity)
- Arctic air is usually dry (cold = small capacity)
- Rising air forms clouds (cooling = reduced capacity)

For glider pilots, this explains why:
- **Summer days** can have high cloud bases (warm air holds lots of vapor before saturating)
- **Spring/autumn days** often have lower cloud bases (cooler air saturates sooner)
- **Thermal tops** are where rising air has cooled enough to saturate

---

### Q5.2: Quels sont les paramètres utilisés pour caractériser l'humidité de l'air?
**English**: What are the parameters used to characterize air humidity?

**Réponse (FR)**:
- Humidité relative (en %)
- Quantité de vapeur d'eau par volume d'air sec (humidité absolue, en g/m³)
- Point de rosée (température en °C)

**Answer (EN)**:
- Relative humidity (in %)
- Quantity of water vapor per volume of dry air (absolute humidity, in g/m³)
- Dew point (temperature in °C)

**Explanation**: Each parameter tells us something different:
- **Relative humidity**: How close to saturation (useful for comfort, fog prediction)
- **Absolute humidity**: Actual amount of water vapor (useful for calculating energy in storms)
- **Dew point**: Temperature for saturation (**most useful for pilots - predicts cloud base!**)

As a glider pilot, **focus on dew point (Td)** - it directly tells you cloud base height!

---

### Q6: Qu'est-ce que le point de rosée?
**English**: What is the dew point?

**Réponse (FR)**: Le point de rosée est la température à laquelle il faut refroidir l'air pour atteindre la saturation (100% d'humidité relative), c'est-à-dire la formation des premières gouttelettes d'eau.

**Answer (EN)**: The dew point is the temperature to which air must be cooled to reach saturation (100% relative humidity), that is, the formation of the first water droplets.

**Explanation**: The dew point is your most valuable humidity parameter because:

1. **It predicts cloud base**: Cloud base ≈ [(T - Td) / 0.8] × 100 meters AGL
2. **It's stable**: Unlike RH, dew point doesn't change much as air heats during the day
3. **It indicates comfort**: High Td (>18°C) feels muggy, low Td (<5°C) feels dry

**Practical example**:
- Morning at 0800: T=15°C, Td=11°C → spread is 4°C
- Predicted cloud base: (4/0.8) × 100 = **500m AGL**
- Afternoon at 1400: T=25°C, Td=12°C → spread is 13°C
- New cloud base: (13/0.8) × 100 = **1625m AGL**

Notice the dew point barely changed (+1°C) but cloud base rose 1125m because surface temperature increased!

---

### Q7: Quels processus permettent d'atteindre la saturation?
**English**: What processes allow reaching saturation?

**Réponse (FR)**: Refroidissement ou un apport d'humidité (mélange entre 2 masses d'air). Deux types de refroidissement : à pression constante (isobare) ou par détente (lors de l'élévation de l'air).

**Answer (EN)**: Cooling or adding humidity (mixing between 2 air masses). Two types of cooling: at constant pressure (isobaric) or by expansion (when air rises).

**Explanation**:
- **Isobaric cooling** (pressure constant): Night cooling → fog, warm air over cold lake → fog
- **Cooling by expansion** (adiabatic): Rising thermals → cumulus clouds
- **Adding moisture**: Evaporation from wet surfaces, mixing air masses

For glider pilots, **adiabatic cooling is most important** - this creates the convective clouds we soar under!

---

## Abbreviations and Key Terms {#abbreviations}

**Humidity Terms**:
- **RH**: Relative Humidity - Percentage of water vapor relative to maximum capacity at current temperature
- **HR**: Humidité Relative (French for Relative Humidity)
- **Td**: Dew Point Temperature - Temperature at which air becomes saturated
- **T**: Temperature (ambient air temperature)
- **g/m³**: Grams per cubic meter - Unit for absolute humidity

**Cloud/Weather Abbreviations**:
- **Cu**: Cumulus clouds (fair weather puffy clouds)
- **METAR**: Meteorological Aerodrome Report - Current weather observation
- **TAF**: Terminal Aerodrome Forecast - Airport weather forecast
- **AGL**: Above Ground Level - Height measured from ground
- **MSL**: Mean Sea Level - Altitude measured from sea level

**Weather Observation Terms**:
- **Spread**: Difference between temperature and dew point (T - Td)
  - Small spread (< 3°C) = High humidity, low clouds
  - Large spread (> 15°C) = Dry air, high cloud base or blue day
- **Convergence**: How quickly T and Td approach each other as air rises
  - T drops ~1°C/100m
  - Td drops ~0.2°C/100m
  - They converge at ~0.8°C/100m

**Pressure Terms**:
- **Isobaric**: Constant pressure (no altitude change)
- **hPa**: Hectopascal - Unit of atmospheric pressure (1 hPa = 1 millibar)
  - Standard sea level: 1013.25 hPa
  - Pressure decreases ~1 hPa per 30 ft altitude gain

**Aviation Terms**:
- **VMC**: Visual Meteorological Conditions - Good visibility, VFR flight possible
- **IMC**: Instrument Meteorological Conditions - Poor visibility, IFR required
- **VFR**: Visual Flight Rules - Flying by visual reference
- **IFR**: Instrument Flight Rules - Flying by instruments in poor visibility

---

*Related topics*: [Phase Changes](01_phase_changes_latent_heat.md), [Adiabatic Processes](03_adiabatic_processes.md), [Convection](05_convection_thermals.md)
