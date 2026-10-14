---
title: "ARG27 T1100 Woven and Unidirectional Composite Tensile Coupon Analysis"
layout: default
permalink: /projects/coupon-calculations/
---

# ARG27 T1100 Woven and Unidirectional Composite Tensile Coupon Analysis

> **GitHub Pages version:** The equations below use GitHub-compatible `$$...$$` LaTeX. Values from Toray are typical datasheet reference values, not certified design allowables. This document provides comparative calculations and references; verify any value against the original datasheet before use.

## Overview

Six plies of T1100/3960 woven carbon-fiber prepreg are being evaluated in axial tension at 0°/90° and ±45° fiber orientations. The previously discussed ±45° woven coupon recorded **5.00 kN**. The objective here is to summarize relevant Toray reference values and present simple transformed-stress and reference-load calculations for comparison.

## Test Geometry and Material Inputs

| Parameter | Value |
|---|---:|
| Material | Toray T1100G / 3960 epoxy, plain weave (PW); unidirectional (UD) reference included |
| Plies | 6 |
| Woven fiber orientations | 0°/90° or +45°/−45° relative to pull direction |
| Coupon dimensions | 25 × 250 mm |
| Assumed measured coupon thickness | 1.4 mm |
| Recorded ±45° woven load only | 5,000 N |
| Room-temperature oven-cured woven reference strengths | 1,519 MPa (0°); 1,501 MPa (90°) — 2017 Toray 3960 sheet (reference) |
| Room-temperature oven-cured UD reference strength | 3,702 MPa (0°), 2025 Toray 3960 sheet, P173EBN-19 |
| ±45° woven reference in-plane shear criterion | 114 MPa at 5% shear strain (2025 Toray 3960 sheet, autoclave-cured); this is a shear-strain reference, not an ultimate tensile strength |

**Thickness qualification:** Toray's published cured-ply thicknesses depend on format and product revision (typical cured ply thickness values near 0.19–0.20 mm for plain weave and approximately 0.183 mm for some UD formats). Verify the cured ply thickness for the specific product/version you used.

## Cross-Sectional Area

$$
A=wt=(25\,\mathrm{mm})(1.4\,\mathrm{mm})=\boxed{35\,\mathrm{mm^2}}
$$

## Toray T1100G Fiber and 3960 Prepreg Reported Properties

Toray reports properties for individual T1100G fibers, T1100G/3960 plain-weave laminates, and T1100G/3960 UD laminates. They are not the same material property set. The following tables summarize representative reported values from Toray datasheets.

### T1100G Fiber Properties (Bare Fiber; Not Laminate Properties)

| Property | Toray-reported value |
|---|---:|
| Fiber tensile strength | 7,000 MPa |
| Fiber tensile modulus | 324 GPa |
| Fiber strain at failure | 2.2% |
| Fiber density | 1.79 g/cm³ |
| Filament diameter | 5 µm |
| 12K tow linear density | 505 g/1000 m |
| 24K tow linear density | 1,010 g/1000 m |
| Fiber coefficient of thermal expansion | −0.5 × 10⁻⁶ /°C |

Toray also reports reference composite properties for different resin systems and fiber volume fractions; those composite numbers are provided in the datasheets and should not be assumed identical across product codes.

### Toray 3960 / T1100G Plain-Weave Properties — 2025 Sheet, Autoclave RTA

| Property | Symbol | Test method | Toray RTA value |
|---|---|---|---:|
| 0° tensile strength | $F_{1t}$ | ASTM D3039 | 1,662 MPa |
| 90° tensile strength | $F_{2t}$ | ASTM D3039 | 1,538 MPa |
| 0° tensile modulus | $E_{1t}$ | ASTM D3039 | 87.8 GPa |
| 90° tensile modulus | $E_{2t}$ | ASTM D3039 | 85.5 GPa |
| In-plane shear stress at 5% shear strain | $F_{12\,@5\%}$ | ASTM D5379 | 114 MPa |
| In-plane shear modulus | $G_{12}$ | ASTM D5379 | 5.17 GPa |
| Laminate density | $\rho$ | ASTM D792 | 1.570 g/cm³ |
| Fiber volume fraction | $V_f$ | ASTM D3171 | 56.9% |
| Cured ply thickness | CPT | ASTM D3171 | approx. 0.193 mm |

**Important:** 114 MPa is a 5%-strain shear criterion from the autoclave-cured 2025 sheet and is not a measured ±45° woven ultimate tensile failure stress. Use caution when comparing different cure processes or product revisions.

### Toray 3960 / T1100G Plain-Weave Properties — 2017 Sheet, Oven RTA

