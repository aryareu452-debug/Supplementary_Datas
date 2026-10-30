# Supplementary Mathematical Proofs & Numerical Derivations
### Project Jacket Analytical Framework

**Core Analytical Matrix & Performance Proofs**

---

## Abstract

This supplementary manuscript consolidates the core analytical proofs, thermodynamic boundary conditions, and numerical modeling matrices supporting the multi-carrier harvesting architecture of Project Jacket[cite: 4]. By synthesizing electrostatic barrier tuning, near-field radiative flux coupling, sub-micron gap sensitivity, and thermal back-emission limits, this document provides the quantitative framework necessary to evaluate both Far-Field and Near-Field operational regimes[cite: 4, 6]. Crucially, while Near-Field Radiative Heat Transfer (NFRHT) yields theoretical power density enhancements of $55.15\times$ over Far-Field baselines[cite: 7], this document establishes the governing thermodynamic source-input requirements and core-quenching boundaries that dictate when Far-Field versus Near-Field harvesting must be deployed[cite: 6].

---

## 1. Electrostatic Barrier Engineering & Work Function Optimization

This section establishes the thermodynamic and electrical performance across three distinct design configurations for a thermionic energy harvesting system operating at extreme temperatures[cite: 4]. It demonstrates why maintaining a low anode work function ($\phi_{\text{anode}}$) combined with active Schottky grid biasing ($\Delta\phi$) is mandatory to bypass space-charge bottlenecks[cite: 4].

### 1.1 Baseline Parameters & Fundamental Quantities

* **Hot Emitter (Cathode) Temperature ($T_H$):** $2000\text{ K}$ ($\approx 1727^\circ\text{C}$)[cite: 4]
* **Cold Collector (Anode) Temperature ($T_C$):** $600\text{ K}$ ($\approx 327^\circ\text{C}$)[cite: 4]
* **Richardson's Constant ($A_R$):** $120.4\text{ A}/(\text{cm}^2 \cdot \text{K}^2)$[cite: 4]
* **Unbiased Cathode Work Function ($\phi_{\text{cathode}}$):** $3.00\text{ eV}$ (Refractory ceramic/metal matrix)[cite: 4]

**Thermal Energy Equivalent Voltage ($V_{\text{th}}$):**
$$V_{\text{th}} = \frac{k_B T_H}{e} = (8.61733 \times 10^{-5}\text{ eV/K}) \times 2000\text{ K} = \mathbf{0.17235\text{ eV}}$$[cite: 4]

### 1.2 Step-by-Step Case Calculations

#### Case 1: High Anode Work Function ($\phi_{\text{anode}} = 2.80\text{ eV}$) & No Active Bias[cite: 4]

Built-in Extraction Voltage:
$$V_{\text{ext}} = \frac{\phi_{\text{cathode}} - \phi_{\text{anode}}}{e} = \frac{3.00\text{ eV} - 2.80\text{ eV}}{e} = \mathbf{0.20\text{ V}}$$[cite: 4]

Thermionic Current Density ($J_{\text{th}}$):
$$J_{\text{th}} = A_R T_H^2 \exp\left(-\frac{\phi_{\text{cathode}}}{V_{\text{th}}}\right) = 120.4 \times (2000)^2 \times \exp\left(-\frac{3.00}{0.17235}\right) = \mathbf{13.27\text{ A/cm}^2}$$[cite: 4]

Harvested Electrical Power Density ($P_{\text{elec}}$):
$$P_{\text{elec}} = J_{\text{th}} \times V_{\text{ext}} = 13.27\text{ A/cm}^2 \times 0.20\text{ V} = \mathbf{2.65\text{ W/cm}^2}$$[cite: 5]

#### Case 2: Low Anode Work Function ($\phi_{\text{anode}} = 1.50\text{ eV}$) & No Active Bias[cite: 5]

Built-in Extraction Voltage:
$$V_{\text{ext}} = \frac{3.00\text{ eV} - 1.50\text{ eV}}{e} = \mathbf{1.50\text{ V}}$$[cite: 5]

Thermionic Current Density ($J_{\text{th}}$):
$$J_{\text{th}} = \mathbf{13.27\text{ A/cm}^2} \quad (\text{Unchanged without active barrier lowering})$$[cite: 5]

Harvested Electrical Power Density ($P_{\text{elec}}$):
$$P_{\text{elec}} = 13.27\text{ A/cm}^2 \times 1.50\text{ V} = \mathbf{19.91\text{ W/cm}^2} \quad \mathbf{(7.50\times\text{ gain over Case 1})}$$[cite: 5]

