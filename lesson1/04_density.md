# Air Density (Densité de l'air)

**📖 Reference**: [Lesson 1 Slides - Density](slides/meteo1_part-01-50.pdf#page=9)

## Why This Matters for Glider Pilots

Air density is **THE** critical factor for aircraft performance:
- **Dense air = Better performance** - more lift, better climb rates
- **Thin air = Poor performance** - less lift, worse climb rates, longer takeoff
- Density changes with **altitude**, **temperature**, and **humidity**
- **Hot & high = dangerous combination** - low density affects safety
- Understanding [density altitude](https://en.wikipedia.org/wiki/Density_altitude) is essential for mountain flying
- Affects both wing performance and (for powered aircraft) engine performance

## What is Density?

**[Density](https://en.wikipedia.org/wiki/Density) (ρ)** is the mass per unit volume:

**ρ = m/V**

Where:
- ρ = density (kg/m³)
- m = mass (kg)
- V = volume (m³)

## Relationship with Pressure and Temperature

Air density follows the **[ideal gas law](https://en.wikipedia.org/wiki/Ideal_gas_law)**:

**ρ ∝ p/(RT)**

Where:
- p = pressure
- R = gas constant
- T = temperature (in Kelvin!)

### Key Relationships:

1. **Higher pressure → Higher density**
   - More air molecules compressed into same volume
   - Example: Sea level has higher density than mountaintop

2. **Higher temperature → Lower density**
   - Air molecules have more kinetic energy
   - They spread out more (thermal agitation - agitation thermique)
   - Same mass occupies larger volume
   - Example: Hot summer day has lower density than cold winter day

**What this means**: Pressure and temperature work together to determine density. That's why the worst performance happens on **hot days at high altitude airports** - low pressure AND high temperature both reduce density!

## States of Matter and Density

From **most dense to least dense**:

1. **[Solid](https://en.wikipedia.org/wiki/Solid) (Solide)**: Molecules tightly packed, vibrate in place
2. **[Liquid](https://en.wikipedia.org/wiki/Liquid) (Liquide)**: Molecules can move but stay close together
3. **[Gas](https://en.wikipedia.org/wiki/Gas) (Gaz)**: Molecules widely separated, move freely

As temperature increases, molecular agitation increases, and density decreases.

**What this means**: Air (a gas) is compressible - its density changes significantly with pressure and temperature. This is why you need to account for conditions when planning flights.

## Importance for Aviation

### Aircraft Performance
- **Higher density** = Better aircraft performance
  - More air molecules for wings to generate lift ([Bernoulli's principle](https://en.wikipedia.org/wiki/Bernoulli%27s_principle))
  - More air for propeller/engine thrust
  - Better glider performance - higher L/D ratio
  - Shorter takeoff distance

- **Lower density** = Reduced performance
  - Less lift generated (wings must fly faster to generate same lift!)
  - Longer takeoff distance required
  - Reduced climb rate
  - Higher stall speed

**What this means**: Your glider's stall speed increases in low-density conditions! The wings need to move faster through the air to generate the same lift force.

### Density Changes With:
- **Altitude**: Density decreases (pressure decreases)
  - ISA sea level: 1.225 kg/m³
  - At 3000m: ~0.9 kg/m³ (about 27% less!)
- **Temperature**: Hot day = lower density = worse performance
  - 15°C at sea level: 1.225 kg/m³
  - 30°C at sea level: ~1.16 kg/m³ (about 5% less)
- **Humidity**: More water vapor = slightly lower density (H₂O lighter than N₂ and O₂)
  - Humid air is actually LIGHTER than dry air (counter-intuitive!)

### Practical Example - Samedan Airport (1,707m elevation):
On a hot summer day (30°C):
- Low pressure (due to altitude)
- High temperature
- **Combined effect**: Density altitude might be 3000m+
- Longer takeoff roll (maybe 50% longer!)
- Reduced climb performance
- **Plan accordingly - use full runway, expect sluggish performance**

### Density Altitude
[Density altitude](https://en.wikipedia.org/wiki/Density_altitude) is the altitude at which the air density would occur in ISA standard conditions. It's a way to account for both pressure altitude and temperature.

**Rule of thumb**: For every 1°C above ISA, add ~120 ft (37m) to pressure altitude to get density altitude.

**Example**: At Bex (400m), on a 25°C day:
- ISA temperature at 400m: 15 - (0.65 × 4) = 12.4°C
- Actual - ISA: 25 - 12.4 = 12.6°C warmer
- Density altitude: 400m + (12.6 × 37m) ≈ 866m
- Performance will be as if you're at 866m on a standard day!

---

*Related topics*: [Pressure](03_pressure.md), [Temperature](02_temperature.md), [ISA Standard Atmosphere](05_isa_standard_atmosphere.md)