| Property | Symbol | Toray oven RTA value |
|---|---:|
| 0° tensile strength ($F_{1t}$) | 1,519 MPa |
| 90° tensile strength ($F_{2t}$) | 1,501 MPa |
| Cured ply thickness | CPT | 0.20 mm |

The older plain-weave table does not list a direct in-plane shear strength in the same way; do not substitute short-beam shear for $F_{12}$.

### Toray 3960 / T1100G Unidirectional Properties — 2025 Sheet, P173EBN-19

| Property | Symbol | Autoclave RTA | Oven RTA |
|---|---:|---:|---:|
| 0° tensile strength ($F_{1t}$) | 3,778 MPa | 3,702 MPa |
| 90° tensile strength ($F_{2t}$) | 68.3 MPa | 59.4 MPa |
| 0° tensile modulus ($E_{1t}$) | 172 GPa | 169 GPa |
| In-plane shear strength at 5% strain ($F_{12\,@5\%}$) | 107 MPa | — |
| In-plane shear modulus ($G_{12}$) | 5.38 GPa | 5.52 GPa |
| Cured ply thickness (CPT) | approx. 0.183 mm | — |

### Toray 3960 Neat Resin (2025 Datasheet)

| Property | Reported value |
|---|---:|
| Neat resin density | 1.274 g/cm³ |
| Dry glass-transition temperature | 202°C |

These resin values characterize the resin system, not a cured laminate's axial tensile strength.

## Theoretical 0°/90° Woven Axial Tensile Loads

Use a simple area-based conversion for axial tensile load estimates using published axial tensile strengths.

$$
\sigma_{x,\mathrm{failure}}\approx F_{it},\qquad F_{\mathrm{reference}}=\sigma_{x,\mathrm{failure}}A
$$

For the 2017 oven-cured 0° woven direction:

$$
F_{0^\circ,\mathrm{PW}}=(1519\,\mathrm{N/mm^2})(35\,\mathrm{mm^2})=53{,}165\,\mathrm{N}
$$

$$
\boxed{F_{0^\circ,\mathrm{PW}}\approx 53.17\,\mathrm{kN}}
$$

For the 90° woven direction:

$$
F_{90^\circ,\mathrm{PW}}=(1501\,\mathrm{N/mm^2})(35\,\mathrm{mm^2})=52{,}535\,\mathrm{N}
$$

$$
\boxed{F_{90^\circ,\mathrm{PW}}\approx 52.54\,\mathrm{kN}}
$$

For the 2025 autoclave RTA dataset:

$$
F_{0^\circ,\mathrm{PW,autoclave}}=(1662)(35)=\boxed{58.17\,\mathrm{kN}}
$$

$$
F_{90^\circ,\mathrm{PW,autoclave}}=(1538)(35)=\boxed{53.83\,\mathrm{kN}}
$$

These values are nominal and should not be treated as direct predictions for different cure processes without verification.

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

This is the local stress transformation and not a full failure model. Off-axis response can include rotation, nonlinear shear, and progressive damage.

## Theoretical Reference Load Using a Shear Criterion

Using the 2025 autoclave RTA plain-weave reported $F_{12\,@5\%}=114\,\mathrm{MPa}$ as a reference:

$$
|\tau_{12}|=\frac{F}{2A}=F_{12\,@5\%}
$$

$$
F_{45^\circ,\mathrm{reference}}=2AF_{12\,@5\%}=2(35\,\mathrm{mm^2})(114\,\mathrm{N/mm^2})
$$

$$
\boxed{F_{45^\circ,\mathrm{reference}}=7980\,\mathrm{N}=7.98\,\mathrm{kN}}
$$

**Interpretation:** 7.98 kN is the axial force corresponding to a transformed material-axis shear stress of 114 MPa under idealized assumptions; it is not a verified ultimate load.

## Theoretical Unidirectional Tensile Loads

For a 0° UD laminate using Toray's 2025 P173EBN-19 oven RTA 0° tensile strength:

$$
F_{0^\circ,\mathrm{UD}}=F_{1t}A=(3702\,\mathrm{N/mm^2})(35\,\mathrm{mm^2})
$$

$$
\boxed{F_{0^\circ,\mathrm{UD}}=129{,}570\,\mathrm{N}=129.57\,\mathrm{kN}}
$$

For a 90° UD laminate under transverse tension:

$$
F_{90^\circ,\mathrm{UD}}=F_{2t}A=(59.4\,\mathrm{N/mm^2})(35\,\mathrm{mm^2})=\boxed{2079\,\mathrm{N}=2.08\,\mathrm{kN}}
$$