#### Case 3: Low Anode Work Function ($1.50\text{ eV}$) + Active Extraction Bias ($0.30\text{ eV}$ Grid)[cite: 5]

Effective Cathode Barrier (Schottky Lowered):
$$\phi_{\text{eff}} = 3.00\text{ eV} - 0.30\text{ eV} = \mathbf{2.70\text{ eV}}$$[cite: 5]

Total Extraction Voltage:
$$V_{\text{ext}} = 1.50\text{ V} + 0.30\text{ V} = \mathbf{1.80\text{ V}}$$[cite: 5]

Accelerated Thermionic Current Density ($J_{\text{th, active}}$):
$$J_{\text{th, active}} = 120.4 \times (2000)^2 \times \exp\left(-\frac{2.70}{0.17235}\right) = \mathbf{75.68\text{ A/cm}^2} \quad \mathbf{(5.70\times\text{ current jump})}$$[cite: 5]

Extracted Power Density ($P_{\text{elec, active}}$):
$$P_{\text{elec, active}} = 75.68\text{ A/cm}^2 \times 1.80\text{ V} = \mathbf{136.23\text{ W/cm}^2} \quad \mathbf{(51.31\times\text{ gain over Case 1})}$$[cite: 5]

### 1.3 Case Comparative Matrix

| Parameter | Case 1: High $\phi_{\text{anode}}$ (No Bias) | Case 2: Low $\phi_{\text{anode}}$ (No Bias) | Case 3: Low $\phi_{\text{anode}}$ (+ Active Bias) | Physical Significance |
| :--- | :---: | :---: | :---: | :--- |
| **Emitter Barrier ($\phi_{\text{eff}}$)** | $3.00\text{ eV}$[cite: 5] | $3.00\text{ eV}$[cite: 5] | $2.70\text{ eV}$[cite: 5] | Active field barrier lowering[cite: 5] |
| **Output Voltage ($V_{\text{ext}}$)** | $0.20\text{ V}$[cite: 5] | $1.50\text{ V}$[cite: 5] | $1.80\text{ V}$[cite: 5] | Maximized voltage capture[cite: 5] |
| **Current Density ($J_{\text{th}}$)** | $13.27\text{ A/cm}^2$[cite: 5] | $13.27\text{ A/cm}^2$[cite: 5] | $75.68\text{ A/cm}^2$[cite: 5] | $5.70\times$ current jump (space charge cleared)[cite: 5] |
| **Power Density ($P_{\text{elec}}$)** | $2.65\text{ W/cm}^2$[cite: 5] | $19.91\text{ W/cm}^2$[cite: 5] | $136.23\text{ W/cm}^2$[cite: 5] | $51.31\times$ total power increase over Case 1[cite: 5] |

* **Why Low Anode Work Function is Necessary ($\text{Case 1} \to \text{Case 2}$):** Dropping $\phi_{\text{anode}}$ from $2.80\text{ eV}$ to $1.50\text{ eV}$ expands the built-in potential difference from $0.20\text{ V}$ to $1.50\text{ V}$, increasing power harvest by $7.50\times$ without requiring additional thermal input[cite: 5].
* **Why Active Bias is Necessary ($\text{Case 2} \to \text{Case 3}$):** A low anode work function alone cannot clear space-charge buildup in narrow gaps[cite: 5]. Applying active bias sweeps away negative electron clouds, boosting current density and unlocking an additional $6.84\times$ power gain[cite: 5].

---

## 2. Mathematical Proof — Near-Field Photon Tunneling vs. Far-Field Harvesting & Regime Applicability

This section presents a quantitative comparative proof between the sub-wavelength Near-Field Regime ($d \ll \lambda_c$) and the conventional Far-Field Regime ($d \gg \lambda_c$)[cite: 6]. While Near-Field operation achieves ultra-high power extraction densities, it imposes a corresponding thermal load on the source that limits its deployment to active heat-sink applications or compensated energy systems[cite: 6].

### 2.1 Governing Equations & Calibration Constants

Far-Field Power Density:
$$P_{\text{elec, far}} = \psi \left[ \eta_\gamma \cdot \eta_{\text{spec}} \cdot \sigma T_H^4 + \eta_e \cdot (J_{\text{th}} \cdot V_{\text{ext}}) \right]$$[cite: 6]

