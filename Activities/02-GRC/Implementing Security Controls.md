## Implementing Security Controls

In this activity, you will draft the final piece of recommendations submitted to GeldCorp.

- You've already developed a full training plan, with target dates and a suggested delegation structure. However, training won't address the problem in the short term: It will take at least a quarter to train just 25% of the company. Improving the organization's security culture is a valuable long-term outcome, but the issue also needs to be mitigated immediately.

- The training plan is a personnel security measure, and won't drastically reduce tailgating rates until at least next year. 

- Consider physical, technical, or procedural controls that would immediately reduce employee tailgaiting.

### Instructions

  - How does this reduce tailgating?
  - What is the cost of implementation?
  - What percentage reduction in tailgaiting rates do you expect?

Control suggestions: 

1. **Implement a turnstile**. The organization could implement turnstiles in all of its data centers. 
    - These turnstiles would only allow one person through at a time and require employees to scan an ID card to proceed. 

    - This requires installing the system at all sites, and issuing keycards to all employees, both of which have significant costs attached. 

    - However, a financial organization might deem the added security of such physical access controls worth the expense.
  
2. **Encrypt top-secret data**. The attacker wouldn't have been successful if they'd broken into the data facility and stolen _encrypted_ financial records. 
    - The organization could choose to encrypt all of its top-secret data, and only allow it to be decrypted by a single server, verified by digital signature. 
    
    - As an advanced suggestion, the company could then choose to allow access to that decrypted data via API, and restrict access to this API to only trusted individuals. This is a technical control.