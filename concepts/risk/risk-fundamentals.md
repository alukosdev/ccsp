# Risk Fundamentals

## Quick Reference

==- Risk Modeling
Risk modeling is based on an asset or a threat.
==- Risk Register
A risk register is a table to consolidate information about risks.
==-

## Risk Identification

`Risk = Asset * Threat * Vulnerability` (in some cases, the asset is excluded from the calcuation and shouldn't be)

What the above calculation displays is that if there is no threat, no there is no vulnerability. Likewise, if there is no vulnerability, there is no risk. Finally, if the asset has no value, there is also no risk.

## Risk Controls

### Administrative

Administrative controls are those processes and activities that provide some aspect of security.

!!!
Examples include personnel background checks, scheduled routine log reviews, mandatory vacations, robust and comprehensive security policies and procedures, and deciding business processes so that there are no single points of failure and so that proper separation of duties exists.
!!!

### Technical

Technical (logical) controls, are those controls that enhance some facets of the CIA triad, usually operating within a system, often in electronic fashion.

!!!
Technical controls include encryption mechanisms, access control lists to limit user permissions, and audit trails and logs of system activity.
!!!

### Physical

Physical controls are controls that limit physical access to assets or that operate in a manner that reduces the impact of a physical event.''

!!!
Examples include locks on doors, fire suppression equipment in datacenters, fences, and guards.
!!!

### Compensating

Controls to catch the failure of a first control.

- Intent and rigor of the original equipment
- Provide a similar level of defense as the original requirement
- Be above and beyond other requirements
- Be commensurate with the additional risk imposed by not adhering to the requirement

## Risk Response

Organizations have four primary ways to address risk (rejection is not a valid method for addressing risk), all of which should take into effect the cost-benefit analysis (the potential cost should not outweigh the benefit). For example, we do not put a $10 lock on a $5 bicycle.

### Avoidance

Leaving a business opportunity because the risk is simply too high and cannot be compensated for with adequate control mechanisms-a risk that exceeds the organization's appetite.

!!!
Risk avoidance is the only surefire method for eliminating a specific risk.
!!!

### Acceptance

The opposite of avoidance; the risk falls within the organization's risk appetite, so the organization continues operations without any additional efforts regarding the risk.

The only reason organizations accept any level of risk is because of the potential benefit also afforded by a risky activity. Risk is often balanced by corresponding *opportunity*.

!!!
If the risk of the activity is estimated to be within the organization's risk appetite, then the organization might choose risk acceptance.
!!!

### Transference

The organization pays someone else to accept the risk, at a lower cost than the potential impact that would result from the risk being realized; this is usually in the form of insurance. This type of risk is often associated with things that have a low probability of occurring but a high impact should they occur.

This typically takes the form of insurance, but contracts and SLAs are another method of transferring risk.

### Mitigation

The organization takes steps to decrease the likelihood or the impact of the risk (and often both); this can take the form of controls/countermeasures, and is usually where security practitioners are involved.

When we choose to mitigate risk by applying countermeasures and controls, the remaining, leftover risk is called residual risk. The task of the security program is to reduce residual risk until it falls within the acceptable level of risk according to the organization's risk appetite.

### Rejection

Risk rejection isn't a legitimate form of risk response. Rejection involves ignoring risks and continuing with operations. This is essentially the same thing as accepting a risk without mitigating it to a tolerable level. In most cases, this would indicate failure of due diligence and may put the organization in a position of liability.

## Risk Types

==- Policy and Organization Risk
- Provider lock-in
- Loss of governance
- Compliance risks
- Provider exit (vendor lock-out)
==- General Risks
- Impact of SPOF
- Increased need for technical skills
- Provider assumes more control over technical risks (loss of governance)
==- Virtualization Risks
- Guest breakout
- Snapshot and image security
- Sprawl
==- Cloud-Specific Risks
- Management plane breach
- Resource exhaustion
- Isolation control failure
- Insecure or incomplete data deletion
- Control conflict risk
- Software-related risks
==- Legal Risks
- Data protection
- Jurisdiction
- Law enforcement
- Licensing
==- Non-Cloud-Specific Risks
- Natural disasters
- Unauthorized access
- Social engineering
- Default passwords
- Network attacks
==-