Near-Field Power Density:
$$P_{\text{elec, near}} = \psi \left[ \eta_\gamma \cdot \eta_{\text{spec}} \cdot h(d) \cdot \sigma T_H^4 + \eta_e \cdot (J_{\text{th}} \cdot V_{\text{ext}}) \right]$$[cite: 6]

* **Hot Surface Temp ($T_H$):** $1956\text{ K}$ ($\approx 1683^\circ\text{C}$)[cite: 6]
* **Stefan-Boltzmann Constant ($\sigma$):** $5.67037 \times 10^{-12}\text{ W/(cm}^2\cdot\text{K}^4)$[cite: 6]
* **Active Fill Factor ($\psi$):** $0.85$ (Accounts for structural flexures and active grid coverage)[cite: 6]
* **Photonic Efficiency ($\eta_\gamma$):** $0.40$[cite: 6] | **Spectral Matching ($\eta_{\text{spec}}$):** $0.80$[cite: 6]
* **Electron Collection Efficiency ($\eta_e$):** $0.88$[cite: 6]
* **Active Thermionic Current ($J_{\text{th}}$):** $50.89\text{ A/cm}^2$ at $T_H = 1956\text{ K}$ ($\phi_{\text{eff}} = 2.70\text{ eV}$)[cite: 6]
* **Extraction Potential ($V_{\text{ext}}$):** $1.80\text{ V}$[cite: 6]

### 2.2 Peak Thermal Wavelength ($\lambda_c$) & Spatial Factor ($h(d)$)

By Wien's Displacement Law, the peak wavelength at $T_H = 1956\text{ K}$ is:
$$\lambda_c = \frac{2897.77\text{ }\mu\text{m}\cdot\text{K}}{1956\text{ K}} = 1.4815\text{ }\mu\text{m} = \mathbf{1481.5\text{ nm}}$$[cite: 6]

* **Far-Field Regime ($d = 1.0\text{ cm} = 10^7\text{ nm}$):** $d \gg \lambda_c \implies h(d) \equiv \mathbf{1.00}$[cite: 6]
* **Near-Field Regime ($d = 100\text{ nm}$):** $d \ll \lambda_c \implies$ Evanescent photon modes tunnel across the gap:
$$h(d=100\text{ nm}) \approx \left( \frac{\lambda_c}{d} \right)^2 = \left( \frac{1481.5\text{ nm}}{100\text{ nm}} \right)^2 = (14.815)^2 \approx \mathbf{219.48}$$[cite: 6]

### 2.3 Numerical Derivation Steps

Blackbody Baseline Radiation:
$$\sigma T_H^4 = (5.67037 \times 10^{-12}) \times (1956)^4 = \mathbf{83.00\text{ W/cm}^2}$$[cite: 6]

Thermionic Contribution:
$$P_{\text{thermionic}} = \eta_e \cdot (J_{\text{th}} \cdot V_{\text{ext}}) = 0.88 \times (50.89\text{ A/cm}^2 \times 1.80\text{ V}) = \mathbf{80.61\text{ W/cm}^2}$$[cite: 6]

Far-Field Total Electrical Power Output ($d = 1\text{ cm}$):
$$P_{\text{rad, far}} = 0.40 \times 0.80 \times 1.0 \times 83.00\text{ W/cm}^2 = \mathbf{26.56\text{ W/cm}^2}$$[cite: 6]
$$P_{\text{elec, far}} = 0.85 \times \left[ 26.56 + 80.61 \right] = 0.85 \times 107.17\text{ W/cm}^2 = \mathbf{91.09\text{ W/cm}^2} \quad (\approx \mathbf{9.11 \times 10^5\text{ W/m}^2})$$[cite: 7]

Near-Field Total Electrical Power Output ($d = 100\text{ nm}$):
$$P_{\text{rad, near}} = 0.40 \times 0.80 \times 219.48 \times 83.00\text{ W/cm}^2 = \mathbf{5830.05\text{ W/cm}^2}$$[cite: 7]
$$P_{\text{elec, near}} = 0.85 \times \left[ 5830.05 + 80.61 \right] = 0.85 \times 5910.66\text{ W/cm}^2 = \mathbf{5024.06\text{ W/cm}^2} \quad (\approx \mathbf{5.02 \times 10^7\text{ W/m}^2})$$[cite: 7]

### 2.4 Regime Comparison & Operational Trade-offs

