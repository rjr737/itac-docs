---
hide:
  - toc
---

# Install Variable Frequency Drives

Variable frequency drives (VFDs) control motor speed by varying the electrical frequency supplied to the motor. For variable-torque loads such as fans, pumps, and blowers, power consumption scales with the cube of speed — cutting speed by 20% reduces power by nearly 50%. Most such equipment runs at full speed while throttling devices (dampers, valves) waste the excess energy; a VFD eliminates this by matching motor speed to actual demand.

**ARC Code(s):** 2.4121

## Savings Calculation

Savings depend on how much the motor speed can be reduced and for how long. The affinity laws govern centrifugal fans and pumps: flow is proportional to speed, and power is proportional to the cube of speed. For applications with a measurable average load fraction, a single-point estimate is appropriate. For applications with significant load variation, a bin analysis across multiple operating conditions is more accurate.

### Annual Energy Savings

For a single average operating condition, annual energy savings are:

$$
\Delta kWh = P_{\text{baseline}} \times \left(1 - \bar{f}^{\,3}\right) \times H
$$

- $\Delta kWh$ = annual energy savings (kWh/yr)

- $P_{\text{baseline}}$ = motor input power at full speed (kW)

- $\bar{f}$ = average speed fraction, equal to average flow fraction for centrifugal equipment (decimal)

- $H$ = annual operating hours (hrs/yr)

For applications with known hours at multiple load conditions, sum across all operating points:

$$
\Delta kWh = P_{\text{baseline}} \times \sum_{i}\left(1 - f_i^{\,3}\right) \times H_i
$$

- $f_i$ = speed fraction at operating condition $i$ (decimal)

- $H_i$ = annual hours at operating condition $i$ (hrs/yr)

??? note "Determining the average speed fraction"

    The average speed fraction equals the average flow fraction for centrifugal fans and pumps (Q ∝ N). Estimate it from production schedules, damper/valve position logs, or short-term power measurements. A common approach is to compare average measured power to full-speed nameplate power: $\bar{f} = \left(P_{\text{avg}} / P_{\text{baseline}}\right)^{1/3}$.

!!! note "Assumptions"

    - Equipment is a centrifugal fan, pump, or blower (affinity law exponent = 3)

    - Baseline operation is at or near full motor speed with throttling control

    - For positive-displacement equipment (screw compressors, etc.), the affinity law exponent differs — verify with manufacturer data

### Peak Demand Savings

$$
\Delta kW_{\text{summer}} = \Delta kW_{\text{winter}} = P_{\text{baseline}} \times \left(1 - \bar{f}^{\,3}\right)
$$

- $\Delta kW_{\text{summer}}$, $\Delta kW_{\text{winter}}$ = peak demand reduction (kW)

$$
\Delta kW\text{-months} = (\Delta kW_{\text{summer}} \times 3) + (\Delta kW_{\text{winter}} \times 9)
$$

- $\Delta kW\text{-months}$ = annual demand savings (kW-months)

!!! warning "Minimum Speed Constraints"

    Some equipment cannot operate below a minimum speed due to mechanical constraints, process requirements, or cooling needs. Verify minimum speed limits with equipment specifications before assuming full speed range is available. Savings calculations must be bounded by the actual achievable speed range.

## Anticipated Costs

**Equipment:** VFD costs scale with motor horsepower and voltage. Obtain quotes for the specific HP, voltage, and enclosure type required. Bypass contactors and input line reactors are often recommended as ancillary equipment.

**Installation:** Labor includes VFD mounting, conduit and wiring, programming, and commissioning. Budget 4–8 hours for motors under 25 HP; larger installations or those requiring panel modifications may require significantly more. Some installations also require harmonic filtering depending on facility power quality requirements.

Most utilities offer prescriptive rebates for VFD installations on qualifying fan and pump motors. Check with the local utility for current incentive offerings and verify eligibility before finalizing cost estimates.

Simple payback periods typically range from 1–3 years for equipment running more than 4,000 hours per year at partial load. Equipment running fewer hours or near full load most of the time will have longer payback periods.
