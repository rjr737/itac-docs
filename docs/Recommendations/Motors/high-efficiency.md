---
hide:
  - toc
---

# Upgrade to High Efficiency Motors

Standard efficiency motors waste significant energy as heat during operation. Upgrading to NEMA Premium high efficiency motors reduces electrical consumption, particularly in motors that run continuously or for long hours on constant loads like pumps, fans, and compressors.

**ARC Code(s):** 2.4133

## Savings Calculation

Energy savings result from reduced electrical losses in the windings, magnetic core, and mechanical components. The calculation compares electrical input power required by the existing motor versus a NEMA Premium motor delivering the same mechanical output.

Motor shaft power from nameplate horsepower:

$$
P_{\text{shaft}} = HP \times 0.746
$$

- $P_{\text{shaft}}$ = rated mechanical power output (kW)

- $HP$ = motor nameplate horsepower (HP)

- $0.746$ = unit conversion factor (kW/HP)

### Annual Energy Savings

$$
\Delta kWh = P_{\text{shaft}} \times \left(\frac{1}{\eta_{\text{baseline}}} - \frac{1}{\eta_{\text{premium}}}\right) \times H
$$

- $\Delta kWh$ = annual energy savings (kWh/yr)

- $P_{\text{shaft}}$ = motor shaft power output (kW)

- $\eta_{\text{baseline}}$ = existing motor efficiency (decimal)

- $\eta_{\text{premium}}$ = NEMA Premium motor efficiency (decimal)

- $H$ = annual operating hours (hrs/yr)

!!! note "Assumptions"

    - Motor operates at or near its rated capacity (load factor >75%)

    - Operating hours should be measured or estimated based on production schedules

    - Baseline efficiency should be obtained from motor nameplate or manufacturer data

    - NEMA Premium efficiency values can be found in NEMA MG-1 Table 12-12 or manufacturer specifications

    - For older motors (>15 years), consider additional degradation: reduce nameplate efficiency by 1% per year of operation

### Peak Demand Savings

$$
\Delta kW_{\text{summer}} = \Delta kW_{\text{winter}} = P_{\text{shaft}} \times \left(\frac{1}{\eta_{\text{baseline}}} - \frac{1}{\eta_{\text{premium}}}\right)
$$

- $\Delta kW_{\text{summer}}$, $\Delta kW_{\text{winter}}$ = peak demand reduction (kW)

$$
\Delta kW\text{-months} = (\Delta kW_{\text{summer}} \times 3) + (\Delta kW_{\text{winter}} \times 9)
$$

- $\Delta kW\text{-months}$ = annual demand savings (kW-months)

!!! warning "Load Factor Verification"

    High efficiency motor upgrades only make economic sense when motors run at high load factors (>75% of rated capacity) for significant hours per year. Motors running at low load factors (<50%) should first be evaluated for right-sizing rather than efficiency upgrades. Verify actual operating current against nameplate full load amps before recommending this measure.

## Anticipated Costs

**Equipment:** NEMA Premium motor costs vary with horsepower rating and enclosure type (ODP vs TEFC). Prices depend on vendor, voltage, speed, and mounting configuration. Obtain quotes from local suppliers for project-specific pricing.

**Installation:** Labor includes motor removal, new motor installation, alignment (for direct-coupled applications), and electrical connections. For belt-driven applications, add sheave installation and belt tensioning. Budget 2–4 hours of electrician labor for motors under 25 HP, 4–8 hours for larger motors; add additional time if rigging equipment is required.

Most utility energy efficiency programs offer prescriptive rebates for qualifying motor replacements, including early retirement incentives (replace a working motor before failure) and replace-on-burnout incentives (replace a failed motor with a high efficiency model). Check with the local utility for current offerings and verify eligibility before finalizing cost estimates.

Simple payback periods typically range from 2–5 years for early retirement applications and under 2 years for replace-on-burnout scenarios after utility incentives. Motors running more than 4,000 hours per year generally show better economics than those with intermittent operation.

## Report Requirements

In addition to the [typical report requirements](../how-to.md) and the recommendation-specific savings and costs, the recommendation should include a table documenting all motors being replaced. The table should follow this structure:

- **Column 1:** Motor ID or location description

- **Column 2:** Rated horsepower (HP)

- **Column 3:** Baseline efficiency (%)

- **Column 4:** Premium efficiency (%)

- **Column 5:** Annual operating hours (hrs/yr)

- **Column 6:** Annual energy savings (kWh/yr)

- **Column 7:** Annual demand savings (kW-months)

- **Column 8:** Annual cost savings ($/yr)

If multiple motors are being replaced, include a totals row at the bottom.

```latex
\begin{table}[H]
\centering
\caption{High Efficiency Motor Upgrade Summary}
\label{tab:high-eff-motors}
\begin{tabular}{lccccccc}
\toprule
Motor Location & HP & Baseline Eff. (\%) & Premium Eff. (\%) & Operating Hours & Energy Savings & Demand Savings & Cost Savings \\
 & & & & (hrs/yr) & (kWh/yr) & (kW-months) & (\$/yr) \\
\midrule
Pump 1 &  &  &  &  &  &  &  \\
Fan 3 &  &  &  &  &  &  &  \\
Compressor 2 &  &  &  &  &  &  &  \\
\midrule
\textbf{Total} & \textbf{} & \textbf{--} & \textbf{--} & \textbf{--} & \textbf{} & \textbf{} & \textbf{} \\
\bottomrule
\end{tabular}
\end{table}
```
