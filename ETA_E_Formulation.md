# Microscopic & Quantum Kinetic Formulation of $\eta_e$

## Overview

The parameter $\eta_e$ represents the **electronic collection efficiency factor**. It quantifies the net fraction of emitted thermionic electrons ($e^-$) that successfully reach the collector, get absorbed, and drive net electrical power ($P_{\text{elec}}$) through the external circuit.

If an emitted electron fails to deposit its charge and kinetic energy into the collector's external electrical load, it constitutes a collection loss, causing $\eta_e$ to decrease ($\eta_e < 1$).

---

## The Fundamental Interaction Equation

At the microscopic particle level, most efficiency loss mechanisms that penalize $\eta_e$ can be generalized as a fundamental scattering or interaction event:

$$e^- \overset{X}{\longrightarrow} \theta$$

### Variable Definitions

| Variable | Symbol | Description |
| :--- | :---: | :--- |
| **Incoming Particle** | $e^-$ | The emitted lepton (electron) carrying thermal kinetic energy. |
| **Target Particle** | $\theta$ | • $e^-$ — Another electron in the vacuum gap (space-charge layer).<br>• $\gamma$ — A real photon traversing the radiative gap.<br>• $q$ — Up and down quarks bound within atomic nuclei of the collector.<br>• $\text{else}$ — Residual ambient gas molecules, ions, or plasma species. |
| **Mediator** | $X$ | • $\gamma^*$ (Virtual Photons) — Mediating QED electrostatic repulsion & scattering.<br>• $\emptyset$ (Null) — Direct real-photon Compton/Thomson scattering ($e^- + \gamma \to e^- + \gamma$). |

---

## Spatial Boundary Domain

These interactions occur along the spatial continuum between the emitter and collector:

$$\text{Location} \in [0, d]$$

* $\text{Location} = 0$: Emitter surface ($L1$)
* $0 < \text{Location} < d$: Inter-electrode vacuum/gas gap
* $\text{Location} = d$: Collector anode surface ($L2$)

---

## The Two Primary Loss Channels

### 1. In-Gap Deflection ($0 < \text{Location} < d$)

* **Mechanisms:**
  * $e^- \xrightarrow{\gamma^*} e^-$ *(Lepton–Lepton interaction via virtual photons)*
  * $e^- \xrightarrow{\emptyset} \gamma$ *(Lepton–Boson interaction via real photons)*
* **Physical Process:** As thermionic electrons stream into the gap, they experience electrostatic Coulomb repulsion from the surrounding electron cloud (space-charge potential barrier) or collide with real photon fields.
* **Kinetic Outcome:** The interaction shifts the momentum vector $\vec{p}_e$ of the electron. If forward momentum is inverted or deflected beyond the geometric view factor, the electron is repelled back to the emitter or escapes the boundary without contacting the collector.

---
### 2. Collector Surface Non-Absorption ($\text{Location} = d$)

* **Mechanisms:**
  * $e^- \xrightarrow{\gamma^*} q$ *(Lepton–Quark interaction via virtual photons)*[cite: 6]
  * $e^- \xrightarrow{\gamma^*} e^-$ *(Lepton–Lepton interaction via virtual photons)*

* **Physical Process:** Upon striking the collector anode, the incoming lepton ($e^-$) interacts electromagnetically with the fundamental constituent particles of the target material: positive charge centers (up/down quarks bound within atomic nuclei)[cite: 6] and bound/conduction leptons (electrons residing within the target's atomic shell and conduction states).

* **Kinetic Outcome:** Instead of transitioning into stable, directional conduction states to drive net electrical work ($J_{\text{th}} \cdot V_{\text{ext}}$)[cite: 6], non-electrical loss channels occur across both fundamental particle targets:

  1. **Lepton–Quark Interactions ($e^- \xrightarrow{\gamma^*} q$):**[cite: 6]
     * **Elastic/Inelastic Quark Backscattering:** The incoming lepton scatters off the composite quark potential field, deflecting along a reversed outward vector back into the inter-electrode gap[cite: 6].
     * **Quark Kinetic Energy Transfer:** The incoming lepton transfers its kinetic energy ($\frac{p_e^2}{2m_e}$) into non-directional kinetic motion of target composite quark clusters (nuclei), elevating waste thermal energy ($T_C$) rather than driving electrical current[cite: 6].

  2. **Lepton–Lepton Interactions ($e^- \xrightarrow{\gamma^*} e^-$):**
     * **Multi-Lepton Collision & Ejection:** The incoming lepton transfers sufficient momentum to a target lepton within the material, ejecting a secondary lepton back into the vacuum gap: $e^-$<sub>incoming</sub> + $e^-$<sub>target</sub> $\to$ $e^-$<sub>scattered</sub> + $e^-$<sub>ejected</sub>.
     * **Inelastic Lepton Kinetic Dissipation:** Elastic and inelastic momentum exchange between the incoming lepton and surrounding target leptons thermalizes the incoming particle's kinetic energy into random microstate motion prior to directional charge capture.
---

## The Golden Rule of $\eta_e$

An interaction **only penalizes $\eta_e$** if it changes the electron's momentum vector $\vec{p}_e$ or quantum state such that it **fails to be absorbed as usable current**.

> [!NOTE]
> If an electron undergoes minor electrostatic perturbation or forward elastic scattering along its path but still impacts the collector, gets absorbed into the conduction band, and flows through the external circuit, it constitutes a successful energy conversion event and does **not** reduce $\eta_e$.
