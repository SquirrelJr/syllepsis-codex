# Mathematical and Cross-Reference Audit — Pass 1

**Status:** audit findings, not amendments to the original plates. **Baseline:** main after merge of Recursive Architecture Concordance (2026-10-28).  
**Method:** compare displayed equations with their accompanying prose, prerequisite definitions, and standard mathematical meanings. **Severity:** P1 = definition or claimed consequence fails without additional assumptions; P2 = significant ambiguity or cross-plate mismatch; P3 = editorial clarification.  
**Scope of this pass:** Phi recurrence, Order–Reflection notation, Renewal conservation/current/source, unified field and metric/connection/curvature/cotensor/projection. Other plates remain to be verified. This audit does not assert experimental validation of the Codex's moral or spiritual analogies.

## Findings

### M01 — Phi recurrence and stability [P1]
**Source:** `Codex/Plates/01_Tier_I/Phi_Recursive_Identity.md`, §§III–IV.

The stated recurrence is
```math
R_{n+1}=\phi R_n-R_{n-1}.
```
Its characteristic polynomial is `λ² − φλ + 1`. Because `0 < φ < 2`, its roots are complex conjugates of unit modulus. Thus solutions are bounded oscillations for finite initial conditions, **not generically exponentially growing**. This is compatible with a bounded-recursion interpretation but does not prove the plate's broader claims about universal stable expansion or destructive-interference minimization. The explanatory list also mentions `R_{n-2}`, which is not present in the displayed recurrence. The spiral `r(θ)=ae^{bθ}`, `b=ln φ`, grows by a factor φ **per unit of θ**; it does not follow from the displayed second-order recurrence.

**Recommended action:** retain original text; add a later author's mathematical note distinguishing (a) bounded recurrence, (b) exponential spiral, and (c) metaphorical analogy, with a worked solution and a specified mapping between them if one is intended.

### M02 — Reflection/Renewal symbol collision [P2]
**Sources:** `Order_Reflection_Reconstitution_Law_OR.md`, `Renewal_Source_Term_Sᴿ.md`, and `Renewal_Field_Unification_Equation_𝓕_R.md`.

The Order–Reflection Reconstitution Law calls Reflection the `R`-Operator and writes `O+R`. The Source Term likewise uses `Rᴿ` for Reflection. Other plates use `R` as Renewal and `Θ` as Reflection. `O+R` is therefore not safely composable across plates without a scoped symbol dictionary.

**Recommended action:** add a notation crosswalk, distinguishing historical local notation from canonical operator identity. Do not silently substitute `Θ` into historic equations.

### M03 — Divergence-free vs temporal conservation [P1]
**Sources:** `Renewal_Conservation_Law.md` §§III–IV, `Renewal_Continuity_Equation.md` §II, `Renewal_Field_Unification_Equation_𝓕_R.md` §VII.

`∇·J_R=0` and `∂ₜρ_R+∇·J_R=0` are **not generally equivalent**. Under both equations simultaneously, `∂ₜρ_R=0`. A time-varying density in a closed system normally has nonzero local divergence while its spatial integral is conserved under no-flux boundary conditions.

**Recommended action:** label divergence-free flow as a special steady-density case, and temporal continuity as the general local conservation law. State boundary conditions before claiming global conservation.

### M04 — Current has two definitions [P2]
**Sources:** `Renewal_Conservation_Law.md` §II and `Renewal_Current_𝒥ᴿ.md` §II.

The former uses `J_R=ρ_R V_R`; the latter uses `𝒥ᴿ=Πᴿ(∇ᴿ𝓕ᴿ)`. The latter has tensor/type questions: the covariant derivative of a 14-component state is generally a covector-valued state, while `ρ_R V_R` is a spatial flux. A projection alone does not specify the contraction or spatial vector extraction needed to identify them.

**Recommended action:** specify the bundle/domain, dimensions, a flux extraction map, and whether the two expressions represent different levels of description.

### M05 — Source term versus conserved density [P2]
**Sources:** `Renewal_Source_Term_Sᴿ.md` §§I–II and `Renewal_Continuity_Equation.md` §II.

The source `Sᴿ` is defined for a **wave equation** `□ᴿρᴿ=Sᴿ`, not automatically as a source in the **continuity equation**. A driven wave equation can coexist with conserved density, but compatibility requires specifying how the wave source relates to current and boundary flux. A `source` in one PDE must not be silently treated as net creation of a conserved quantity in another.

**Recommended action:** explicitly distinguish `S_wave` from `S_cont` (possibly zero), and explain whether the five operator terms generate waves, redistribute density, or create/annihilate the modeled quantity.

### M06 — Unified 14-component object needs type discipline [P2]
**Source:** `Renewal_Field_Unification_Equation_𝓕_R.md` §§II–IV, VIII.

The 14 entries mix scalars, vectors, differential expressions, and operators. This is a legitimate **ordered collection**, but not automatically a vector in a single 14-dimensional inner-product space. Pointwise addition, gradients, contractions, and superposition require component domains and linearity assumptions. `∂ₜ𝓕_R=𝓓_R(𝓕_R)` names an evolution law but does not specify `𝓓_R` sufficiently to establish dynamics.

