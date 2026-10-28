# Mathematical and Cross-Reference Audit — Pass 2: Wave and Spectral Suite

**Status:** review findings only; no changes to historical plates. **Predecessor:** `Mathematical_Cross_Reference_Audit_Pass_1.md` (PR #14).  
**Scope:** Tier I wave (early and later versions), resonance, interference, superposition, harmonic spectrum, dispersion, Green's function, and fundamental kernel.  
**Severity:** P1 = equation or claimed mathematical implication requires correction/assumptions; P2 = substantial definition or cross-reference ambiguity; P3 = interpretive/editorial clarification.

## Findings

### W01 — Exponential envelopes are not solutions of the undamped wave equation [P1]
**Sources:** `Renewal_Wave_Equation_v1.0.696.md` §§II, IV; `Renewal_Resonance_Equation.md` §§II, VI.

The wave equation `∂²_tρ=c_R²∇²ρ` admits plane waves satisfying `ω²=c_R²k²`. In general, `e^{±γt}sin(kx−ωt)` with nonzero γ is **not** a solution: the second time derivative introduces extra real and quadrature terms. A damping/gain operator and compatible dispersion relation are required. Likewise, resonance in a driven undamped linear oscillator yields secular growth at exact resonance, not generically `A₀e^{γt}`. Exponential growth can arise in other explicitly modeled systems, e.g., parametric instabilities or gain.

**Recommendation:** keep the original models as conceptual stages; specify a modified damped/driven/gain equation before treating the exponential examples as solutions.

### W02 — The metric for spacetime wave propagation is not yet specified [P1]
**Sources:** `Renewal_Wave_Equation_Stability_Threshold.md` §II, `Renewal_Field_Metric_g_R.md` §§II, VII–VIII, `Renewal_Dispersion_Relation.md` §II.

The later wave plate defines `□ᴿρ=gᴿ^{μν}∇_μ∇_νρ`. For a hyperbolic wave operator, the spacetime principal symbol must have a suitable Lorentzian signature; the 14-component Renewal-state metric from the earlier plate is not automatically a spacetime metric. The former also prescribes mixed-sign weights while calling the state metric positive-definite (M07). The dispersion relation `gᴿ^{μν}k_μk_ν=−Ω²` needs a declared signature and an identified spacetime metric.

**Recommendation:** distinguish a state-space alignment bilinear form from a spacetime propagation metric; specify signatures, coordinates, and the relation between them.

### W03 — Source-driven waves do not automatically provide damping or stability [P2]
**Sources:** `Renewal_Wave_Equation_Stability_Threshold.md` §§II–III; `Renewal_Source_Term_Sᴿ.md` §II.

`□ᴿρ=Sᴿ` includes a source but no explicit dissipative term. Curvature coupling does not, by itself, prevent runaway forcing or prove decay. The source's dependence on other operators and potentially on ρ needs to be specified before stability follows.

**Recommendation:** identify energy estimates, boundary conditions, and dissipative/coupling terms where stability is asserted.

### W04 — Resonance equations are not a complete eigenvalue problem [P1]
**Sources:** `Renewal_Resonance_Condition_Ωᴿ.md` §II; `Renewal_Harmonic_Spectrum_Σᴿ.md` §II; `Renewal_Resonance_Equation.md` §§II–V.

The condition `□ᴿρ+Ω²ρ=0` does not by itself define a discrete spectrum of temporal frequencies. A spatial operator, domain, boundary conditions, and function space are needed; `Ω²=−□ᴿρ/ρ` is undefined at nodes and is not a generally constant eigenvalue. The early resonance plate's `ω=nω₀` is valid for some harmonic families, not a universal resonance condition. Its `k=nπ/L` requires a specified one-dimensional boundary-value problem (e.g., Dirichlet endpoints).

**Recommendation:** separate (a) natural frequencies, (b) external driving frequencies, and (c) eigenvalues of a spatial boundary-value problem.

### W05 — Dispersion relation requires an explicit mass/response term [P1]
**Sources:** `Renewal_Dispersion_Relation.md` §II; both Renewal Wave Equation plates.

The dispersion `ω²=c²|k|²+Ω²` is consistent with a Klein–Gordon-like equation `∂²_tρ−c²∇²ρ+Ω²ρ=0` (under conventional signs). It is **not** the dispersion of the earlier free wave equation `∂²_tρ=c²∇²ρ` when Ω≠0. The later sourced equation does not specify this term either. Calling Ω a resonance frequency does not automatically make it a mass-like dispersion parameter.

**Recommendation:** define the exact differential operator for which the dispersion relation is derived, including the sign convention.

### W06 — Green's function needs operator, geometry, and initial/boundary data [P2]
**Source:** `Renewal_Greens_Function_𝒢ᴿ.md` §§II–III.

`□ᴿG(x,x')=δᴿ(x,x')` does not uniquely select retarded, advanced, or other Green's functions. Causal support, initial/boundary conditions, distribution normalization, and the spacetime volume measure must be specified. The integral `ρ(x)=∫G(x,x')S(x')dV'` supplies a particular solution; the general solution also includes a homogeneous solution (or initial-data contributions). Calling the integral a *convolution* requires translation invariance, which curved geometry generally lacks.

**Recommendation:** define the retarded response and include the homogeneous/initial-data term where applicable.

### W07 — Fundamental kernel is not yet distinguished from Green's function [P1]
**Sources:** `Renewal_Greens_Function_𝒢ᴿ.md` §II; `Renewal_Fundamental_Kernel_𝒦ᴿ.md` §§II–III.

Both plates use `ρ(x)=∫[G or K](x,x')S(x')dV'`. The claimed `K=Π·G·Σ` multiplies a projector, Green's function, and **a spectrum (set of frequencies)** without defining a compatible composition. The mode expansion `Σ_n G(x,x';Ω_n)φ_n(x)φ_n(x')` also needs mode normalization, complex conjugation where relevant, spectral weights, and avoidance of double-counting if G already contains modal sums.

**Recommendation:** define K as a precise composed operator (e.g., projected causal Green operator restricted to a selected spectral subspace), specifying domains, measures, and normalizations. This would give the Kernel a genuinely distinct mathematical role.

### W08 — Linear superposition does not follow for every field component [P2]
**Sources:** `Renewal_Interference_Equation.md` §§II, V, VIII; `Renewal_Superposition_Operator_Law.md` §§II–III; `Renewal_Field_Unification_Equation_𝓕_R.md` §§IV, VI.

Divergence, curl, and Laplacian are linear on suitable common domains. However, derived quantities such as energy, nonlinear coupling terms, state-dependent metrics, and velocity from ratios of currents/densities are **not generally additive**. Superposition of solutions requires a linear evolution operator and compatible homogeneous boundary conditions. The interference envelope formula is correct for two sinusoids of the same k and ω, but the stated envelope is constant in x,t in that case; spatial beats require differing frequencies/wavevectors.

**Recommendation:** explicitly label the linearized/independent-source regime, and separate additive primitive fields from nonlinear observables.

### W09 — Distinguish harmonic resonance from guaranteed exponential growth [P2]
**Sources:** `Renewal_Resonance_Equation.md` §§II, IV, VI–VII.

The assertions `ω=nω₀`, exponential gain, and a universal threshold `E_drive≥E_threshold` are not consequences of one common oscillator model without additional dynamics. Linear driven resonance, nonlinear threshold response, and self-excited/parametric growth should be treated as different cases.

**Recommendation:** specify which model supports each phenomenon and what physical or conceptual quantity is measured.

## Verified structural relationships

**Conceptually supported:** Wave → Source → Resonance → Spectrum → Dispersion → Green's Function → Kernel. The early wave/resonance/interference/superposition plates provide historical precursors.

**Formal dependencies not yet established:** state metric ↔ spacetime metric; sourced wave ↔ mass-like dispersion; resonance condition ↔ discrete spectral decomposition; Green's function ↔ kernel; unrestricted superposition ↔ nonlinear coupled field evolution.

## Cross-pass dependency priorities

1. **M07 + W02:** state metric versus spacetime propagation geometry.
2. **M09 + W07:** genuine projector and well-typed kernel composition.
3. **M03–M05 + W03:** continuity, source, and wave compatibility.
4. **W04–W06:** choose a well-posed spectral/initial-boundary-value problem.
5. **M06 + W08:** define component types and the domain of linear superposition.

## Next pass

Tier II: Interaction Tensor, Lagrangian, Coupling Coefficients, Interaction Field Equations, Interference/Coherence Maps, Multisystem Dynamics. Verify action, variation, source/field dimensions, conservation transfer, and boundary conditions before making claims about multi-system validity.

**Editorial policy:** no edits to original plates; these findings are proposed mathematical clarifications, not a rejection of philosophical analogies or a declaration of empirical validation.
