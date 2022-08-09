# Risk Management

## Summary

Every decision we make should be based on risk. Risk management in the cloud is based on the *shared responsibilities* model.

NIST 800-30 recommends a risk management process containing the following four components:

1. Risk Framing
2. Risk Assessment
3. Risk Response
4. Risk Monitoring

## Risk Framing

Addresses how organizations describe the environment in which risk-based decisions are made. Refers to determine what risk and levels are to be evaluated.

Risk framing is designed to produce a risk-management strategy intended to address how organizations assess, respond to, and monitor risk. This allows the organization to clearly articulate the risks that it needs to manage, and it establishes the boundaries for risk-based decisions within organizations.

## Risk Assessment

Risk assessment is the process used to identify, estimate, and prioritize information security risks. It is the process of determining risks that could potentially prevent the program, enterprise, or investment from achieving its objectives. It includes documenting and communicating the concern.

Risks must be communicated in a way that is clear and easy to understand. It may also be important to communicate risk information outside the organization. To be successful in this, the organization must agree to a set of risk-management metrics.

Risk is determined as the by-product of likelihood and impact. For example, if an exploit has a likelihood of 1 (high) and an impact of 100 (high), the risk would be 100. As a result, 100 would be the highest exploit ranking available.

!!!
No countermeasure should be greater in cost than the risk it mitigates, transfers, or avoids.
!!!

The purpose of engaging in risk assessment is to identify:

- Threats to organizations (i.e., operations, assets, or individuals) or threats directed through organizations against other organizations.
- Vulnerabilities internal and external to organizations.
- The harm (i.e., adverse impact) that may occur given the potential for threats exploiting vulnerabilities.
- The likelihood that harm will occur.

`Risk = Asset + Threat + Vulnerability`

- If there is no threat, there is no vulnerability.
- If there is no vulnerability, there is no risk.
- If the asset has no value, there is no risk.

!!!
In some cases, the asset is excluded from the risk calculation. The asset should always be included in the calculation because you do not want to spend more money than the asset is worth to protect it.
!!!

There are additional cloud-specific risk concerns that should also be considered:

- Risk of service failure and associated impact
- Insider threat risk impact
- Risk of compromised customer to other tenants in the cloud environment
- Risk of DoS attacks
- Supply chain risk to the CSP

Identifying these factors helps to determine risk, which includes the likelihood of harm occurring and the potential degree of harm. Using a risk scorecard is recommended. The impact (consequence) and probability (likelihood) of each risk are assessed separately, and then the results are combined.

![Risk Ranking](/static/risk-ranking.png)

Threat categories:

- Human
- Natural
- Technical
- Physical
- Environmental
- Operational

!!!
Risk assessments should be performed *periodically*.
!!!

### Qualititative Risk Assessments

Qualitative risk assessments typically employ a set of methods, principles, or rules for assessing risk based on *non-numerical* categories or levels (such as high, medium, or low). Qualitative risk assessments use subjective analysis to help prioritize probability and impact of risk events.

The opinion of an expert in the field is a prime source for qualitative analysis. Interviews and risk workshops are two ways in which you can work with experts on managing qualitative risk.

#### Characteristics

- Assessors have limited expertise in quantitative assessments (assessors do not require as much experience when performing a qualitative assessment)
- The timeframe to complete the assessment is short
- Implementation is easier
- The organization doesn't have enough data for a quantitative assessment
- The assessors are long-term employees who have experience with the business and critical systems
- Results that are descriptive versus measurable

#### Process

- Management approval is obtained and management is kept informed
- A risk-assessment team can be formed. Members may include staff from senior management, IS, legal or compliance, internal audit, HR, facilities and safety coordination, IT, and business owners, as appropriate.
- The assessment team requests documentation
- The team sets up interviews with organizational members to identify vulnerabilities, threats, and countermeasures. All levels of staff should be represented.
- The analysis of the data gathered can be completed, which typically includes matching the threat to a vulnerability, matching threats to assets, determining how likely the threat is to exploit the vulnerability, and determining the impact to the organization in the event an exploit is successful. Analysis also includes matching of current and planned countermeasures to the threat-vulnerability pair.
- When matching is completed, risk can be calculated. In qualitative analysis, the product of likelihood and impact produces the level of risk.
- Once risk is determined, additional countermeasures can be recommended to minimize, transfer, or avoid the risk.
 When this is completed, the risk that is left over-after countermeasures have been applied to protect against the risk-is also calculated. This is the residual risk.

