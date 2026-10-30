# Mathematical Data Points & Numerical Matrices
### Project Jacket Analytical Framework

## 1. Electrostatic Barrier Engineering & Work Function Optimization

* **Hot Emitter (Cathode) Temperature ($T_H$):** $2000\text{ K}$ ($\approx 1727^\circ\text{C}$)[cite: 4]
* **Cold Collector (Anode) Temperature ($T_C$):** $600\text{ K}$ ($\approx 327^\circ\text{C}$)[cite: 4]
* **Richardson's Constant ($A_R$):** $120.4\text{ A}/(\text{cm}^2 \cdot \text{K}^2)$[cite: 4]
* **Unbiased Cathode Work Function ($\phi_{\text{cathode}}$):** $3.00\text{ eV}$[cite: 4]
* **Thermal Energy Equivalent Voltage ($V_{\text{th}}$):** $0.17235\text{ eV}$[cite: 4]

### 1.1 Step-by-Step Case Calculations

* **Case 1 ($\phi_{\text{anode}} = 2.80\text{ eV}$, No Active Bias):**[cite: 4]
  * $V_{\text{ext}} = 0.20\text{ V}$[cite: 4]
  * $J_{\text{th}} = 13.27\text{ A/cm}^2$[cite: 4]
  * $P_{\text{elec}} = 2.65\text{ W/cm}^2$[cite: 5]
* **Case 2 ($\phi_{\text{anode}} = 1.50\text{ eV}$, No Active Bias):**[cite: 5]
  * $V_{\text{ext}} = 1.50\text{ V}$[cite: 5]
  * $J_{\text{th}} = 13.27\text{ A/cm}^2$[cite: 5]
  * $P_{\text{elec}} = 19.91\text{ W/cm}^2$[cite: 5]
* **Case 3 ($\phi_{\text{anode}} = 1.50\text{ eV}$ + $0.30\text{ eV}$ Active Bias):**[cite: 5]
  * $\phi_{\text{eff}} = 2.70\text{ eV}$[cite: 5]
  * $V_{\text{ext}} = 1.80\text{ V}$[cite: 5]
  * $J_{\text{th, active}} = 75.68\text{ A/cm}^2$[cite: 5]
  * $P_{\text{elec, active}} = 136.23\text{ W/cm}^2$[cite: 5]

### 1.2 Case Comparative Matrix

| Parameter | Case 1: High $\phi_{\text{anode}}$ (No Bias) | Case 2: Low $\phi_{\text{anode}}$ (No Bias) | Case 3: Low $\phi_{\text{anode}}$ (+ Active Bias) |
| :--- | :---: | :---: | :---: |
| **Emitter Barrier ($\phi_{\text{eff}}$)** | $3.00\text{ eV}$[cite: 5] | $3.00\text{ eV}$[cite: 5] | $2.70\text{ eV}$[cite: 5] |
| **Output Voltage ($V_{\text{ext}}$)** | $0.20\text{ V}$[cite: 5] | $1.50\text{ V}$[cite: 5] | $1.80\text{ V}$[cite: 5] |
| **Current Density ($J_{\text{th}}$)** | $13.27\text{ A/cm}^2$[cite: 5] | $13.27\text{ A/cm}^2$[cite: 5] | $75.68\text{ A/cm}^2$[cite: 5] |
| **Power Density ($P_{\text{elec}}$)** | $2.65\text{ W/cm}^2$[cite: 5] | $19.91\text{ W/cm}^2$[cite: 5] | $136.23\text{ W/cm}^2$[cite: 5] |

---

## 2. Near-Field vs. Far-Field Harvesting Data Points

### 2.1 Constants & Parameters
* **Hot Surface Temp ($T_H$):** $1956\text{ K}$[cite: 6]
* **Stefan-Boltzmann Constant ($\sigma$):** $5.67037 \times 10^{-12}\text{ W/(cm}^2\cdot\text{K}^4)$[cite: 6]
* **Active Fill Factor ($\psi$):** $0.85$[cite: 6]
* **Photonic Efficiency ($\eta_\gamma$):** $0.40$[cite: 6]
* **Spectral Matching ($\eta_{\text{spec}}$):** $0.80$[cite: 6]
* **Electron Collection Efficiency ($\eta_e$):** $0.88$[cite: 6]
* **Active Thermionic Current ($J_{\text{th}}$):** $50.89\text{ A/cm}^2$[cite: 6]
* **Extraction Potential ($V_{\text{ext}}$):** $1.80\text{ V}$[cite: 6]
* **Peak Thermal Wavelength ($\lambda_c$):** $1481.5\text{ nm}$ ($1.4815\text{ }\mu\text{m}$)[cite: 6]
* **Blackbody Baseline Radiation ($\sigma T_H^4$):** $83.00\text{ W/cm}^2$[cite: 6]
* **Thermionic Contribution ($P_{\text{thermionic}}$):** $80.61\text{ W/cm}^2$[cite: 6]

