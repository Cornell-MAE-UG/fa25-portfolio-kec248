# ARG27 T1100 Woven and Unidirectional Composite Tensile Coupon Analysis

> **GitHub Pages version:** The equations below use GitHub-compatible `$$...$$` LaTeX. Values from Toray are *typical datasheet reference values*, not certified design allowables. This document retains the previously recorded ±45° woven coupon observation; all other coupon loads are **theoretical expectations only**.

## Overview

Six plies of T1100/3960 woven carbon-fiber prepreg are being evaluated in axial tension at 0°/90° and ±45° fiber orientations. The previously discussed ±45° woven coupon recorded **5.00 kN**. No physical tensile results are yet available for the 0°/90° woven or unidirectional coupons. This analysis calculates reference loads from published Toray strengths and compares the distinct tensile and shear-dominated loading cases. Values are not interchangeable between different fiber formats, cure methods, and test conditions.

## Test Geometry and Material Inputs

| Parameter | Value |
|---|---:|
| Material | Toray T1100G / 3960 epoxy, plain weave (PW); unidirectional (UD) reference included |
| Plies | 6 |
| Woven fiber orientations | 0°/90° or +45°/−45° relative to pull direction |
| Coupon dimensions | 25 × 250 mm |
| Assumed measured coupon thickness | 1.4 mm |
| Recorded ±45° woven load only | 5,000 N |
| Room-temperature oven-cured woven reference strengths | 1,519 MPa (0°); 1,501 MPa (90°), 2017 Toray 3960 sheet |
| Room-temperature oven-cured UD reference strength | 3,702 MPa (0°), 2025 Toray 3960 sheet, P173EBN-19 |
| ±45° woven reference in-plane shear criterion | 114 MPa at 5% shear strain, 2025 Toray 3960 sheet, **autoclave-cured**, not an ultimate tensile strength |

**Thickness qualification:** Toray's published cured-ply thicknesses depend on format: approximately **0.20 mm/ply for older PW**, **0.19 mm/ply for newer PW**, and **0.183 mm/ply for P173EBN-19 UD**. Six nominal PW plies therefore are about 1.14–1.20 mm, not necessarily 1.4 mm. All calculations below intentionally use the **specified 1.4 mm measured coupon thickness**. Before comparing testing to predictions, measure actual gauge-region width and thickness for each coupon.

## Cross-Sectional Area

$$
A=wt=(25\,\mathrm{mm})(1.4\,\mathrm{mm})=\boxed{35\,\mathrm{mm^2}}
$$

## Toray T1100G Fiber and 3960 Prepreg Reported Properties

Toray reports properties for **individual T1100G fibers**, **T1100G/3960 plain-weave laminates**, and **T1100G/3960 UD laminates**. They are not the same material property set. The following tables include the reported characteristics relevant to coupon mechanics and comparisons. **RTA** means room-temperature, as-received; **CTA** is cold-temperature, as-received; **ETW** means elevated-temperature, wet-conditioned. A dash means the relevant datasheet does not report a value under that condition.

### T1100G Fiber Properties (Bare Fiber; Not Laminate Properties)

| Property | Toray-reported value |
|---|---:|
| **Fiber tensile strength** | **7,000 MPa** |
| Fiber tensile modulus | 324 GPa |
| Fiber strain at failure | 2.2% |
| Fiber density | 1.79 g/cm³ |
| Filament diameter | 5 µm |
| 12K tow linear density | 505 g/1000 m |
| 24K tow linear density | 1,010 g/1000 m |
| Fiber coefficient of thermal expansion | −0.5 × 10⁻⁶ /°C |
| Specific heat | 0.749 J/(g·°C) |
| Thermal conductivity | 0.130 J/(cm·s·°C) |
| Electrical resistivity | 1.4 × 10⁻³ Ω·cm |
| Carbon content | >96% |
| Sodium + potassium | <50 ppm |

Toray also reports the following **reference composite** properties in the T1100G fiber datasheet for a **different #2592 epoxy resin (130°C cure, 60% fiber volume)**: tensile strength **3,460 MPa**, tensile modulus **185 GPa**, tensile strain **1.82%**, compressive strength **1,870 MPa**, flexural strength **1,920 MPa**, flexural modulus **159 GPa**, interlaminar shear strength (ILSS) **104.5 MPa**, in-plane shear strength **160 MPa**, and 90° tensile strength **80 MPa**. These values are **not** valid replacements for 3960 woven or UD laminate properties.

### Toray 3960 / T1100G Plain-Weave Properties — 2025 Sheet, Autoclave RTA

