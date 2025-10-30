# The Physics Behind the Lapse Rate

The 6.5°C/km lapse rate emerges from the balance of several fundamental atmospheric processes:

**Where L = 6.5°C/km comes from**:

1. **[Dry adiabatic lapse rate](https://en.wikipedia.org/wiki/Lapse_rate#Dry_adiabatic_lapse_rate)**: Rising dry air expands and cools at 9.8°C/km due to decreasing pressure
2. **[Moist adiabatic lapse rate](https://en.wikipedia.org/wiki/Lapse_rate#Saturated_adiabatic_lapse_rate)**: Saturated air cools slower (~6°C/km) because condensation releases latent heat
3. **[Radiative cooling](https://en.wikipedia.org/wiki/Radiative_cooling)**: Atmosphere loses heat to space
4. **Convective mixing**: Turbulent mixing redistributes heat vertically

The **environmental lapse rate** of 6.5°C/km is the equilibrium value that emerges when these competing processes balance out in Earth's average atmosphere.

**Mathematical derivation**: Starting from hydrostatic equilibrium and the ideal gas law:
- $\frac{dP}{dh} = -\rho g$ (pressure decreases with altitude)  
- $P = \rho R T$ (ideal gas law)
- Combining with energy balance gives: $L = \frac{g}{c_p} \cdot \frac{\gamma - 1}{\gamma}$ ≈ 9.8°C/km (dry)

**Where these constants are**:
- **g** = [gravitational acceleration](https://en.wikipedia.org/wiki/Gravitational_acceleration) = 9.8 m/s² (force pulling air downward)
- **c_p** = [specific heat capacity at constant pressure](https://en.wikipedia.org/wiki/Heat_capacity) = 1005 J/(kg·K) for air (energy needed to heat 1kg of air by 1°C)
- **γ** = [heat capacity ratio](https://en.wikipedia.org/wiki/Heat_capacity_ratio) = 1.4 for air (ratio of heat capacities: γ = c_p/c_v)

**Plugging in the numbers**:

$L = \frac{9.8}{1005} \cdot \frac{1.4 - 1}{1.4} = \frac{9.8}{1005} \cdot \frac{0.4}{1.4} = 0.0098$ K/m = **9.8°C/km**

**Physical meaning**: 

- **g/c_p**: How much temperature drops per unit energy lost to expansion work
- **(γ-1)/γ**: Fraction of energy that goes into expansion work vs. internal energy
- **Result**: When air rises 1000m, it does expansion work against lower pressure, cooling by 9.8°C

**Why 9.8°C/km becomes 6.5°C/km in reality**:

The observed 6.5°C/km is reduced from the theoretical dry value due to average moisture effects and radiative processes.


**1. Moisture Effects (Latent Heat Release)**:
- **Pure dry air**: Cools at 9.8°C/km when rising
- **Moist air**: When rising air reaches [dewpoint](https://en.wikipedia.org/wiki/Dew_point), water vapor condenses
- **[Latent heat](https://en.wikipedia.org/wiki/Latent_heat)**: Condensation releases ~2260 kJ/kg of energy, warming the air
- **Result**: Saturated air cools at only ~6°C/km (moist adiabatic lapse rate)

**2. Radiative Cooling Effects**:
- **Heat loss to space**: Atmosphere continuously radiates heat to space
- **Greenhouse gases**: CO₂, H₂O absorb/emit infrared radiation
- **Net cooling**: This radiative cooling steepens the temperature profile slightly

**3. The Global Average**:
- **Sometimes dry**: Desert air approaches 9.8°C/km
- **Sometimes moist**: Tropical air closer to 6°C/km  
- **Radiative balance**: Space cooling vs. surface heating
- **Statistical result**: All these effects average to **6.5°C/km globally**

**The calculation**:
- ~30% of atmosphere has significant moisture → contributes ~6°C/km
- ~70% is relatively dry → contributes ~9.8°C/km
- Weighted average: (0.3 × 6) + (0.7 × 9.8) ≈ 8.7°C/km
- Radiative cooling reduces this further to ~6.5°C/km

**Bottom line**: 6.5°C/km is Earth's atmospheric equilibrium when you balance adiabatic cooling, latent heat effects, and radiative processes globally.

The **[barometric height formula](https://en.wikipedia.org/wiki/Barometric_formula)** then uses this empirically-derived L:

$P = P_0 \cdot \left(1 - \frac{L \cdot h}{T_0}\right)^{\frac{g \cdot M}{R \cdot L}}$

**Where the constants represent**:
- **P** = pressure at altitude h (Pa)
- **P₀** = [sea level standard pressure](https://en.wikipedia.org/wiki/Atmospheric_pressure) = 101,325 Pa (1013.25 hPa)
- **L** = [temperature lapse rate](https://en.wikipedia.org/wiki/Lapse_rate) = 0.0065 K/m (6.5°C/km)
- **h** = height above sea level (m)
- **T₀** = sea level standard temperature = 288.15 K (15°C)
- **g** = [standard gravity](https://en.wikipedia.org/wiki/Standard_gravity) = 9.80665 m/s²
- **M** = [molar mass of Earth's air](https://en.wikipedia.org/wiki/Molar_mass) = 0.0289644 kg/mol
- **R** = [universal gas constant](https://en.wikipedia.org/wiki/Gas_constant) = 8.31432 J/(mol·K)

This formula emerges from three fundamental principles:
- **[Hydrostatic equilibrium](https://en.wikipedia.org/wiki/Hydrostatic_equilibrium)**: Pressure decreases with altitude due to gravity
- **[Ideal gas law](https://en.wikipedia.org/wiki/Ideal_gas_law)**: Temperature, pressure, and density relationships
- **[Adiabatic processes](https://en.wikipedia.org/wiki/Adiabatic_process)**: Rising air expands and cools



---
<mark style="margin-top: 100; background-color: #3B3836; color: #494942">Created: `$=dv.span(dv.current().file.ctime)`</mark>