| Performance Parameter | Far-Field Regime ($d=1\text{ cm}$) | Near-Field Regime ($d=100\text{ nm}$) | Physical Impact & Thermodynamic Trade-off |
| :--- | :---: | :---: | :--- |
| **Gap Ratio ($d / \lambda_c$)** | $d \approx 6750 \times \lambda_c$[cite: 7] | $d \approx 0.067 \times \lambda_c$[cite: 7] | Sub-wavelength threshold unlocked in Near-Field[cite: 7]. |
| **Spatial Factor $h(d)$** | $1.00$[cite: 7] | $219.48$[cite: 7] | Photon tunneling via evanescent fields[cite: 7]. |
| **Radiative Power ($P_{\text{rad}}$)** | $26.56\text{ W/cm}^2$[cite: 7] | $5830.05\text{ W/cm}^2$[cite: 7] | $219.48\times$ radiative density jump[cite: 7]. |
| **Thermionic Power ($P_{\text{therm}}$)** | $80.61\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | Baseline electronic current harvest[cite: 7]. |
| **Total Power Density ($P_{\text{elec}}$)** | $91.09\text{ W/cm}^2$[cite: 7] | $5024.06\text{ W/cm}^2$[cite: 7] | $55.15\times$ overall power harvesting gain[cite: 7]. |
| **Source Cooling Impact** | Low / Gentle ($\sim 10^2\text{ W/cm}^2$)[cite: 7] | Extreme ($\sim 10^4\text{ W/cm}^2$ thermal drain)[cite: 7] | **Near-Field requires matching thermal input ($\Delta E \ge q_{\text{rad}}$) to avoid rapid source thermal collapse (quenching).**[cite: 7] |
| **Mechanical Viability** | High (1 cm gap)[cite: 7] | Low / Extreme (100 nm gap)[cite: 7] | Far-Field bypasses mechanical gap shorting and vibration risks in aerospace/fusion environments[cite: 7]. |

---

## 3. Sub-Micron Gap Sensitivity, Thermal Quenching Risk & Spatial Scaling

While collapsing the vacuum gap $d$ unlocks exponential scaling via evanescent photon modes[cite: 7], it introduces severe engineering and thermodynamic constraints:

$$P_{\text{elec}}(d) = \psi \left[ \eta_\gamma \cdot \eta_{\text{spec}} \cdot \left(\frac{\lambda_c}{d}\right)^2 \cdot \sigma T_H^4 + \eta_e \cdot (J_{\text{th}} \cdot V_{\text{ext}}) \right]$$[cite: 7]

### 3.1 Numerical Scaling Matrix ($T_H = 1956\text{ K}$, $\lambda_c = 1481.5\text{ nm}$)

| Vacuum Gap ($d$) | Spatial Factor $h(d)$ | Photonic Power ($P_{\text{rad}}$) | Thermionic Power ($P_{\text{therm}}$) | Net Power Density ($P_{\text{elec}}$) | Power Gain vs. $500\text{ nm}$ | Core Thermal Quenching Risk |
| :---: | :---: | :---: | :---: | :---: | :---: | :--- |
| **$500\text{ nm}$** | $8.78$[cite: 7] | $233.18\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $266.72\text{ W/cm}^2$[cite: 7] | $1.00\times$ (Baseline)[cite: 7] | Low (Manageable thermal drain)[cite: 7] |
| **$200\text{ nm}$** | $54.87$[cite: 7] | $1,457.36\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $1,307.27\text{ W/cm}^2$[cite: 7] | $4.90\times$[cite: 7] | Moderate[cite: 7] |
| **$100\text{ nm}$** | $219.48$[cite: 7] | $5,829.45\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $5,023.54\text{ W/cm}^2$[cite: 7] | $18.83\times$[cite: 7] | **High** (Requires active power compensation)[cite: 7] |
| **$50\text{ nm}$** | $877.91$[cite: 7] | $23,317.78\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $19,888.63\text{ W/cm}^2$[cite: 7] | $74.57\times$[cite: 7] | **Extreme** (Immediate thermal collapse if uncompensated)[cite: 7] |
| **$20\text{ nm}$** | $5486.94$[cite: 7] | $145,736.14\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $123,944.23\text{ W/cm}^2$[cite: 7] | $464.69\times$[cite: 7] | **Catastrophic** (Unusable on sensitive core boundaries)[cite: 7] |