Part designation **FT6243R-3EF (T1100G-12K PW)**, nominal room-temperature, as-received, autoclave cure. Toray reports the following:

| Property | Symbol | Test method | Toray RTA value |
|---|---|---|---:|
| 0° tensile strength | $F_{1t}$ | ASTM D3039 | 1,662 MPa |
| 90° tensile strength | $F_{2t}$ | ASTM D3039 | 1,538 MPa |
| 0° tensile modulus | $E_{1t}$ | ASTM D3039 | 87.8 GPa |
| 90° tensile modulus | $E_{2t}$ | ASTM D3039 | 85.5 GPa |
| 0° compressive strength | $F_{1c}$ | ASTM D6641 | 848 MPa |
| 90° compressive strength | $F_{2c}$ | ASTM D6641 | 827 MPa |
| 0° compressive modulus | $E_{1c}$ | ASTM D6641 | 77.9 GPa |
| 90° compressive modulus | $E_{2c}$ | ASTM D6641 | 77.9 GPa |
| In-plane shear stress at 5% shear strain | $F_{12\,@5\%}$ | ASTM D5379 | 114 MPa |
| In-plane shear modulus | $G_{12}$ | ASTM D5379 | 5.17 GPa |
| Short-beam strength | SBS | ASTM D2344 | 86.2 MPa |
| Open-hole compression, QI 25/50/25 | OHC | ASTM D6484 | 323 MPa |
| Compression after impact, QI 25/50/25 | CAI | ASTM D7137 | 299 MPa |
| Laminate density | $\rho$ | ASTM D792 | 1.570 g/cm³ |
| Fiber volume fraction | $V_f$ | ASTM D3171 | 56.9% |
| Cured ply thickness | CPT | ASTM D3171 | approx. 0.0076 in (0.193 mm) |

**Important:** 114 MPa is a **5%-strain shear criterion**, not a measured ±45° woven **ultimate tensile failure stress**. The 2025 sheet reports 0°/90° axial tensile properties under different conditions; only the 90° oven-cured RTA result (1,434 MPa) is available in its woven oven-cure table. For the calculations based on *oven-cured 0° and 90° properties together*, the older reference below is used.

### Toray 3960 / T1100G Plain-Weave Properties — 2017 Sheet, Oven RTA

Part designation in the earlier sheet **FT62YER-3EI (T1100G-12K PW)**. This is an **older material/product dataset**, used to supply a matched oven-cured 0°/90° tensile comparison.

| Property | Symbol | Toray oven RTA value |
|---|---|---:|
| 0° tensile strength | $F_{1t}$ | 1,519 MPa |
| 90° tensile strength | $F_{2t}$ | 1,501 MPa |
| 0° tensile modulus | $E_{1t}$ | 83 GPa |
| 90° tensile modulus | $E_{2t}$ | 87 GPa |
| 0° compressive strength | $F_{1c}$ | 880 MPa |
| 90° compressive strength | $F_{2c}$ | 889 MPa |
| 0° compressive modulus | $E_{1c}$ | 74 GPa |
| 90° compressive modulus | $E_{2c}$ | 76 GPa |
| Short-beam shear strength | SBS | 89 MPa |
| Open-hole tension, QI 25/50/25 | OHT | 563 MPa |
| Open-hole compression, QI 25/50/25 | OHC | 318 MPa |
| Compression after impact, QI 25/50/25 | CAI | 313 MPa |
| Laminate density | $\rho$ | 1.551 g/cm³ |
| Fiber volume fraction | $V_f$ | 52.8% |
| Cured ply thickness | CPT | 0.20 mm |

The older plain-weave table **does not list a direct in-plane shear strength or modulus**. Do not substitute the **short-beam shear** value for $F_{12}$; short-beam strength describes a different test and stress state.

### Toray 3960 / T1100G Unidirectional Properties — 2025 Sheet, P173EBN-19

Part designation **P173EBN-19 (T1100G UD/Gr 192)**, RTA values shown for **autoclave cure** and **oven cure** when available. Unlike plain weave, UD 90° direction has no aligned load-carrying fibers and is matrix/interface dominated.

