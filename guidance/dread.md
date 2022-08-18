---
categories: [Threat Models]
---

# DREAD

## Acronyms, Abbreviations, and Initialisms

| Short Form | Full Form |
| - | - |
| DREAD | Damage, Reproducibility, Exploitability, Affected Users, and Discoverability |

## Overview

### Introduction

DREAD is an acronym that describes five criteria for assessing threats to software.

!!!
DREAD was developed by Microsoft.
!!!

## Categories

The DREAD acronym stands for:

- **D**amage
- **R**eproducibility
- **E**xploitability
- **A**ffected users
- **D**iscoverability

To prioritize the threats to your driver, rank each threat from 1 to 10 on all 5 of the DREAD assessment criteria, and then add the scores and divide by 5 (the number of criteria). The result is a numeric score between 1 and 10 for each threat. High scores indicate serious threats.

```
RISK_DREAD = (Damage + Reproducibility + Exploitability + Affected Users + Discoverability) / 5
```

### [D]amage

Assessing the damage that could result from a security attack is obviously a critical part of threat modeling. Damage can include data loss, hardware or media failure, substandard performance, or any similar measure that applies to your device and its operating environment.

### [R]eproducibility

Reproducibility is a measure of how often a specified type of attack will succeed. An easily reproducible threat is more likely to be exploited than a vulnerability that occurs rarely or unpredictable. For example, threats to features that are installed by default, or are used in every potential code path, are highly reproducible.

### [E]xploitability

Exploitability assesses the effort and expertise that are required to mount an attack. A threat that can be attacked by a relatively inexperienced college student is highly exploitable. An attack that requires highly skilled personnel and is expensive to carry out is less exploitable.

In assessing exploitability, consider also the number of potential attackers. A threat that can be exploited by any remote, anonymous user is more exploitable than one that requires an onsite, highly authorized user.

### [A]ffected Users

The number of users that could be affected by an attack is another important factor in assessing a threat. An attack that could affect at most one or two users would rate relatively low on this measure. Conversely, a denial-of-service attack that crashes a network server could affect thousands of users and therefore would rate much higher.

### [D]iscoverability

Discoverability is the likelihood that a threat will be exploited. Discoverability is difficult to estimate accurately. The safest approach is to assume that any vulnerability will eventually be taken advantage of and, consequently, to rely on the other measures to establish the relative ranking of the threat.

## Sources

!!!danger
I need to add formatting for referencing websites here.
!!!

- https://cloudsecurityalliance.org/download/artifacts/top-threats-to-cloud-computing-pandemic-eleven