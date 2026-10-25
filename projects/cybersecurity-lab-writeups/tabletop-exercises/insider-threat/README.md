# Insider Threat Resulting in a Data Breach

## Independent Cybersecurity Tabletop Assessment

**Project type:** Independent, scenario-based tabletop assessment
**Scenario source:** UK National Cyber Security Centre (NCSC), Exercise in a Box
**Status:** Completed
**Environment:** Fictional organisation; no live systems accessed or tested

---

## 1. Executive Summary

This project analyses a fictional insider-threat scenario in which commercially sensitive documents are discovered on social media. The scenario develops to include original documents found on an internal file server, suspected transfer using a personal USB device, and wider media attention.

The assessment considers how an organisation could investigate the disclosure, preserve and correlate evidence, limit further exposure, manage insider risk, assess regulatory obligations, communicate with stakeholders and prioritise security improvements.

A central finding from this exercise is that **authorised access, actual access and unauthorised disclosure are three separate investigative questions**. An employee having permission to open a file does not establish that they opened it, copied it or disclosed it. Conclusions should be supported by relevant evidence and recorded with appropriate limitations.

The assessment explores the following areas:

* Identification and classification of exposed information.
* Investigation and preservation of digital evidence.
* File permissions, access logging and activity monitoring.
* Least-privilege access and approval processes.
* Removable-media restrictions and alternative data-transfer channels.
* Privileged-access management and independent oversight.
* Employee investigation and procedural fairness.
* Regulatory considerations, including UK GDPR.
* Incident communications and reputational risk.
* Risk-based prioritisation and remediation planning.

The resulting recommendations focus on improving both preventive and detective security controls while maintaining appropriate investigative, legal and privacy safeguards.

**Important:** Risk ratings in this report are provisional estimates based on the fictional scenario. They are not measurements of a real organisation's security posture.

---

## 2. Background and Attribution

This project is an independent cybersecurity assessment based on the National Cyber Security Centre's (NCSC) *Exercise in a Box: Insider threat resulting in a data breach*.

The original exercise provides the scenario and discussion prompts. The analysis, risk assessment methodology, risk register, recommendations and reflections presented here are my own work.

