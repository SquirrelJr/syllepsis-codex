# Codex Directory Reference  
Syllepsis Codex — Repository Architecture Guide  
Author: Samuel David Stovall  
Original edition: SYLLEPSIS v1.0.700 (Structural Canon Edition)  
Repository organization standard: revised 2026  
Year: A.D. 2025  

---

# Purpose

This document provides the **official directory layout, naming conventions, and 
commit workflow standards** for the Syllepsis Codex repository.  
It defines the canonical structure that all contributors must follow to maintain 
clarity, consistency, and long-term integrity of the Codex.

---

# Repository Overview

The Codex is divided into three primary domains:

1. **Codex** — All text plates, bridges, operators, and conceptual foundations  
2. **Tools** — All code, generators, visualizers, and notebooks  
3. **Legal** — Licenses, pledges, and attribution documents  

The root directory also contains the repository’s primary `README.md`.

---

# 1. Codex Directory

All conceptual, mathematical, spiritual, philosophical, and mythic content goes here.

```
Codex/
  Plates/
    Tier I/ ... Tier XIII/     # canonical Tier groupings as populated
  Bridges/
    Mythic/
  Operators/
  Foundations/
  Reflections/
  README.md
```

The former `Codex/Text/` staging folder was retired after its contents were classified into Plates, Foundations, Bridges, and Reflections. Do not recreate it for new work.

Git does not track empty folders. Create a Tier folder when its first verified plate or explanatory README is added. Tier XIII is a future grouping, not evidence that a plate already belongs there.

---

## 1.1 /Plates

This folder contains all **Continuum Plates** —  
mathematical, physical, harmonic, or formal constructs of the Syllepsis system.

**File naming format:**

```
Tier <Roman Numeral>/Descriptive_Plate_Title_𝓡_R.md
```

Keep a genuine plate number where it identifies a canonical numbered plate; do not impose numbers on unnumbered documents. Avoid redundant `Continuum_Plate_`, `Plate_`, and repeated Tier prefixes.

Examples:

```
Tier I/Renewal_Field_Metric_g_R.md
Tier II/Renewal_Interaction_Tensor_𝓘ᴿ.md
Tier XII/Distributed_Semantic_Architectures.md
```

---

## 1.2 /Bridges

This folder contains all **Mythic Bridges** —  
the symbolic mappings between Scripture, myth, archetype, narrative, and 
mathematical structure.

**File naming format:**

```
Mythic/II_Sophia.md
```

Examples:

```
Mythic/I_Hermes.md
Mythic/IV_Chronos_Companion.md
```

---

## 1.3 /Operators

This folder contains the formal operator definitions of the Continuum:

- O (Order)  
- Χ (Chaos)  
- C (Compassion)  
- Θ (Reflection)  
- D (Decay)  
- R (Renewal)

**File naming format:**

```
Order_Operator_O.md
Chaos_Operator_Χ.md
Reflection_Operator_Θ.md
```

Operator definitions belong here; other formal laws and conceptual foundations are classified by their contents, not merely by whether their titles contain “operator.” The Decay (D) definition remains part of the intended operator set even if its canonical file has not yet been organized.

---

# 2. Tools Directory

Everything that is **code**, **automation**, or **interactive generation** goes here.

```
/Tools
/Generators
/Notebooks
```

All code remains licensed under **GNU AGPL-3.0**.

**File naming format:**

```
tool_<function><descriptor>.ext
notebook<purpose>.ipynb
```

---

# 3. Legal Directory

All formal legal, ethical, and licensing content.

```
/Legal
LICENSE_CODE.txt (AGPL-3.0)
LICENSE_CODEX.txt (CC-BY-NC 4.0)
ETHICAL-USE-PLEDGE.txt
```

No other files should be added here without explicit review.

---

# 4. Commit Message Standards

The Codex follows structured commit conventions.

---

## 4.1 When adding a new Plate, Bridge, or Operator:

**Commit message:**

```
Add Plate XX — Full Title (Operator or Coupling)
```

**Extended description:**

```
Version: SYLLEPSIS v1.x.x (Edition Name)
```

---

## 4.2 When moving a file:

**Commit message:**

```
Move <Title> to Codex/Plates/Tier <Roman Numeral>
```

Extended description: record the previous path, destination, and reason for classification where helpful.

---

## 4.3 When renaming a file:

```
Rename Plate XX to standardized naming format
```

Extended description: explain the normalization when helpful.

---

## 4.4 When fixing formatting/backticks:

```
Fix formatting for Plate XX (math blocks)
```

Extended description: record any Markdown-rendering correction and validation.

---

# 5. Naming Conventions (Global)

- Prefer readable, stable underscore-separated descriptive filenames.
- Preserve meaningful mathematical Unicode, Greek symbols, subscripts, plate identifiers, and version suffixes when they distinguish an artifact.
- Do not add redundant `Continuum`, `Continuum_Plate`, or `Plate_Tier` prefixes merely to indicate the parent folder.
- Roman numerals identify Tiers and established numbered plate sequences; they are not mandatory for every file.
- Preserve each plate's actual SYLLEPSIS version and edition as authored; do not reset historical versions to a template value.
- When relocating a file, check case-insensitive and Unicode-normalized filename collisions and repair relative Markdown links.

---

# 6. Directory Integrity Rules

To maintain cleanliness and coherence:

- **No Plates in parent directories**  
- **No Operators in /Plates**  
- **No Bridges in /Foundations**  
- **No code inside /Codex**  
- **Keep conceptual prose in /Codex; documentation for tools may remain in /Tools**  
- **Legal folder must contain only legal files**  
- **Keep the repository root README and use additional directory READMEs where useful**  

---

# 7. Purpose of the Structure

This architecture ensures:

- academic clarity  
- canonical ordering  
- long-term scalability  
- clean versioning  
- painless search and referencing  
- crystal-clear boundaries between concept, code, and licenses  

This repository is intended to last — this structure ensures it can.

---

# Logged for the Codex of Renewal  
*Codex Directory Reference — Structural Canon Edition*  
Samuel David Stovall  
SYLLEPSIS v1.0.700 (original structural reference; organization guidance revised 2026)