For ±45° UD using the autoclave $F_{12\,@5\%}=107\,\mathrm{MPa}$ reference:

$$
F_{45^\circ,\mathrm{UD,reference}}=2(35)(107)=\boxed{7.49\,\mathrm{kN}}
$$

These are reference computations only and not ultimate-failure predictions.

## Expected Coupon Load Summary

| Configuration | Published property used | Calculated nominal load | Basis / status |
|---|---:|---:|---|
| 0° woven, oven RTA | 1,519 MPa axial tensile strength | **53.17 kN** | 2017 oven reference; untested |
| 90° woven, oven RTA | 1,501 MPa axial tensile strength | **52.54 kN** | 2017 oven reference; untested |
| 0° woven, autoclave RTA | 1,662 MPa axial tensile strength | **58.17 kN** | 2025 autoclave reference; untested |
| 90° woven, autoclave RTA | 1,538 MPa axial tensile strength | **53.83 kN** | 2025 autoclave reference; untested |
| ±45° woven, shear criterion | 114 MPa shear at 5% strain | **7.98 kN** | 2025 autoclave shear criterion; not ultimate load |
| 0° UD, oven RTA | 3,702 MPa axial tensile strength | **129.57 kN** | 2025 P173EBN-19 oven reference; untested |
| 90° UD, oven RTA | 59.4 MPa transverse tensile strength | **2.08 kN** | 2025 P173EBN-19 oven reference; untested |
| ±45° UD, shear criterion | 107 MPa shear at 5% strain | **7.49 kN** | 2025 autoclave criterion; not ultimate load |

**Machine capacity:** These nominal aligned-fiber reference loads can exceed a 50 kN Instron limit for a 25 mm wide coupon. Do not attempt to pull past the machine/load-cell/fixture rating.

## Experimental Comparison — Existing ±45° Woven Observation Only

The previously reported ±45° woven coupon load was **5.00 kN**; confirmation of a gauge-section ultimate failure requires checking the test trace and failure photographs.

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

This 37.3% difference is not proof of a 37.3% loss in composite strength; the shear-based comparison is not a validated tensile ultimate-load model.

## Conclusion

For an assumed 25 mm × 1.4 mm gauge cross-section, oven-cured Toray reference strengths imply approximately 53.17 kN for 0° woven and 52.54 kN for 90° woven coupons. The ±45° woven shear-criterion reference is 7.98 kN while the measured ±45° woven coupon was 5.00 kN. These computations are illustrative; verify all values against original datasheets and test records.

## Assumptions and Limitations

- Coupon gauge width and thickness are assumed to be 25 mm and 1.4 mm for every hypothetical comparison; actual coupon dimensions and fiber volume content may differ.
- Length is 250 mm; grip length, tabbing and strain measurement method still matter for test outcomes.
- The 2017 oven and 2025 autoclave woven data refer to different product revisions and are presented separately rather than assumed identical.
- T1100G fiber properties, 3960 UD properties, and 3960 woven-laminate properties must not be interchanged.
- The ±45° shear transformation assumes uniform axial stress. The actual off-axis response can include nonlinear shear, fiber reorientation, matrix cracking, delamination and progressive damage.
- A measured 5 kN is not necessarily an ultimate load unless a valid failure event was observed and documented.
- Alignment, tab/grip effects, strain rate, test method, cure, storage, prepreg age and laminate quality can change measured loads.
- Published Toray numbers are typical averages for material selection, not structural allowables; use representative coupon tests and a statistically defensible method before relying on these numbers.
- Do not exceed rated equipment capacity when testing.

## References

1. [Toray Composite Materials America — 3960 Prepreg System (2025 technical data sheet)](https://www.toraycma.com/wp-content/uploads/3960-Prepreg-System_3.14.2025.pdf)
2. [Toray Composite Materials America — Prepreg data sheet directory](https://www.toraycma.com/resources/data-sheets/)
3. [Toray 3960 Prepreg System, Rev. 4 (November 2017), reproduced document](https://www.scribd.com/document/875661736/T1100-3960-Prepreg-Optimal-Properties)
4. [Toray T1100G Carbon Fiber data sheet](https://www.toraycma.com/wp-content/uploads/T1100G-Data-Sheet.pdf)
5. [ASTM D3039/D3039M — Tensile Properties of Polymer Matrix Composite Materials](https://www.astm.org/d3039_d3039m-17.html)
6. [ASTM D3518/D3518M — In-Plane Shear Response from ±45° Tensile Test](https://www.astm.org/d3518_d3518m-18.html)
7. [ASTM D5379/D5379M — Shear Properties by V-Notched Beam Method](https://www.astm.org/standards/d5379)