### Quantitative Risk Assessments

Quantitative risk assessments typically employ a set of methods, principles, or rules for assessing risk based on the use of numbers.

The hallmark of a quantitative assessment is the numeric nature of the analysis. Frequency, probability, impact, countermeasure effectiveness, and other aspects of the risk assessment have a discrete mathematical value in a pure quantitative analysis.

#### Characteristics

- Allows the assessor to determine whether the cost of the risk outweighs the cost of the countermeasure
- Requires a lot of time
- Must be performed by assessors with a significant amount of experience and particular skillset
- Subjectivity is introduced because the metrics may need to be applied to qualitative measures
- This type of assessment most effectively supports cost-benefit analyses

!!!
Most organizations are not in a position to authorize the level of work required for a quantitative risk assessment.
!!!

#### Process

Three steps are undertaken in a quantitative risk assessment:

- Management approval
- Define risk assessment team
- Review information available within the organization

!!!
Quantitative risk assessments often use values such as AV, EF, SLE, ARO, and ALE to quantify risk. Quantitative assessments lead to the proper mitigation strategy by specifying a dollar value for risks.
!!!

!!!
Often, the risk assessment an organization conducts is a combination of qualitative and quantitative methods. Fully quantitative risk assessment may not be possible because there is always some subjective input present, such as the value of information. Value of information is often one of the most difficult factors to calculate.
!!!

!!!
Unlike risk assessments, vulnerability assessments tend to focus on the technology aspects of an organization, such as the network or applications. Data gathering for vulnerability assessments typically includes the use of software tools.
!!!

## Risk Response

Risk response provides a consistent, organization-wide response to risk in accordance with the organizational risk frame by taking these steps:

- Developing alternative courses of action for responding to risk
- Evaluating the alternative courses of action
- Determining appropriate courses of action consistent with organizational risk tolerance
- Implementing risk responses based on selected courses of action

!!!
Risk response is sometimes also referred to as risk management methods or risk treatment.
!!!

Organizations have four primary ways to address risk, all of which should take into effect the cost-benefit analysis (the potential cost should not outweigh the benefit). For example, we do not put a $10 lock on a $5 bicycle:

1. Avoidance
2. Acceptance
3. Transference
4. Mitigation
5. Rejection

### Avoidance

Leaving a business opportunity because the risk is simply too high and cannot be compensated for with adequate control mechanisms-a risk that exceeds the organization's appetite.

!!!
This is the only surefire method for eliminating a specific risk.
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

There are four main categories of controls:

- Administrative Controls
- Technical Controls
- Physical Controls
- Compensating Controls

#### Administrative Controls

Administrative controls are those processes and activities that provide some aspect of security.

!!!
Examples include personnel background checks, scheduled routine log reviews, mandatory vacations, robust and comprehensive security policies and procedures, and deciding business processes so that there are no single points of failure and so that proper separation of duties exists.
!!!

#### Technical Controls

Technical (logical) controls, are those controls that enhance some facets of the CIA triad, usually operating within a system, often in electronic fashion.

!!!
Technical controls include encryption mechanisms, access control lists to limit user permissions, and audit trails and logs of system activity.
!!!

#### Physical Controls

Physical controls are controls that limit physical access to assets or that operate in a manner that reduces the impact of a physical event.''

!!!
Examples include locks on doors, fire suppression equipment in datacenters, fences, and guards.
!!!

#### Compensating Controls

Controls to catch the failure of a first control.

- Intent and rigor of the original equipment
- Provide a similar level of defense as the original requirement
- Be above and beyond other requirements
- Be commensurate with the additional risk imposed by not adhering to the requirement

### Rejection

Risk rejection isn't a legitimate form of risk response. Rejection involves ignoring risks and continuing with operations. This is essentially the same thing as accepting a risk without mitigating it to a tolerable level. In most cases, this would indicate failure of due diligence and may put the organization in a position of liability.

## Risk Monitoring

Risk monitoring is the process of keeping track of identified risks. It should be treated as an ongoing process and implemented throughout the system life cycle.

The most important elements of a risk monitoring system include the ability to:

- Clearly identify a risk
- Classify or categorize the risk
- Track the risk over time

There are three purposes of the risk-monitoring components:

- Determine the ongoing effectiveness of risk responses
- Identify risk-impacting changes
- Verify that planned risk responses are implemented and inline with organizational mission
