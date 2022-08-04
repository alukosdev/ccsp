---
categories: [Threat Models]
---

# DREAD

## Overview

DREAD is part of a system for risk-assessing computer security threats previously used at Microsoft and although currently used by OpenStack and other corporations it was abandoned by its creators. It provides a mnemonic for risk rating security threats using five categories.

The categories are:

- Damage
- Reproducibility
- Exploitability
- Affected users
- Discoverability

When a given threat is assessed using DREAD, each category is given a rating from 1 to 10. The sum of all ratings for a given issue can be used to prioritize among different issues.

```RISK_DREAD = (Damage + Reproducibility + Exploitability + Affected Users + Discoverability) / 10```

## Categories

### [D]amage

### [R]eproducibility

Reproducibility is the measure of how easy an exploit is to reproduce.

### [E]xploitability

### [A]ffected Users

### [D]iscoverability