### 2.2 Regime Comparison Table

| Performance Parameter | Far-Field Regime ($d=1\text{ cm}$) | Near-Field Regime ($d=100\text{ nm}$) |
| :--- | :---: | :---: |
| **Gap Ratio ($d / \lambda_c$)** | $6750 \times \lambda_c$[cite: 7] | $0.067 \times \lambda_c$[cite: 7] |
| **Spatial Factor ($h(d)$)** | $1.00$[cite: 7] | $219.48$[cite: 7] |
| **Radiative Power ($P_{\text{rad}}$)** | $26.56\text{ W/cm}^2$[cite: 7] | $5830.05\text{ W/cm}^2$[cite: 7] |
| **Thermionic Power ($P_{\text{therm}}$)** | $80.61\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] |
| **Total Electrical Power ($P_{\text{elec}}$)** | $91.09\text{ W/cm}^2$ ($\approx 9.11 \times 10^5\text{ W/m}^2$)[cite: 7] | $5024.06\text{ W/cm}^2$ ($\approx 5.02 \times 10^7\text{ W/m}^2$)[cite: 7] |

---

## 3. Sub-Micron Gap Numerical Scaling Matrix ($T_H = 1956\text{ K}$)

| Vacuum Gap ($d$) | Spatial Factor ($h(d)$) | Photonic Power ($P_{\text{rad}}$) | Thermionic Power ($P_{\text{therm}}$) | Net Power Density ($P_{\text{elec}}$) |
| :---: | :---: | :---: | :---: | :---: |
| **$500\text{ nm}$** | $8.78$[cite: 7] | $233.18\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $266.72\text{ W/cm}^2$[cite: 7] |
| **$200\text{ nm}$** | $54.87$[cite: 7] | $1,457.36\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $1,307.27\text{ W/cm}^2$[cite: 7] |
| **$100\text{ nm}$** | $219.48$[cite: 7] | $5,829.45\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $5,023.54\text{ W/cm}^2$[cite: 7] |
| **$50\text{ nm}$** | $877.91$[cite: 7] | $23,317.78\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $19,888.63\text{ W/cm}^2$[cite: 7] |
| **$20\text{ nm}$** | $5486.94$[cite: 7] | $145,736.14\text{ W/cm}^2$[cite: 7] | $80.61\text{ W/cm}^2$[cite: 7] | $123,944.23\text{ W/cm}^2$[cite: 7] |

---

## 4. Collector Thermal Threshold & Back-Emission Current ($T_C$-Dependence)

$J_{\text{net}} = J_{\text{forward}}(T_H, \phi_E) - J_{\text{back}}(T_C, \phi_C)$[cite: 7]
$J_{\text{back}} = A_R T_C^2 \exp\left(-\frac{\phi_C}{k_B T_C}\right)$[cite: 7]

| Collector Temp ($T_C$) | Forward Current ($J_{\text{forward}}$) | Back-Emission ($J_{\text{back}}$) | Net Current ($J_{\text{net}}$) | Efficiency Loss |
| :---: | :---: | :---: | :---: | :---: |
| **$400\text{ K}$** | $50.888\text{ A/cm}^2$ | $2.43 \times 10^{-12}\text{ A/cm}^2$ | $50.888\text{ A/cm}^2$ | $0.00\%$ |
| **$600\text{ K}$** | $50.888\text{ A/cm}^2$ | $1.09 \times 10^{-5}\text{ A/cm}^2$ | $50.888\text{ A/cm}^2$ | $0.00\%$ |
| **$800\text{ K}$** | $50.888\text{ A/cm}^2$ | $0.027\text{ A/cm}^2$ | $50.861\text{ A/cm}^2$ | $0.05\%$ |
| **$1000\text{ K}$** | $50.888\text{ A/cm}^2$ | $3.319\text{ A/cm}^2$ | $47.569\text{ A/cm}^2$ | $6.52\%$ |
