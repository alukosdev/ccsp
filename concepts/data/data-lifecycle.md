# Data Lifecycle

## Quick Reference

| Acronym | Backronym |
| - | - |
| DLP | Data Loss Prevention |
| DRM | Digital Rights Management |
| IRM | Information Rights Management |

## Summary

Being able to destroy data, or render it inaccessible, in the cloud is critical to ensuring confidentiality and managing a secure lifecycle for data.

1. Map the different lifecycle phases.
2. Integrate the different data locations and access types.
3. Map these into functions, actors, and controls.

## Functions, Actors, and Controls

### Functions

=== Access/Read
View/read the data, including creating, copying, file transfers, dissemination, and other exchanges of information.
=== Process
Perform a transaction on the data; update it; use it in a business processing transaction, etc. This would *not* include viewing, since that is a component of accessing/reading.
=== Store
Hold the data (in a file, database, etc.).
===

![Information Lifecycle Phases](/static/information-lifecycle-phases.png)

### Controls

Controls act as a mechanism to restrict a list of possible actions to allowed or permitted actions. These controls can be of a preventative, detective (monitoring), or corrective nature.

To determine the necessary controls to be deployed, you must first understand the:

- Functions of the data
- Locations of the data
- Actors upon the data

![Mapping the Lifecycle](/static/mapping-the-lifecycle.png)

## Phases

==- Create/Update
==- Store
==- Use
==- Share
==- Archive
==- Destroy
==-
