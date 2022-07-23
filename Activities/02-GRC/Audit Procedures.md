## Audit Procedures

* In this activity, you'll audit how GeldCorp collects and stores user data to ensure their processes are GDPR compliant. In addition, you'll identify any data that must be protected according to PCI standards.

* If you identify any incidents of non-compliance, you'll document a way for the organization to make itself compliant.

### Instructions

1. Review GeldCorp's data collection and access practices:

    **Trading Application**

    - Users are prompted for the following data when signing up for the application:
      - Bank account number
      - Routing number
      - Credit/debit card number and security code

    - The application stores the following data about users:
      - Which stocks users own.
      - Which stocks users have been researching.
      - Which stocks users have purchased and sold.
      - Trading account balances.

    - Users are told exactly what data GeldCorp will store, but are not notified that financial advisors and developers can access their data. 

    - GeldCorp does not notify users when using their data to develop new features.

    **Financial Advisory Portal**

    - Financial advisors are able to see the following information about users:
      - Name, email, address, phone number, and birthday
      - Bank account balances
      - Trading account balances
      - Portfolio
      - Trading history
    
    - Advisors cannot modify any of this data, but all of their office computers have access to it.

    - All data is stored on fully encrypted servers.
  
    **Developers Access**
    - Developers can access all customer data, including trading and bank account details, as long as it is relevant to their projects.

**Trading Application**

- Is this category GDPR compliant?
  - No, users should be informed of what their data is being used for.

- Is this category of data protected by PCI? If so, which pieces of data must be protected?
  - Yes. Credit and debit card and CVV information are protected by PCI.

- What can GeldCorp do to improve its compliance?

  * GeldCorp must inform users when their data is being used. They must ensure that credit and debit card information is stored securely, perhaps by storing the information on an encrypted server.

**Financial Advisory Portal**

- Is this category GDPR compliant?
  - Yes.

- Is this category of data protected by PCI? If so, which pieces of data must be protected?
  - No.

- What can GeldCorp do to improve its compliance?
  - No changes are required.

**Developers Access**

- Is this category GDPR compliant?
  - No, because users aren't aware that their data is being used.

- Is this category of data protected by PCI? If so, which pieces of data must be protected?
  - Yes, developers can access customer credit and debit card information.

- What can GeldCorp do to improve its compliance?
  - GeldCorp can implement access controls on its data to prevent developers from using information they don't need.