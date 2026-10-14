# ARG27 T1100 Woven Composite Tensile Coupon Analysis

> **GitHub Pages version:** [T1100_45_Degree_Woven_Tensile_Analysis.html](T1100_45_Degree_Woven_Tensile_Analysis.html) follows the earlier torsional-twist-test Jekyll HTML structure and uses `\[...\]`[...] 

## Overview

Six plies of T1100/3960 woven carbon-fiber prepreg were oriented at 45° to axial loading, giving +45° and −45° tow directions. The test reported a load of **5.00 kN**. The purpose of this analysis is to compare the measured load against a provisional in-plane shear criterion for a ±45° woven laminate.

## Test Geometry and Material Inputs

| Parameter | Value |
|---|---:|
| Material | T1100 / Toray 3960 woven prepreg |
| Plies | 6 |
| Woven fiber orientation | +45° / −45° relative to pull direction |
| Coupon dimensions | 25 × 250 mm |
| Coupon thickness | 1.4 mm |
| Recorded load | 5,000 N |
| Assumed reference in-plane shear stress | 114 MPa (provisional; not verified for this exact woven material) |

## Cross-Sectional Area

$$
A=wt=(25\,\mathrm{mm})(1.4\,\mathrm{mm})=\boxed{35\,\mathrm{mm^2}}
$$

## Experimental Axial Tensile Stress

$$
\sigma_x=\frac{F}{A}=\frac{5000\,\mathrm{N}}{35\,\mathrm{mm^2}}=\boxed{142.86\,\mathrm{MPa}}
$$

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

At 5 kN:

$$
\boxed{|\tau_{12,\mathrm{test}}|=71.43\,\mathrm{MPa}}
$$

The normal stresses $\sigma_1$ and $\sigma_2$ are also 71.43 MPa. Thus, shear is **not** the only local stress acting on the fabric.

## Theoretical Reference Load Using a Shear Criterion

Assume an illustrative in-plane shear stress criterion $S_{12}=114\,\mathrm{MPa}$.

$$
|\tau_{12}|=\frac{F}{2A}=S_{12}
$$

$$
F_{\mathrm{reference}}=2AS_{12}=2(35\,\mathrm{mm^2})(114\,\mathrm{N/mm^2})
$$

$$
\boxed{F_{\mathrm{reference}}=7980\,\mathrm{N}=7.98\,\mathrm{kN}}
$$

**Interpretation:** This is the axial load that would produce 114 MPa transformed shear stress in the coupon. It is **not** a verified prediction of ultimate tensile failure. The 114 MPa value must be treated as a provisional comparison metric, not as a material allowables value.

## Experimental Comparison

$$
\eta=\frac{F_{\mathrm{test}}}{F_{\mathrm{reference}}}=\frac{5.00}{7.98}=\boxed{62.7\%}
$$

$$
\Delta_F=\frac{F_{\mathrm{reference}}-F_{\mathrm{test}}}{F_{\mathrm{reference}}}\times100\%=\boxed{37.3\%}
$$

| Result | Value |
|---|---:|
| Experimental load | **5.00 kN** |
| Reference criterion load | **7.98 kN** |
| Experimental axial stress | **142.86 MPa** |
| Transformed shear stress at 5 kN | **71.43 MPa** |
| Experimental/reference force ratio | **62.7%** |
| Difference relative to reference | **37.3%** |

## Conclusion

The recorded 5.00 kN tensile load corresponds to 142.86 MPa axial engineering stress and 71.43 MPa transformed in-plane shear stress for the 45° woven coupon. Using the provisional 114 MPa shear criterion as a reference, the measured load reaches about 62.7% of that criterion, leaving a 37.3% deficit relative to the illustrative benchmark. This comparison is useful for contextualizing the loading state, but it is not a validated failure prediction for the material system.

## Assumptions and Limitations

- All six woven plies are oriented with tow families at ±45° to the applied tensile load.
- The coupon's gauge-region width is 25 mm and local thickness is 1.4 mm.
- Engineering stress is taken as uniform in the gauge section; grip/tab and edge effects are ignored.
- The 114 MPa reference shear criterion is provisional; verify against the actual fabric-specific datasheet.
- Coupon peak load and the failure mode (gauge fracture, grip failure, delamination, or test stop) need confirmation.
- A true laminate failure model must account for combined local normal/shear stresses, tow rotation, nonlinear shear, and progressive damage.
- Prepreg age, storage, cure and manufacturing quality can influence measured results.

## References

1. [Toray Composite Materials America — 3960 prepreg data sheets](https://www.toraycma.com/resources/data-sheets/)
2. [ASTM D3518/D3518M, ±45° laminate in-plane shear response](https://www.astm.org/d3518_d3518m-18.html)
