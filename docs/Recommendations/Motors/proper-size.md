---
hide:
  - toc
---

# Replace Oversized Motors with Properly-Sized Units

Oversized motors running at partial load operate at reduced efficiency and power factor, wasting electrical energy compared to properly-sized motors. When replacing failed motors or upgrading equipment, selecting motors sized appropriately for the actual load reduces both energy consumption and demand charges while improving power factor.

**ARC Code(s):** 2.4132

## Savings Calculation

Energy savings result from operating a motor closer to its optimal load point. Electric motors achieve peak efficiency between 75% and 100% of rated capacity. Motors operating below 50% of rated capacity suffer from reduced efficiency, poor power factor, and excessive magnetizing current that provides no useful work.

Actual load factor from current measurements:

$$
LF = \frac{I_{\text{actual}}}{I_{\text{FLA}}}
$$

- $LF$ = load factor (decimal)

- $I_{\text{actual}}$ = measured operating current (A)

- $I_{\text{FLA}}$ = nameplate full load amps (A)

Actual mechanical power output:

$$
P_{\text{shaft}} = HP_{\text{rated}} \times LF \times 0.746
$$

- $P_{\text{shaft}}$ = actual shaft power output (kW)

- $HP_{\text{rated}}$ = nameplate horsepower (HP)

- $LF$ = load factor (decimal)

- $0.746$ = unit conversion factor (kW/HP)

Motor input power at partial load:

$$
P_{\text{input,oversized}} = \frac{P_{\text{shaft}}}{\eta_{\text{oversized}}}
$$

- $P_{\text{input,oversized}}$ = electrical input power of the existing oversized motor (kW)

- $P_{\text{shaft}}$ = actual shaft power output (kW)

- $\eta_{\text{oversized}}$ = efficiency of the oversized motor at its actual load factor (decimal)

??? note "Obtaining part-load efficiency"

    $\eta_{\text{oversized}}$ must be obtained from the motor's performance curve, not the nameplate value. Nameplate efficiency is at full load; efficiency degrades significantly below 50% load. Performance curves are available from the motor manufacturer or from MotorMaster+.

Select a properly-sized motor targeting 75–90% load factor:

$$
HP_{\text{new}} = \frac{P_{\text{shaft}}}{0.746 \times 0.80}
$$

- $HP_{\text{new}}$ = recommended motor size (HP)

- $P_{\text{shaft}}$ = actual shaft power output (kW)

- $0.80$ = target load factor (decimal)

### Annual Energy Savings

$$
\Delta kWh = \left(P_{\text{input,oversized}} - P_{\text{input,new}}\right) \times H
$$

- $\Delta kWh$ = annual energy savings (kWh/yr)

- $P_{\text{input,oversized}}$ = electrical input power of the existing oversized motor (kW)

- $P_{\text{input,new}}$ = electrical input power of the properly-sized motor (kW)

- $H$ = annual operating hours (hrs/yr)

### Peak Demand Savings

$$
\Delta kW_{\text{summer}} = \Delta kW_{\text{winter}} = P_{\text{input,oversized}} - P_{\text{input,new}}
$$

- $\Delta kW_{\text{summer}}$, $\Delta kW_{\text{winter}}$ = peak demand reduction (kW)

$$
\Delta kW\text{-months} = (\Delta kW_{\text{summer}} \times 3) + (\Delta kW_{\text{winter}} \times 9)
$$

- $\Delta kW\text{-months}$ = annual demand savings (kW-months)

!!! warning "Starting Requirements"

    Some applications require high starting torque even if running loads are low. Compressors, loaded conveyors, and equipment with high inertia may need larger motors for starting duty even though running efficiency would favor a smaller motor. Verify starting requirements with equipment specifications before recommending downsizing.

## Anticipated Costs

Motor costs for properly-sized replacements follow the same pricing structure as [high efficiency motor upgrades](high-efficiency.md). Budget 2–4 hours of electrician labor for motors under 25 HP, plus additional time for mechanical modifications if required.

## Report Requirements

In addition to the [typical report requirements](../how-to.md) and the recommendation-specific savings and costs, the recommendation should include a table documenting all oversized motors recommended for replacement. The table should follow this structure:

- **Column 1:** Motor ID or equipment location

- **Column 2:** Current motor size (HP)

- **Column 3:** Measured load factor (%)

- **Column 4:** Recommended motor size (HP)

- **Column 5:** Annual operating hours (hrs/yr)

- **Column 6:** Annual energy savings (kWh/yr)

- **Column 7:** Annual demand savings (kW-months)

- **Column 8:** Annual cost savings ($/yr)

Include a totals row at the bottom for multiple motors.

```latex
\begin{table}[H]
\centering
\caption{Motor Right-Sizing Recommendations}
\label{tab:motor-sizing}
\begin{tabular}{lccccccc}
\toprule
Motor & Current & Measured & Recommended & Operating & Energy & Demand & Cost \\
Location & Size (HP) & Load (\%) & Size (HP) & Hours (hrs/yr) & Savings (kWh/yr) & Savings (kW-months) & Savings (\$/yr) \\
\midrule
Pump 1 &  &  &  &  &  &  &  \\
Fan 3 &  &  &  &  &  &  &  \\
Compressor 2 &  &  &  &  &  &  &  \\
\midrule
\textbf{Total} & \textbf{--} & \textbf{--} & \textbf{--} & \textbf{--} & \textbf{} & \textbf{} & \textbf{} \\
\bottomrule
\end{tabular}
\end{table}
```