| Property | Symbol | Autoclave RTA | Oven RTA |
|---|---|---:|---:|
| 0° tensile strength | $F_{1t}$ | 3,778 MPa | 3,702 MPa |
| 90° tensile strength | $F_{2t}$ | 68.3 MPa | 59.4 MPa |
| 0° tensile modulus | $E_{1t}$ | 172 GPa | 169 GPa |
| 90° tensile modulus | $E_{2t}$ | 9.24 GPa | 9.03 GPa |
| 0° compressive strength (backed out) | $F_{1c}$ | 2,062 MPa | — |
| 90° compressive strength | $F_{2c}$ | 259 MPa | — |
| 0° compressive modulus | $E_{1c}$ | 153 GPa | — |
| 90° compressive modulus | $E_{2c}$ | 9.58 GPa | — |
| In-plane shear strength at 5% strain | $F_{12\,@5\%}$ | 107 MPa | — |
| In-plane shear modulus | $G_{12}$ | 5.38 GPa | 5.52 GPa |
| Short-beam strength | SBS | 114 MPa | 117 MPa |
| Open-hole compression, QI 25/50/25 | OHC | 336 MPa | 324 MPa |
| Compression after impact, QI 25/50/25 | CAI | 339 MPa | 299 MPa |
| Laminate density | $\rho$ | 1.573 g/cm³ | 1.570 g/cm³ |
| Fiber volume fraction | $V_f$ | 57.9% | 56.5% |
| Cured ply thickness | CPT | approx. 0.183 mm | — |

**Other UD format:** The 2025 Toray sheet also lists a lighter **P173EBN-7 (T1100G UD/Gr 70)** configuration with RTA autoclave 0° tensile strength **3,282 MPa**, 90° tensile strength **71.0 MPa**, 0° tensile modulus **155 GPa**, and 90° tensile modulus **8.27 GPa**. Do not assume UD roll types have identical strengths or cured thicknesses.

### Toray 3960 Neat Resin (2025 Datasheet)

| Property | Reported value |
|---|---:|
| Neat resin density | 1.274 g/cm³ |
| Dry glass-transition temperature | 202°C (395°F) |
| Wet glass-transition temperature | 168°C (334°F) |
| Minimum viscosity | 11.2 poise at 154°C (309°F) |

These resin values characterize the resin system, not a cured laminate's axial tensile strength.

## Theoretical 0°/90° Woven Axial Tensile Loads

With warp or weft aligned to tensile loading, the woven laminate can carry axial force primarily through one aligned fiber family. Use the matched **2017 Toray oven-cured RTA woven** tensile strengths and the specified actual cross-sectional area:

$$
\sigma_{x,\mathrm{failure}}\approx F_{it},\qquad
F_{\mathrm{reference}}=\sigma_{x,\mathrm{failure}}A
$$

For the **0° woven direction**:

$$
F_{0^\circ,\mathrm{PW}}=(1519\,\mathrm{N/mm^2})(35\,\mathrm{mm^2})
=53{,}165\,\mathrm{N}
$$

$$
\boxed{F_{0^\circ,\mathrm{PW}}\approx 53.17\,\mathrm{kN}}
$$

For the **90° woven direction**:

$$
F_{90^\circ,\mathrm{PW}}=(1501\,\mathrm{N/mm^2})(35\,\mathrm{mm^2})
=52{,}535\,\mathrm{N}
$$

$$
\boxed{F_{90^\circ,\mathrm{PW}}\approx 52.54\,\mathrm{kN}}
$$

Because a plain weave contains both 0° and 90° tows, rotating the fabric by 90° exchanges warp and weft, not a change to matrix-only transverse tension. The small difference above comes from Toray's separate warp/weft measurements.

For comparison, the **2025 autoclave RTA** woven dataset would produce:

$$
F_{0^\circ,\mathrm{PW,autoclave}}=(1662)(35)=\boxed{58.17\,\mathrm{kN}}
$$

$$
F_{90^\circ,\mathrm{PW,autoclave}}=(1538)(35)=\boxed{53.83\,\mathrm{kN}}
$$

These values should not be treated as predictions for an oven-only cure without verifying equivalency between cure processes and product codes.

## Stress Transformation at 45 Degrees

For uniaxial applied tension, with the axes rotated to one fabric fiber direction:

$$
\sigma_1=\sigma_x\cos^2\theta,\qquad
\sigma_2=\sigma_x\sin^2\theta
$$

$$
\tau_{12}=-\sigma_x\sin\theta\cos\theta=-\frac{\sigma_x}{2}\sin(2\theta)
$$

At $\theta=45^\circ$:

$$
\sigma_1=\sigma_2=|\tau_{12}|=\frac{\sigma_x}{2}
$$

This is the **local stress transformation**, not by itself a complete off-axis laminate failure model. A ±45° woven laminate can rotate, undergo nonlinear shear and damage, and carry combined local normal and shear stresses.

## Theoretical Reference Load Using a Shear Criterion

Use the **2025 autoclave RTA plain-weave** reported $F_{12\,@5\%}=114\,\mathrm{MPa}$ as a **reference shear-strain criterion**. This does **not** mean Toray guarantees 45° tensile rupture at this load.

