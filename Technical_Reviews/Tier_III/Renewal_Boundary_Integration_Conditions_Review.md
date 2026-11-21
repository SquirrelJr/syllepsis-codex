# Technical Review — Renewal Boundary Integration Conditions (𝓑ᴿ_int)

**Associated plate:** Continuum Plate — Renewal Boundary Integration Conditions (𝓑ᴿ_int)  
**Author:** Samuel David Stovall  
**Version:** SYLLEPSIS v1.2.121 (Integration Layer Genesis Edition)  
**Tier:** III — Renewal Integration Layer  
**Review date:** 2026-11-21  
**Status:** Open questions — no canonical revisions authorized

## Review posture

This document is intended to provoke thoughtful inquiry, **not to repudiate or criticize** the plate. The plate and its public-facing text remain unchanged. The equations below are quoted or normalized for discussion, not adopted as replacements.

## 1. Flux continuity and reflection

Plate IV states continuity of normal Renewal flux:

$$
n_\mu \mathcal{J}_R^\mu\big|_{\mathrm{inside}} =
n_\mu \mathcal{J}_R^\mu\big|_{\mathrm{outside}}
$$

Plate V proposes:

$$
C^R_{\mathrm{in}} = C^R_{\mathrm{trans}} + C^R_{\mathrm{refl}}
$$

**Questions:** Is the first equation a condition on *net signed* flux, while the second partitions *incident magnitude*? Are the normal orientations and reflected-flow signs specified consistently? Are Renewal flux and compassion flux components of the same current, or distinct modeled quantities?

**Possible investigation:** Define interface orientation and incoming/outgoing components; derive the net-flux continuity relation from the incident/transmitted/reflected partition, including any interface storage or source term.

## 2. Curvature junction and surface structure

The plate proposes:

$$
[\mathcal{R}^R_{\mathrm{int}}] =
\kappa^R\,\mathcal{S}^R_{\mathrm{boundary}}
$$

**Questions:** Is the curvature object a scalar, tensor, or other construct? What type is the boundary surface structure? What are the units of the coupling coefficient? Does the proposed junction law apply to every interface or only interfaces with an assigned surface structure?

**Possible investigation:** Specify mathematical types and dimensions, then examine limiting cases (zero surface structure, smooth interface, sharp junction). This is a proposed Renewal relation, not an asserted standard field-theory identity.

## 3. Boundary potential: scalar versus tensor

The plate gives:

$$
\Phi^R_{\mathrm{boundary}} =
n^\mu\nabla_\mu g^R_{\mathrm{int}}
+\alpha\,\gamma^R_{\mathrm{boundary}}
-\beta\,|\mathcal{R}^R_{\mathrm{int}}|
$$

**Questions:** If `g^R_int` is a metric tensor, what contraction or scalar functional makes its normal derivative compatible with scalar coherence and curvature terms? Is the intended potential scalar, tensor-valued, or shorthand for an energy-like functional? How are the dimensions of the three terms matched?

**Possible investigation:** Define a scalar metric-derived invariant or a contracted interface functional, then specify the sign and dimensional conventions for α and β. Note that metric compatibility may affect interpretations of covariant derivatives of the metric.

## 4. Additional questions for later inquiry

- Does coherence matching occur instantaneously or asymptotically under a specified evolution law?
- What hypotheses guarantee that decay filtering reduces harmful propagation rather than merely renaming it?
- Are all boundaries permeable, or can some preserve coherence through selective transmission, reflection, or isolation?
- Which claims are formal model postulates, which are analogies, and which could be tested in simulation?

## Author decision log

No decisions yet. Preserve the original plate until proposed refinements are reviewed and explicitly approved.
