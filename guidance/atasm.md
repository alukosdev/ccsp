---
categories: [Threat Models]
icon: zap
---

!!!danger
This page is currently under revision.
!!!

# ATASM

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| ATASM | Architecture, Threats, Attack Surfaces, and Mitigations |

## Overview

<span id="rev1"></span>Architecture, Threats, Attack Surfaces, and Mitigations (ATASM) is a threat-modeling approach that highlights the importance of structural understanding of a system for the purpose of threat modeling (architecture). The architecture is broken apart into its logical and functional components (decomposing and factoring) to discover all potential attackable surfaces (inputs and outputs of the system). Decomposition is also used to define those points at which defenses will be built (mitigations are placed at defensible boundaries).[[¹]](#ref1)

## References

1. <span id="ref1"></span>[⌃](#rev1) SAFECode. (2017). *Tactical Threat Modeling*. https://safecode.org/wp-content/uploads/2017/05/SAFECode_TM_Whitepaper.pdf