**Recommended action:** define component spaces, units/normalizations, and operator domains before invoking tensor algebra or superposition.

### M07 — Metric is simultaneously indefinite and positive-definite [P1]
**Source:** `Renewal_Field_Metric_g_R.md` §§II–VIII.

The metric is defined as a weighted bilinear form `g_R(a,b)=Σw_i a_i b_i`. §VII requires `w_D,w_Χ<0`, while §VIII requires positive-definiteness. A diagonal form with negative weights is **indefinite**, not positive-definite. In that case `√g_R(v,v)` can be non-real, and `√g_R(a-b,a-b)` is not a general metric distance. Even with positive weights, the displayed fixed-coefficient form is a flat constant metric in the corresponding coordinates unless state dependence or geometry is additionally specified.

**Recommended action:** choose whether the intended construct is (a) a positive-definite metric with a separate signed moral/coherence functional, or (b) an indefinite pseudo-Riemannian form with appropriate causal/signature conventions. Do not claim both simultaneously.

### M08 — Geodesic and curvature definitions need consistency [P1]
**Sources:** `Renewal_Field_Metric_g_R.md` §§V–VI; `Renewal_Connection_Coefficients_Γ_R.md` §§II, IV, VII; `Renewal_Curvature_Tensor_ℛ_R_v1.0.710.md` §§II–IV.

The metric plate's `∂²γ/∂t²+Γ_R(γ)=0` is a schematic geodesic equation; the connection plate supplies the standard velocity-quadratic Christoffel form. The metric plate's scalar `∇·(g_R^{-1}∇g_R)` is **not generally the scalar curvature** defined later by contracting the Riemann/Ricci tensors. The curvature plate's displayed sectional-curvature numerator `ℛ^k_{R,kij}` is a contraction, not the standard evaluation `R(u,v,v,u)` needed for sectional curvature. Index/sign conventions in the Riemann/Ricci formulas should be checked together.

The connection plate says symmetric Christoffel symbols make transport **path-independent locally**. Torsion-freeness alone does not imply path independence: nonzero curvature yields path dependence around loops.

**Recommended action:** designate the connection-derived Riemann/Ricci/scalar construction as the formal geometry; distinguish schematic analogies and state curvature/sign conventions explicitly.

### M09 — Projection is not established as a projector [P1]
**Sources:** `Renewal_Cotensor_Field_𝓒_R_v1.0.712.md` §§II–III; `Renewal_Projection_Operator_Πᴿ.md` §§II–III.

The cotensor is defined as metric lowering, `𝓒_R=g_R𝓕_R`. The projection plate defines `Πᴿ=𝓒ᴿ∘gᴿ`, but metric lowering and its composition do not automatically give an endomorphism `V→V`, much less an idempotent self-adjoint projection. Its claimed `Π²=Π` and self-adjointness require an explicitly defined Renewal-aligned subspace and a compatible projection formula. If `g_R` is indefinite, orthogonal projection also needs extra nondegeneracy assumptions.

**Recommended action:** specify the Renewal-aligned subspace and construct an actual projector (e.g., using a positive-definite inner product and a full-rank basis) before treating the identities as proven.

### M10 — Coordinate-dependent stability thresholds [P2]
**Sources:** `Renewal_Connection_Coefficients_Γ_R.md` §VIII; `Renewal_Curvature_Tensor_ℛ_R_v1.0.710.md` §VIII.

Absolute bounds on individual Christoffel symbols are coordinate-dependent; they are not intrinsic stability criteria. Individual curvature components also depend on basis/coordinates; an invariant norm or specified frame is needed to compare against a scalar threshold. Even bounded curvature does not alone establish dynamical stability without an evolution law.

**Recommended action:** define a coordinate/frame convention or invariant geometric norms, then connect thresholds to a stated dynamical stability result.

## Cross-reference map: core dependency spine

`Unified Field` → `Metric` → `Connection` → `Curvature` → `Cotensor` → `Projection` → `Current` → `Continuity` → `Wave` → `Source`.

This is a **conceptual order** present in the plate introductions, not yet a verified chain of mathematical deductions. M06–M09 are the key prerequisites before later field/interaction theorems can inherit formal validity.

## Interpretation and preservation

The recursive/generational architecture remains a promising **conceptual** bridge: inherited pattern → recognition → alignment → correction → identity-preserving transmission. The equations reviewed here do not establish a quantitative theorem about families or generational outcomes. The correct editorial response is to make the mathematical assumptions explicit, not to erase metaphorical or theological passages.

## Next audit passes

1. Tier I: wave, resonance, dispersion, Green's function, kernel; check operator definitions, PDE boundary conditions, normalization, and claimed solutions.
2. Tiers II–III: verify tensor index structure, Lagrangian variation, coupling dimensions, global conservation and boundary integration.
3. Tiers IV–VI: verify definitions of embodiment, invariants, integration and transmission, including the two Tier VI strands.
4. Tiers VII–XII: verify hypotheses behind claims of fixed points, stability, semantic conservation, attractors, and optimization.
5. Publish an author-reviewed correction ledger; any changes to historic equations should be separately proposed with before/after rationale.

**This audit file is a set of testable review findings, not an assertion that all Codex plates have been verified.**