**Original exercise:** [NCSC — Insider threat resulting in a data breach](https://www.ncsc.gov.uk/section/exercise-in-a-box/insider-threat-data-breach)

This project was completed as an individual learning exercise. It does not represent an assessment of a real organisation, and no live systems were accessed or tested.

The assessment also draws on relevant official guidance:

* [NCSC — Logging and monitoring](https://www.ncsc.gov.uk/collection/10-steps/logging-and-monitoring)
* [NCSC — Removable media controls](https://www.ncsc.gov.uk/guidance/10-steps-removablemediacontrols)
* [ICO — Personal data breaches: a guide](https://ico.org.uk/for-organisations/report-a-breach/personal-data-breach/personal-data-breaches-a-guide/)

---

## 3. Objectives and Scope

### Objectives

The objectives of this assessment were to:

1. Identify the initial investigative priorities following the discovery of a suspected data leak.
2. Distinguish authorised access, actual file access, copying or transfer, and external disclosure.
3. Evaluate preventive and detective controls relevant to insider threats.
4. Consider removable-media security and alternative data-transfer routes.
5. Examine privileged-access oversight and evidence preservation.
6. Consider employee procedures, regulatory obligations and stakeholder communications.
7. Prioritise potential security improvements using a consistent risk assessment methodology.

### Scope

The assessment covers the scenario from initial discovery through investigation, containment, organisational response and lessons learned.

Areas considered include file access, endpoint activity, removable media, alternative transfer channels, privileged accounts, personal-data breach assessment and incident communications.

### Out of Scope

This project does not include:

* Testing, scanning or accessing any real organisation or system.
* Verifying that specific security controls are deployed.
* Investigating a real employee or determining the guilt of an individual.
* Providing legal advice or making definitive legal determinations.
* Claiming that security weaknesses exist where the scenario does not establish them.

---

## 4. Scenario Overview

The NCSC exercise develops through four stages.

### Inject 1 — Initial Discovery

A user reports finding commercially sensitive documents on a social media platform.

The organisation must establish whether the documents are genuine, identify the information exposed and begin an appropriate investigation.

### Inject 2 — Internal Investigation

Original versions of the documents are identified on an internal file server.

The investigation considers who had access, which accounts may have accessed the files, and whether the disclosure resulted from accidental or deliberate activity.

### Inject 3 — Suspected Insider Transfer

The scenario indicates that an individual shared internal documents with a third party to help them bid for contracts. The documents were reportedly transferred out of the organisation using a personal USB device.

The organisation considers how removable-media controls could be strengthened.

### Inject 4 — Wider Exposure

The leaked documents receive wider attention on social media, and news organisations report on the incident.

The organisation must consider regulatory obligations, stakeholder communications and reputational consequences.

These stages provide the basis for the independent analysis below. In a real incident, conclusions would need to be supported by preserved evidence and verified facts.

---

## 5. Analysis of the Scenario Injects

### 5.1 Inject 1 — Discovery and Validation

**Scenario:** Commercially sensitive documents are reported on social media.

#### Initial investigative priorities

The organisation should:

* Record how and when the incident was reported.
* Preserve relevant URLs, screenshots, timestamps and other available evidence.
* Verify whether the documents are authentic.
* Identify the information contained within the documents.
* Determine the original storage locations.
* Assess the sensitivity and potential impact of the disclosure.
* Initiate the organisation's incident-reporting and escalation procedures.
* Establish whether the information remains accessible or is continuing to spread.

#### Identifying the exposed information

Before investigating individuals, the organisation needs to establish exactly what was disclosed.

Relevant questions include:

* What are the documents, and what do they contain?
* Are the documents genuine and complete?
* Have they been altered?
* Do they contain commercial, financial, personal or other sensitive information?
* Where have they been published?
* Who could potentially access them?
* What consequences could result from further disclosure?

This helps determine the seriousness of the incident and informs subsequent investigative and regulatory decisions.

For example, leaked tender pricing may create commercial and contractual risks. If the documents also contain personal information, the organisation must consider the potential impact on affected individuals.

#### Evidence collection

Potentially relevant evidence includes:

* Original documents and document metadata.
* Cryptographic hashes of preserved files.
* File-server access records.
* Identity and authentication logs.
* Endpoint security records.
* Removable-media connection records.
* Email and cloud-sharing records.
* Data loss prevention alerts, where available.

The usefulness of each source depends on whether it was enabled, retained and correctly configured.

Finding a document on an internal server does not establish how it left the organisation. Similarly, metadata alone may be incomplete or altered and should not be treated as conclusive proof of origin or responsibility.

**Assessment conclusion:** The initial discovery establishes a suspected disclosure requiring investigation. It does not, by itself, establish the route of disclosure or identify the responsible individual.

---

### 5.2 Inject 2 — Access, Activity and Suspected Insider Conduct

**Scenario:** Original documents are found on an internal file server, and investigators consider who could access them and whether the disclosure was accidental or deliberate.

#### Three distinct investigative stages

The investigation should distinguish between the following:

**1. Authorised access**

Which user accounts had permission to access the documents?

This can be investigated through file permissions, security group membership, user accounts and access approval records.

**2. Actual access**

Which accounts are recorded as opening, modifying or downloading the documents?

This may be established through file-server auditing, endpoint telemetry and other available records.

**3. Transfer or disclosure**

What evidence indicates that the documents were copied, transferred outside the organisation or shared with an unauthorised recipient?

This may require correlating several evidence sources, such as file-copy records, removable-media events, cloud-sharing activity and external publication evidence.

These stages are related but not interchangeable.

An account having permission to access a file does not prove that it accessed the file. Evidence that an account accessed a document does not automatically establish that the account disclosed it.

Accounts can also be compromised or shared, logs may be incomplete, and apparently suspicious activity may have a legitimate explanation.

#### Recommended investigative actions

The organisation should:

1. Review permissions and identify the accounts and groups authorised to access the documents.
2. Preserve relevant records before they are overwritten or altered.
3. Correlate timestamps and activity across relevant systems.
4. Investigate potential file transfers and external-sharing routes.
5. Construct a timeline of relevant events.
6. Record alternative explanations and distinguish established facts from hypotheses.
7. Conduct employee interviews through an appropriate and fair process.
8. Compare explanations with available evidence before reaching conclusions.

#### Access-control recommendations

The organisation should consider:

* Applying least-privilege principles.
* Requiring appropriate approval for sensitive information.
* Reviewing permissions periodically.
* Revoking access when it is no longer required.
* Monitoring relevant activity involving sensitive files.
* Maintaining documented access-control procedures.

The scenario does not establish that every one of these controls was absent. They are recommendations to assess against the organisation's actual environment.

#### Employee investigation and disciplinary response

If evidence indicates deliberate misconduct, the organisation should separate immediate security containment from employment decisions.

It may be necessary to restrict access to sensitive systems while the investigation continues. Any disciplinary decision should follow the organisation's procedures and applicable employment requirements, with an appropriate opportunity for the employee to respond.

The investigation should remain evidence-led. An allegation should not automatically be treated as a final finding.

**Assessment conclusion:** Effective investigation requires both knowledge of who could access the information and reliable evidence of what happened. Neither permissions nor a single activity record should be treated as proof of deliberate disclosure.

---

### 5.3 Inject 3 — Removable Media and Alternative Transfer Channels

**Scenario:** The exercise indicates that a personal USB device was used to transfer documents outside the organisation.

#### Identified risks

Removable media can provide a route for transferring sensitive information beyond an organisation's control.

Potential risks include:

* Unauthorised copying of confidential information.
* Loss or theft of removable storage.
* Inadequate monitoring of file transfers.
* Exposure through unencrypted storage.
* Inconsistent enforcement of removable-media policies.
* Disruption caused by overly restrictive controls without suitable business exceptions.

A policy prohibiting personal USB devices is useful, but a policy alone does not technically prevent their use.

#### Recommended controls

The organisation should consider:

**Removable-media policy**

Define which devices may be used, for what purposes, and under what approval conditions.

**Device restrictions**

Block unauthorised removable storage where appropriate. Approved-device allowlisting may be suitable where legitimate business requirements exist.

**Encryption**

Require encryption for authorised removable devices containing sensitive information.

**Monitoring**

Record relevant device connections and file-transfer activity where technically feasible and proportionate.

**Access control**

Limit access to sensitive documents and systems according to business need.

**Exception management**

Provide a documented process for authorising legitimate uses of removable storage.

**Alternative transfer channels**

Review other routes through which sensitive information could leave the organisation, including personal email, cloud storage, messaging applications and other file-sharing methods.

Data loss prevention controls may help identify or restrict certain sensitive data transfers, depending on the technology, configuration and available telemetry.

#### Encryption is not a complete solution

Encryption can protect information against unauthorised reading, particularly if a device is lost or stolen.

However, encryption does not automatically prevent an authorised insider from deliberately disclosing information or sharing the decryption key with an unauthorised recipient.

Controls must therefore address both the protection of stored data and the circumstances in which information is shared.

#### Privacy and investigative considerations

If investigators need to examine a personal USB device, they should consider their authority to do so and use a proportionate approach.

A personal device may contain private information unrelated to the incident. Investigators should seek to preserve relevant evidence while avoiding unnecessary access to unrelated personal material.

**Assessment conclusion:** Removable-media controls should be supported by technical enforcement, monitoring and clear policies. Blocking one transfer method is insufficient if other channels remain available without appropriate oversight.

---

### 5.4 Inject 4 — Regulatory Assessment and Communications

**Scenario:** The leaked documents receive widespread attention on social media, and news organisations report on the incident.

The organisation must assess its obligations and communicate appropriately with relevant stakeholders.

#### Regulatory considerations

The organisation should identify:

* What information was exposed.
* Whether personal data was included.
* Which individuals or organisations may be affected.
* The potential consequences of the disclosure.
* Which legal, regulatory or contractual obligations apply.
* Whether notification to a regulator or affected individuals is required.
* Who is responsible for making and documenting reporting decisions.

A breach involving commercially sensitive information alone does not automatically require notification to the Information Commissioner's Office (ICO) under UK GDPR.

If personal data is involved, the organisation must assess whether a personal data breach has occurred and whether it is likely to pose a risk to individuals' rights and freedoms.

Where a personal data breach is notifiable to the ICO, notification must be made without undue delay and, where feasible, within 72 hours of awareness.

Where the breach is likely to result in a high risk to individuals' rights and freedoms, affected individuals must also generally be informed without undue delay.

The organisation should consult current official guidance and appropriate advisers to determine its obligations in the specific circumstances.

**Reference:** [ICO — Personal data breaches: a guide](https://ico.org.uk/for-organisations/report-a-breach/personal-data-breach/personal-data-breaches-a-guide/)

#### Secondary exposure and OSINT considerations

Information that appears relatively harmless in isolation may become more revealing when combined with other publicly available information.

For example, a leaked business email address might be correlated with public professional profiles or other online sources. Depending on the circumstances, this could expose additional personal information or increase the risk of targeted phishing, impersonation or unwanted contact.

This possibility should be considered as part of the risk assessment. It does not automatically mean that the breach is reportable; the organisation must assess the actual information, likelihood of harm and applicable reporting threshold.

#### Incident communications

The organisation should:

1. Designate an authorised spokesperson.
2. Establish an approval process for external communications.
3. Prepare an accurate initial holding statement.
4. Avoid speculation and premature accusations.
5. Protect personal information and sensitive investigative details.
6. Provide appropriate information to employees, customers and suppliers.
7. Coordinate communications with incident responders, legal advisers and regulatory reporting processes.
8. Provide further updates when appropriate.

A holding statement might acknowledge that the organisation is investigating a reported disclosure of confidential information and has initiated appropriate response procedures.

The exact wording should reflect verified facts and applicable legal requirements.

#### Audience-specific communication

Different stakeholders may require different information.

| Audience                        | Communication priority                                                                             |
| ------------------------------- | -------------------------------------------------------------------------------------------------- |
| Journalists and the public      | Provide accurate, approved information without speculation or unnecessary disclosure.              |
| Employees                       | Explain relevant procedures, reporting channels and where to direct external enquiries.            |
| Customers                       | Explain any verified impact and provide appropriate advice or support.                             |
| Suppliers and business partners | Communicate relevant commercial risks and any actions they may need to take.                       |
| Regulators                      | Provide information required under applicable reporting obligations and within relevant deadlines. |

**Assessment conclusion:** Communication should be controlled, accurate and proportionate. Avoiding speculation is important, but it should not prevent required notifications or appropriate communication with affected stakeholders.

---

## 6. Risk Assessment Methodology

This assessment uses a simple 5 × 5 likelihood-and-impact matrix to make risk judgements and assumptions visible.

The scoring methodology and thresholds below were selected for this portfolio project. They are not presented as the NCSC's prescribed scoring system.

### 6.1 Likelihood Scale

| Score | Rating         | Definition                                   |
| ----: | -------------- | -------------------------------------------- |
|     1 | Rare           | Very unlikely in the assessed circumstances. |
|     2 | Unlikely       | Could occur, but is not expected.            |
|     3 | Possible       | Could reasonably occur.                      |
|     4 | Likely         | Expected to occur in many circumstances.     |
|     5 | Almost certain | Expected to occur frequently or imminently.  |

### 6.2 Impact Scale

| Score | Rating        | Definition                                                          |
| ----: | ------------- | ------------------------------------------------------------------- |
|     1 | Insignificant | Negligible business or operational consequences.                    |
|     2 | Minor         | Limited disruption or harm.                                         |
|     3 | Moderate      | Meaningful operational, financial or reputational consequences.     |
|     4 | Major         | Serious disruption, substantial financial loss or significant harm. |
|     5 | Severe        | Catastrophic business impact or exceptionally serious consequences. |

### 6.3 Risk Calculation

**Risk score = Likelihood × Impact**

The resulting score is mapped to the following rating bands:

| Score | Overall rating |
| ----: | -------------- |
|   1–4 | Low            |
|   5–9 | Medium         |
| 10–15 | High           |
| 16–25 | Critical       |

### 6.4 Methodology Limitations

The ratings are provisional scenario-based estimates. Likelihood and impact should be reassessed using evidence about the organisation's environment, existing controls, information sensitivity and potential consequences.

The score supports decision-making but does not replace professional judgement.

Mandatory legal or regulatory deadlines must be met regardless of the numerical risk rating.

---

## 7. Risk Register

**Important:** This register distinguishes the disclosure described in the scenario from potential control weaknesses that would need verification. The ratings are illustrative and are not findings from a real organisational audit.

| ID  | Risk or issue                                                                                                     | Likelihood | Impact | Score | Rating   | Recommended treatment                                                                               |
| --- | ----------------------------------------------------------------------------------------------------------------- | ---------: | -----: | ----: | -------- | --------------------------------------------------------------------------------------------------- |
| R01 | Continued exposure or redistribution of confidential documents already found online                               |          4 |      5 |    20 | Critical | Contain exposure where feasible, preserve evidence and coordinate incident response.                |
| R02 | Inadequate ability to establish who accessed sensitive files, if relevant logging is missing or incomplete        |          3 |      4 |    12 | High     | Verify logging coverage; configure, centralise and protect relevant records.                        |
| R03 | Unauthorised transfer through removable media, as described in the scenario                                       |          4 |      4 |    16 | Critical | Review removable-media policy, restrict unapproved devices and monitor relevant transfers.          |
| R04 | Excessive permissions allow more people than necessary to access sensitive tender documents                       |          3 |      4 |    12 | High     | Verify permissions; apply least privilege, access approval and periodic reviews.                    |
| R05 | A privileged user could alter controls or interfere with evidence without independent oversight                   |          2 |      5 |    10 | High     | Assess privileged-access arrangements, separate duties and protect logs independently.              |
| R06 | Unclear incident reporting or escalation could delay response                                                     |          3 |      3 |     9 | Medium   | Verify reporting procedures, responsibilities and escalation paths.                                 |
| R07 | Inconsistent or premature communications could increase reputational and legal risk                               |          3 |      3 |     9 | Medium   | Establish an approved communications process and audience-specific response plan.                   |
| R08 | Personal data, if present in the leaked documents, could create risks to individuals and notification obligations |          3 |      4 |    12 | High     | Identify affected data and individuals, assess risks, document decisions and notify where required. |

### 7.1 Interpretation of the Register

**R01 — Continued exposure**

This is rated Critical in the illustrative assessment because the scenario describes documents already published online. The urgency of containment depends on whether exposure is continuing, what information is involved and what mitigation is possible.

**R02 — File-access logging**

This is a potential control weakness to investigate. The rating assumes that incomplete logging would materially limit the organisation's ability to reconstruct events.

**R03 — Removable-media transfer**

The scenario describes a transfer using a personal USB device. The rating reflects the potential seriousness of unauthorised disclosure through this route. The effectiveness of the organisation's existing controls remains unverified.

**R04 — Excessive access**

The organisation should establish whether permissions are broader than necessary. The rating is provisional until actual permissions and business requirements are assessed.

**R05 — Privileged-account oversight**

A privileged user may have the ability to alter security configurations or interfere with evidence. Independent oversight and protected logging can reduce this risk.

**R06 — Incident escalation**

The organisation should verify whether employees understand how to report suspected incidents and whether responsibilities are clearly defined.

**R07 — Communications**

Inaccurate or premature statements can create additional risks. An approved process can help ensure that communication is consistent and evidence-led.

**R08 — Personal-data exposure**

This risk is conditional. The scenario information used for this assessment does not establish that personal data was included. The organisation must identify the actual content before determining applicable reporting obligations.

### 7.2 Risk Ownership

In a real organisation, each risk should have an assigned owner, agreed treatment, target date and review status.

Those details have not been assigned here because this is a desk-based assessment of a fictional organisation.

---

## 8. Prioritised Remediation Plan

The timeframes below are proposed planning categories rather than universal service-level requirements. Immediate containment and mandatory notifications take precedence where circumstances require them.

### Priority 1 — Immediate Response

**Objectives:** Limit further exposure, preserve evidence and establish the facts.

Recommended actions:

* Preserve relevant digital evidence and maintain an incident timeline.
* Assess whether the leaked information remains accessible.
* Take proportionate containment steps where possible.
* Identify the documents, their sensitivity and potentially affected parties.
* Review available file-access, endpoint, removable-media and sharing records.
* Assess applicable legal, regulatory and contractual reporting obligations.
* Assign incident leadership and coordinate communications.

### Priority 2 — Short-Term Improvements

**Objectives:** Address important gaps in investigative visibility and data protection.

Recommended actions:

* Verify auditing for sensitive file access and relevant file operations.
* Confirm that logs are collected, retained, searchable and protected against unauthorised alteration.
* Review permissions for sensitive folders and tender documents.
* Enforce a risk-based removable-media policy.
* Restrict unapproved storage devices where appropriate.
* Review personal cloud, email and other data-transfer controls.
* Confirm that incident-reporting and escalation procedures are understood.
* Review access approval and revocation processes.

### Priority 3 — Longer-Term Resilience

**Objectives:** Reduce recurrence risk and improve the organisation's ability to detect and respond to insider threats.

Recommended actions:

* Implement periodic access reviews and stronger approval for highly sensitive information.
* Assess privileged-access management and independent approval for critical security changes.
* Improve monitoring and alerting for suspicious access and data-transfer activity.
* Establish and test a coordinated incident communications plan.
* Conduct further tabletop exercises.
* Track lessons learned through to completion.
* Reassess risk ratings after controls have been implemented and tested.

### 8.1 Measuring Progress

The organisation should define how it will verify that each improvement is effective.

Possible measures include:

* Percentage of sensitive file locations covered by tested auditing.
* Completion rate of periodic access reviews.
* Percentage of privileged accounts covered by appropriate oversight.
* Compliance with removable-media policy.
* Time taken to acknowledge and escalate reported incidents.
* Completion of planned remediation actions.
* Results from subsequent exercises or control tests.

These measures are examples for future assessment, not results achieved during this project.

---

## 9. Evidence Required to Validate Recommendations

In a real assessment, the following evidence would help determine whether the recommended controls are effective.

| Evidence source                                 | Purpose                                                                         |
| ----------------------------------------------- | ------------------------------------------------------------------------------- |
| File permissions and security group memberships | Establish which accounts are authorised to access sensitive documents.          |
| File-server and identity logs                   | Reconstruct relevant access and authentication activity.                        |
| Endpoint and removable-media records            | Investigate device connections and potentially relevant file-transfer activity. |
| Cloud-sharing and email records                 | Identify possible alternative transfer routes.                                  |
| Logging configuration and retention settings    | Establish whether relevant events are captured and retained.                    |
| Privileged-account activity and change records  | Review administrative actions and security-control changes.                     |
| Removable-media and data-handling policies      | Assess whether requirements are documented and communicated.                    |
| Incident-reporting and escalation procedures    | Establish how suspected incidents should be reported and managed.               |
| Data inventory and classification records       | Identify sensitive information and support regulatory impact assessment.        |
| Control-test results and access reviews         | Determine whether controls operate as intended.                                 |

The absence of evidence should be recorded as an assessment limitation. It should not automatically be treated as proof that a control does not exist.

---

## 10. Lessons Learned and Reflection

This exercise reinforced several practical cybersecurity principles.

### 10.1 Distinguish Access from Disclosure

Permission to access a document does not prove that it was accessed, copied or disclosed.

Investigations should distinguish these stages and avoid drawing conclusions that go beyond the available evidence.

### 10.2 Build a Timeline from Multiple Sources

Reliable investigations depend on preserving and correlating evidence across relevant systems.

A single log entry or technical indicator may be insufficient to establish what happened or who was responsible.

### 10.3 Design Controls Before an Incident

Least-privilege access, removable-media restrictions and appropriate logging can reduce exposure and improve investigative capability.

Security controls are more effective when they are considered during system design rather than introduced only after a breach.

### 10.4 Apply Defence in Depth

Blocking one transfer method does not eliminate alternative routes.

Similarly, an administrator's legitimate privileges may create opportunities to bypass controls unless appropriate oversight exists.

Multiple complementary safeguards provide greater resilience than relying on a single control.

### 10.5 Balance Security, Privacy and Fairness

Investigations should be proportionate, evidence-led and consistent with applicable requirements.

This includes protecting unrelated personal information when examining devices and following appropriate procedures when investigating employee conduct.

### 10.6 Assess Regulatory Obligations Against the Actual Information Exposed

A commercial confidentiality breach does not automatically require an ICO report.

The organisation must establish whether personal data was involved, assess the applicable risk threshold and consider other relevant legal, regulatory and contractual obligations.

### 10.7 Communicate Carefully and Responsibly

Organisations should avoid speculation and premature accusations while ensuring that appropriate stakeholders receive accurate information.

Required notifications should not be unnecessarily delayed because the wider investigation is still ongoing.

### 10.8 Prioritise Using Risk and Evidence

Risk scores can help structure decisions and allocate resources.

However, ratings depend on assumptions and should be updated as evidence becomes available. A numerical score should support, rather than replace, professional judgement.

### Personal Development Outcome

This exercise provided practice in structuring an incident investigation, distinguishing facts from hypotheses, considering preventive and detective controls, and translating scenario observations into risk-based recommendations.

A useful next step would be to apply the methodology in a clearly scoped, authorised lab environment and document the evidence gathered. This would help distinguish recommendations based on scenario analysis from findings supported by practical testing.

---

## 11. References

1. National Cyber Security Centre (NCSC). [Exercise in a Box: Insider threat resulting in a data breach](https://www.ncsc.gov.uk/section/exercise-in-a-box/insider-threat-data-breach).
2. National Cyber Security Centre (NCSC). [Logging and monitoring](https://www.ncsc.gov.uk/collection/10-steps/logging-and-monitoring).
3. National Cyber Security Centre (NCSC). [Removable media controls](https://www.ncsc.gov.uk/guidance/10-steps-removablemediacontrols).
4. Information Commissioner's Office (ICO). [Personal data breaches: a guide](https://ico.org.uk/for-organisations/report-a-breach/personal-data-breach/personal-data-breaches-a-guide/).

---

**Disclaimer:** This is an educational, independent assessment of a fictional scenario. It is not legal advice, a formal audit, a penetration test or a claim that a real organisation's controls have been assessed. The NCSC exercise is credited as the source of the scenario; the analysis, risk assessment and recommendations presented here are independent portfolio work.