$$
|\tau_{12}|=\frac{F}{2A}=F_{12\,@5\%}
$$

$$
F_{45^\circ,\mathrm{reference}}=2AF_{12\,@5\%}=2(35\,\mathrm{mm^2})(114\,\mathrm{N/mm^2})
$$

$$
\boxed{F_{45^\circ,\mathrm{reference}}=7980\,\mathrm{N}=7.98\,\mathrm{kN}}
$$

**Interpretation:** 7.98 kN is the axial force corresponding to a transformed material-axis shear stress of 114 MPa, assuming homogeneous uniaxial stress. It is **not a verified ultimate load**. A separate measured woven ±45° response or a calibrated nonlinear failure model is required to predict ultimate fracture.

## Theoretical Unidirectional Tensile Loads

For a **0° UD** laminate using Toray's 2025 P173EBN-19 **oven RTA** 0° tensile strength:

$$
F_{0^\circ,\mathrm{UD}}=F_{1t}A=(3702\,\mathrm{N/mm^2})(35\,\mathrm{mm^2})
$$

$$
\boxed{F_{0^\circ,\mathrm{UD}}=129{,}570\,\mathrm{N}=129.57\,\mathrm{kN}}
$$

For a **90° UD** laminate under transverse tension (matrix/interface dominated):

$$
F_{90^\circ,\mathrm{UD}}=F_{2t}A=(59.4\,\mathrm{N/mm^2})(35\,\mathrm{mm^2})
$$

$$
\boxed{F_{90^\circ,\mathrm{UD}}=2079\,\mathrm{N}=2.08\,\mathrm{kN}}
$$

For **±45° UD**, the transformed shear criterion using the P173EBN-19 2025 *autoclave* RTA $F_{12\,@5\%}=107\,\mathrm{MPa}$ would correspond to:

$$
F_{45^\circ,\mathrm{UD,reference}}=2(35)(107)=\boxed{7.49\,\mathrm{kN}}
$$

Again, this is **not** an ultimate tensile-failure prediction. A single +45° UD laminate is not equivalent to a balanced ±45° UD laminate or to ±45° woven cloth; do not apply the same simplified criterion without verifying stacking sequence and failure mode.

## Expected Coupon Load Summary

| Configuration | Published property used | Calculated nominal load | Basis / status |
|---|---:|---:|---|
| **0° woven, oven RTA** | 1,519 MPa axial tensile strength | **53.17 kN** | Older 2017 oven reference; untested |
| **90° woven, oven RTA** | 1,501 MPa axial tensile strength | **52.54 kN** | Older 2017 oven reference; untested |
| 0° woven, autoclave RTA | 1,662 MPa axial tensile strength | 58.17 kN | 2025 autoclave reference; untested |
| 90° woven, autoclave RTA | 1,538 MPa axial tensile strength | 53.83 kN | 2025 autoclave reference; untested |
| **±45° woven, shear criterion** | 114 MPa shear at 5% strain | **7.98 kN** | 2025 autoclave shear criterion; **not ultimate load** |
| **0° UD, oven RTA** | 3,702 MPa axial tensile strength | **129.57 kN** | 2025 P173EBN-19 oven reference; untested |
| 90° UD, oven RTA | 59.4 MPa transverse tensile strength | 2.08 kN | 2025 P173EBN-19 oven reference; untested |
| ±45° UD, shear criterion | 107 MPa shear at 5% strain | 7.49 kN | 2025 P173EBN-19 autoclave criterion; **not ultimate load** |

**Machine capacity:** These nominal aligned-fiber reference loads can exceed a 50 kN Instron limit even for a 25 mm wide coupon. **Do not attempt to pull past the machine/load-cell/fixture rating.** Check the rated capacity and grip limits before deciding dimensions. A lower-capacity load frame does not establish the true ultimate strength of a coupon that survives its maximum test load.

## Experimental Comparison — Existing ±45° Woven Observation Only

The previously reported ±45° woven coupon load was **5.00 kN**; whether that was a confirmed gauge-section ultimate failure requires checking the actual test trace and failure photographs. No 0° woven, 90° woven, or UD experiments are represented in this document.

$$
\sigma_x=\frac{F}{A}=\frac{5000\,\mathrm{N}}{35\,\mathrm{mm^2}}=\boxed{142.86\,\mathrm{MPa}}
$$

$$
\boxed{|\tau_{12,\mathrm{test}}|=\frac{\sigma_x}{2}=71.43\,\mathrm{MPa}}
$$

