## Sullivan & Cromwell Phishing Email

<img width="1600" height="849" alt="2" src="https://github.com/user-attachments/assets/8de7cddc-3afc-4217-b1f4-5800417b5b5f" />


## 1. Scenario 

A phishing email was analysed in which the attacker impersonates an attorney from Sullivan & Cromwell.

## 2. Email summary 

The email appeared to be sent from an internal member of Sullivan & Cromwells legal team. It claimed that there was an overdue invoice issued to the receivers company . It included a message directing the user to settle the account urgently. 

## 3. Analysis

### Identified Indicators  
1. The sender email address mimics that of the legitimate Sullivan & Cromwell domain, but contains a subtle variation, with “Sullivan” misspelled as “sullivam”, indicating a likely spoofed domain.
2. The email contains grammatical inconsistencies, such as the incorrect use of “advise” instead of “advised”, as well as missing punctuation. These errors are common indicators of phishing attempts.
3. The message uses urgency to pressure the recipient into settling the invoice immediately, potentially bypassing standard internal approval processes.

These indicators collectively suggest a business email compromise (BEC) style phishing attempt aimed at financial fraud.

## 4. Threat Assessment
- Unlike traditional phishing attacks, this type of attack does not rely on malicious links or attachments. Instead, it uses social engineering techniques, such as urgency and impersonation, to manipulate the recipient into transferring funds.
- If successful, the organisation could suffer direct financial loss, as well as potential reputational damage and operational disruption.
- Additionally, the absence of malicious links may allow this type of email to bypass standard email filtering systems, increasing the likelihood of user interaction.
- This type of attack often targets employees involved in finance or payment processing, exploiting trust and existing business workflows.

## 5. Evidence Reviewed
- Sender email and domain structure
- Email content , including tone and language used
- Invoice request details and context
- Domain similiarity to known organisation

The analysis focused on identifying inconsistencies between the sender identity and expected communication patterns, as well as indicators of social engineering.

## 6. Diamond Model Analysis
  <img width="476" height="390" alt="Diamond Model of Intrusion Analysis scenario 1" src="https://github.com/user-attachments/assets/11d6cf05-28fe-45ae-9f3d-93513be233e5" />
Figure 1: Diamond Model representation of the analysed BEC phishing incident, illustrating the relationship between the adversary, capability, infrastructure, and victim.

The components of the model are detailed below in the context of the analysed incident:

### Adversary
The adversary is an external attacker impersonating a legal representative from Sullivan & Cromwell. The attacker is likely financially motivated and is using social engineering techniques rather than technical exploitation.

### Infrastructure
The infrastructure used in this attack is a spoofed email domain (“sullivamncromwell.com”), designed to closely resemble the legitimate organisation’s domain in order to establish credibility and evade detection.

### Capability
The attacker’s capability is Business Email Compromise (BEC), specifically using social engineering to request fraudulent invoice payments. This includes impersonation, urgency, and exploitation of business processes.

### Victim
The intended victim is an employee responsible for financial processing or invoice handling. The attacker targets this role due to their ability to authorise or process payments.

This analysis highlights how the attacker leverages trust and organisational workflows, rather than malware, to achieve their objective.

## 7. SOC Triage Output

**Alert Type**: Business Email Compromise (BEC) – Invoice Fraud  
**Category**: Phishing / Social Engineering  
**Severity**: High  
**Priority**: High  

**Analysis Summary**:
The alert involves a spoofed domain impersonating a trusted legal entity, combined with urgency to trigger an unauthorised financial transaction. No malicious links or attachments are present, indicating a BEC-style attack focused on process exploitation.

**Recommended Actio**n:
- Escalate to security and finance teams
- Do not process the invoice request
- Verify the request using trusted communication channels
- Flag or block the sender domain if confirmed malicious

**Justification**:
This alert is prioritised as high due to the potential for direct financial loss and the likelihood of bypassing traditional technical controls. The attack leverages trust and business processes, increasing the probability of user interaction.

## 8. Recommended Response Actions

- Do not process the invoice request
- Contact Sullivan & Cromwell using verified contact details to confirm legitimacy
- Notify internal security teams of the suspected BEC attempt
- Alert finance and accounts teams to prevent similar incidents
- Block or flag the spoofed domain if confirmed malicious
- Monitor for similar phishing emails targeting the organisation

## 9. Phishing Simulation Approach

To reduce the risk of similar BEC attacks, a targeted phishing simulation could be conducted focusing on employees involved in financial processes.

**The simulation would:**
- Send controlled invoice-themed phishing emails to selected users
- Replicate real-world tactics such as domain spoofing and urgency
- Encourage users to report suspicious emails through official channels

**Key Metrics:**
- Reporting rate (how many users report the email)
- Response rate (how many users engage with the request)
- Time taken to report the email

**Outcome:**
The results would be used to identify high-risk users and improve targeted security awareness training, particularly within finance-related roles.
