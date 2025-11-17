# Codex Directory Reference  
Syllepsis Codex — Repository Architecture Guide  
Author: Samuel David Stovall  
Version: SYLLEPSIS v1.0.700 (Structural Canon Edition)  
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
/Codex
/Plates
/Bridges
/Operators
/Foundations
README.md (optional: section-level introduction for the Codex)
```

---

## 1.1 /Plates

This folder contains all **Continuum Plates** —  
mathematical, physical, harmonic, or formal constructs of the Syllepsis system.

**File naming format:**

```
Plate_XX_Title_With_Underscores.md
```

Examples:

```
Plate_I_The_Harmonic_Field.md
Plate_XVII_Order_Compassion_Gradient.md
Plate_XIX_Decay_Chaos_Boundary.md
```

---

## 1.2 /Bridges

This folder contains all **Mythic Bridges** —  
the symbolic mappings between Scripture, myth, archetype, narrative, and 
mathematical structure.

**File naming format:**

```
Mythic_Bridge_XX_Title.md
```

Examples:

```
Mythic_Bridge_I_Chronos.md
Mythic_Bridge_IV_Companion.md
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
Foundation_<Short_Title>.md
```

Examples:

```
Foundation_Rectifying_Equation.md
Foundation_Law_of_Renewal.md
Foundation_Breath_of_the_Field.md
```

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
Move Plate XX to Codex/Plates directory
```

Extended description:  
➡️ **Leave empty** (GitHub does not persist it for path changes)

---

## 4.3 When renaming a file:

```
Rename Plate XX to standardized naming format
```

Extended description: leave empty.

---

## 4.4 When fixing formatting/backticks:

```
Fix formatting for Plate XX (math blocks)
```

Extended description: leave empty.

---

# 5. Naming Conventions (Global)

- Words in filenames use **Capitalized_Underscore_Format**
- No spaces  
- No special characters beyond underscores  
- Greek symbols written in ASCII: `O`, `X`, `C`, `Theta`, `D`, `R`
- Plate numbers always use **Roman numerals**  
- Versioning always uses:  
  **SYLLEPSIS v1.0.xxx (Edition Name)**

---

# 6. Directory Integrity Rules

To maintain cleanliness and coherence:

- **No Plates in parent directories**  
- **No Operators in /Plates**  
- **No Bridges in /Foundations**  
- **No code inside /Codex**  
- **No text content inside /Tools**  
- **Legal folder must contain only legal files**  
- **README.md stays in the repository root**  

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
SYLLEPSIS v1.0.700