### 3.2 Thermodynamic Source-Balance Rule
To maintain steady-state emitter temperature $T_H = 2000\text{ K}$, the source energy input rate $E_{\text{in}}$ must equal total thermal dissipation:
$$E_{\text{in}} = q_{\text{rad}}(d) + q_{\text{far}} + q_{\text{other}}$$

In uncompensated or sensitive operational nodes (e.g., Tokamak divertor plasmas, hypersonic vehicle leading edges, nuclear thermal propulsion cores, or crystal growth crucibles), deploying a $d \le 100\text{ nm}$ gap without matching $E_{\text{in}}$ causes a sharp thermal energy deficit ($\Delta E < 0$), resulting in rapid thermal quenching ($T_H < 2000\text{ K}$) and system breakdown[cite: 7].

---

## 4. Collector Thermal Threshold & Back-Emission Current Breakdown ($T_C$-Dependence)

This section proves why active liquid-cooling of the collector bus (Layer $L_4$) is required to prevent thermal back-emission from eroding net extracted current[cite: 7].

$$J_{\text{net}} = J_{\text{forward}}(T_H, \phi_E) - J_{\text{back}}(T_C, \phi_C)$$[cite: 7]
$$J_{\text{back}} = A_R T_C^2 \exp\left(-\frac{\phi_C}{k_B T_C}\right)$$[cite: 7]

### Breakdown Across Collector Temperatures ($T_H = 1956\text{ K}$, $\phi_C = 1.50\text{ eV}$)

| Collector Temp ($T_C$) | Forward Current ($J_{\text{forward}}$) | Back-Emission ($J_{\text{back}}$) | Net Current ($J_{\text{net}}$) | Thermal Efficiency Loss |
| :---: | :---: | :---: | :---: | :--- |
| **$400\text{ K}$ ($127^\circ\text{C}$)** | $50.888\text{ A/cm}^2$ | $2.43 \times 10^{-12}\text{ A/cm}^2$ | $50.888\text{ A/cm}^2$ | $0.00\%$ (Ideal) |
| **$600\text{ K}$ ($327^\circ\text{C}$)** | $50.888\text{ A/cm}^2$ | $1.09 \times 10^{-5}\text{ A/cm}^2$ | $50.888\text{ A/cm}^2$ | $0.00\%$ (Optimal Sink) |
| **$800\text{ K}$ ($527^\circ\text{C}$)** | $50.888\text{ A/cm}^2$ | $0.027\text{ A/cm}^2$ | $50.861\text{ A/cm}^2$ | $0.05\%$ (Acceptable) |
| **$1000\text{ K}$ ($727^\circ\text{C}$)** | $50.888\text{ A/cm}^2$ | $3.319\text{ A/cm}^2$ | $47.569\text{ A/cm}^2$ | $6.52\%$ (Choked / Critical) |

---

## 5. Integrated System Performance Conclusions

1. **Work Function & Bias Optimization:** Reducing $\phi_{\text{anode}}$ to $1.50\text{ eV}$ expands output voltage to $1.50\text{ V}$ ($7.50\times$ power gain). Adding a $0.30\text{ eV}$ active bias clears space charge, providing an overall $51.31\times$ performance jump ($136.23\text{ W/cm}^2$).
2. **Operational Regime Selection:** 
   * **Far-Field Harvesting ($d \gg \lambda_c$):** Delivers $\approx 91.09\text{ W/cm}^2$ ($\approx 9.11 \times 10^5\text{ W/m}^2$)[cite: 7]. It represents the **only mechanically and thermally viable choice** for magnetic confinement fusion divertors, hypersonic flight surfaces, deep-space nuclear cores, and semiconductor crystal growth furnaces where core thermal quenching or sub-micron mechanical instability would cause catastrophic failure[cite: 7].
   * **Near-Field Harvesting ($d = 100\text{ nm} < \lambda_c$):** Yields up to $5024.06\text{ W/cm}^2$ ($\approx 5.02 \times 10^7\text{ W/m}^2$)[cite: 7]. However, it operates as an aggressive heat sink and is strictly restricted to controlled systems equipped with matching active power compensation ($\Delta E \ge q_{\text{rad}}$) to maintain thermal equilibrium[cite: 7].
3. **Sub-Micron Sensitivity & Thermal Back-Emission Limits:** Collapsing the gap to $50\text{ nm}$ yields $19,888.63\text{ W/cm}^2$, but increases core quenching risk proportionally[cite: 7]. Active cooling must maintain $T_C \le 800\text{ K}$ to restrict thermionic back-emission current losses to $< 0.05\%$.