The material-axis normal stresses $\sigma_1$ and $\sigma_2$ are likewise 71.43 MPa for the idealized transformation.

$$
\eta=\frac{F_{\mathrm{test}}}{F_{45^\circ,\mathrm{reference}}}=\frac{5.00}{7.98}=\boxed{62.7\%}
$$

$$
\Delta_F=\frac{F_{45^\circ,\mathrm{reference}}-F_{\mathrm{test}}}{F_{45^\circ,\mathrm{reference}}}\times100\%=\boxed{37.3\%}
$$

| Result | Value |
|---|---:|
| Previously recorded ±45° woven load | **5.00 kN** |
| ±45° reference shear criterion load | **7.98 kN** |
| Axial stress at recorded load | **142.86 MPa** |
| Transformed shear stress at recorded load | **71.43 MPa** |
| Recorded/reference load ratio | **62.7%** |
| Difference relative to shear criterion reference | **37.3%** |
| 0°/90° woven experimental results | **Not yet tested** |
| UD experimental results | **Not yet tested** |

This 37.3% difference is **not** proof of a 37.3% loss in composite strength: the shear-based comparison is not a validated tensile ultimate-load model.

## Conclusion

For an assumed **25 mm × 1.4 mm** gauge cross-section, oven-cured Toray reference strengths imply approximately **53.17 kN** for 0° woven and **52.54 kN** for 90° woven coupons. The ±45° woven reference of **7.98 kN** is a stress-transformation estimate tied to a **5%-strain shear criterion**, not to measured ultimate tensile rupture. A 0° UD P173EBN-19 coupon calculated from Toray's newer oven RTA tensile property has a much larger nominal tensile reference of **129.57 kN**; a transverse 90° UD coupon has a much smaller reference of **2.08 kN**. The prior ±45° woven observation of **5.00 kN** is the only test value included. All other configurations remain predictions pending actual tensile testing.

## Assumptions and Limitations

- Coupon gauge width and thickness are assumed to be 25 mm and 1.4 mm for every hypothetical comparison; actual coupon dimensions and fiber volume content may differ by material format.
- Length is 250 mm, but it does not directly enter the $F=\sigma A$ ultimate-force estimate; grip length, tabbing and strain measurement still matter.
- The 2017 oven and 2025 autoclave woven data refer to **different product revisions/designations**, and are presented separately rather than assumed identical.
- T1100G fiber properties, 3960 UD properties, and 3960 woven-laminate properties must not be interchanged.
- The ±45° shear transformation assumes uniform axial stress. The actual off-axis response can include nonlinear shear, fiber reorientation, matrix cracking, delamination and damage progression.
- A measured 5 kN is not necessarily an ultimate load unless a valid failure event was observed and documented.
- Alignment, tab/grip effects, strain rate, test method, cure, storage, prepreg age and laminate quality can change measured loads.
- Published Toray numbers are typical averages for material selection, not structural allowables; use representative coupon tests and a statistically defensible method before relying on these numbers in FSAE safety decisions.
- A **50 kN** test machine may not be sufficient to reach failure of the specified aligned-fiber coupon dimensions, and exceeding rated equipment capacity is not acceptable.

## References

1. [Toray Composite Materials America — 3960 Prepreg System (2025 technical data sheet)](https://www.toraycma.com/wp-content/uploads/3960-Prepreg-System_3.14.2025.pdf). Refer to tables for FT6243R-3EF PW, P173EBN-19 UD and P173EBN-7 UD; Toray typical reference values.
2. [Toray Composite Materials America — Prepreg data sheet directory](https://www.toraycma.com/resources/data-sheets/). Toray's data sheet directory and notice that typical properties are not guaranteed values.
3. [Toray 3960 Prepreg System, Rev. 4 (November 2017), reproduced document](https://www.scribd.com/document/875661736/T1100-3960-Prepreg-Optimal-Properties). Earlier oven-cured 0°/90° woven laminate values used for the matched oven-cure load comparison.
4. [Toray T1100G Carbon Fiber data sheet](https://www.toraycma.com/wp-content/uploads/T1100G-Data-Sheet.pdf). Fiber-level properties, distinct from cured 3960 laminate properties.
5. [ASTM D3039/D3039M — Tensile Properties of Polymer Matrix Composite Materials](https://www.astm.org/d3039_d3039m-17.html).
6. [ASTM D3518/D3518M — In-Plane Shear Response from ±45° Tensile Test](https://www.astm.org/d3518_d3518m-18.html).
7. [ASTM D5379/D5379M — Shear Properties by V-Notched Beam Method](https://www.astm.org/standards/d5379).
