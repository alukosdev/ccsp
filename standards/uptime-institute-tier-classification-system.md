---
categories: [Standards, Data Center Design Standards]
---

# Uptime Institute Tier Classification System

## Overview

The Tier Classification System designed by Uptime Institute is the globally recognized standard for data center reliability and overall performance. It allows for various levels of performance to be chosen based on the intended applications and business parameters associated with those applications.

## Tier Levels

The data center classifications are divided into four Tiers that match a particular business function and define criteria for maintenance, power, cooling and fault capabilities. The Tiers are progressive, so each Tier incorporates the requirements of the lower Tiers. This progression does not mean that a Tier IV data center is better than a Tier II - it means that these levels fit differing business operations. The definitions and benefits of the Tiers are set in our topology standard and focus on the data center infrastructure.

The data center Tier definitions define criteria, but not specific technology options or design choices to meet the Tier. Tiers are flexible enough to allow for many solutions that meet performance goals and compliance regulations. Many solutions lead to engineering innovation and uniqueness across data centers. Each data center can decide the best way to meet the Tier criteria and business goals.

The data center Tier levels are:

- [Tier I: Basic Capacity Level](#tier-i-basic-capacity-level)
- [Tier II: Redundant Capacity Components](#tier-ii-redundant-capacity-components)
- [Tier III: Concurrently Maintainable](#tier-iii-concurrently-maintainable)
- [Tier IV: Fault-Tolerant](#tier-iv-fault-tolerant)

==- Tier I: Basic Capacity

A Tier I data center is the basic capacity level with infrastructure to support information technology for an office setting and beyond. The requirements for a Tier I facility include:

- An uninterruptible power supply (UPS) for power sags, outages, and spikes.
- An area for IT systems.
- Dedicated cooling equipment that runs outside office hours.
- An engine generator for power outages.
- Tier I protects against disruptions from human error, but not unexpected failure or outage. Redundant equipment includes chillers, pumps, UPS modules, and engine generators. The facility will have to shut down completely for preventive maintenance and repairs, and failure to do so increases the risk of unplanned disruptions and severe consequences from system failure.

==- Tier II: Redundant Capacity

Tier II facilities cover redundant capacity components for power and cooling that provide better maintenance opportunities and safety against disruptions. These components include:

- Engine generators.
- Energy storage.
- Chillers.
- Cooling units.
- UPS modules.
- Pumps.
- Heat rejection equipment.
- Fuel tanks.
- Fuel cells.
- The distribution path of Tier II serves a critical environment, and the components can be removed without shutting it down. Like a Tier I facility, unexpected shutdown of a Tier II data center will affect the system.

==- Tier III: Concurrently Maintainable

A Tier III data center is concurrently maintainable with redundant components as a key differentiator, with redundant distribution paths to serve the critical environment. Unlike Tier I and Tier II, these facilities require no shutdowns when equipment needs maintenance or replacement. The components of Tier III are added to Tier II components so that any part can be shut down without impacting IT operation.

==- Tier IV: Fault-Tolerant

A Tier IV data center has several independent and physically isolated systems that act as redundant capacity components and distribution paths. The separation is necessary to prevent an event from compromising both systems. The environment will not be affected by a disruption from planned and unplanned events. However, if the redundant components or distribution paths are shut down for maintenance, the environment may experience a higher risk of disruption if a failure occurs.

Tier IV facilities add fault tolerance to the Tier III topology. When a piece of equipment fails, or there is an interruption in the distribution path, IT operations will not be affected. All of the IT equipment must have a fault-tolerant power design to be compatible. Tier IV data centers also require continuous cooling to make the environment stable.

==-

Parameters | Tier I | Tier II | Tier III | Tier IV
:--- | :--- | :--- | :--- | :---
**Uptime guarantee** | 99.671% | 99.741% | 99.982% | 99.995%
**Downtime per year** | <28.8 hours | <22 hours | <1.6 hours | <26.3 minutes
**Component redundancy** | None | Partial power and cooling (partial N+1) | Full N+1 | Fault-tolerant (2N or 2N+1)
**Concurrently maintainable** | No | No | Partially | Yes
**Price** | $ | $$ | $$$ | $$$$
**Staffing** | None | 1 shift | 1+ shift | 24/7/365

## Noteworthy

- [x] Tier I is known as `Basic Capacity`.
- [x] Tier II is known as `Redundant Capacity`.
- [x] Tier III is known as `Concurrently Maintainable`.
- [x] Tier IV is known as `Fault-Tolerant`.

## Sources

- https://uptimeinstitute.com/tier-certification
- https://uptimeinstitute.com/tiers
- https://phoenixnap.com/blog/data-center-tiers-classification