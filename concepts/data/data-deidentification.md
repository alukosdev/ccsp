# Data Deidentification

## Summary

In certain scenarios, we may find it necessary to obscure actual data and instead use a representation of that data. Data de-identification is a method of creating a structurally similar but inauthentic version of an organization's data, typically used for purposes like software testing and user training or:

- In *test environments* where new software is tested, actual production data should never be used. However, in order to determine the actual functionality and performance of the system, it will be necessary to use data that approximates closely the same traits and characteristics of the production data.
- When *enforcing least privilege* we do not always need to show user's all elements of a dataset. For instance, a customer service representative might need to access a customer's account information, and be shown a screen with that information, but that data might be an abridged version of the customer's total account specifics.
- For *secure remote access* when a customer logs onto a web service, the customer's account may have some data abridged to avoid risks such as hijacked sessions, stolen credentials, or shoulder-surfing.

!!!
*Deidentification* is needed when you want to give a dataset to someone for statistical analysis or for testing new software but parts of the actual data (usually data that could be used to identify a person) must be hidden from them (often required by regulatory legislation).

*Encryption* is needed when you want to ensure that people who can access the files containing the data or backups can't read any of the data unless they are able to log in to the database and have database user permissions to see what they want to see. You may want to encrypt deidentified data for testing and performance measurement purposes, so that the testers can't see the identities but do find any problems arising out of the encryption as well as other problems - that's the case where both are needed.
!!!

## Data Deidentification Techniques

### Masking

==- Substitution/Randomization
Substitution/randomization is the replacement of the data (or part of the data) with random characters. Usually, other traits are left intact: length of the string, character sets, special characters, case sensitivity, etc.

There are two primary methods of substitution:

- *Random substitution*. Does not allow for reconstruction of the original data stream.
- *Algorithmic substitution*. Allows the real data to be regenerated.

!!!
This is the most effective method of applying data masking and still being able to preserve the authentic look and feel of the data records.
!!!
==- Hashing
Using a one-way cryptographic function to create a digest of the original data. Ensures data is unrecoverable and can be used as an integrity check.

Because hashing converts variable-length messages into fixed-length digests, you lose many of the properties of the original data. Additionally, you can no longer recover the original message.
==- Shuffling
Using different entries from within the same data set to represent the data. This has the obvious drawback of using actual production data.
==- Masking
Hiding the data with useless characters; for example, showing only the last four digits of a Social Security number.

Data masking is a technology that keeps the format of a data string but alters the content. For example, if you are storing development data for a system that is meant to parse SSNs, it is important that the format remain intact. Data masking ensures that the data retains its original format without being actionable by anyone who manages to intercept the data.

- *Static data masking (SDM)/static obscuring*. A new dataset is created as a copy from the original data. Only the obscured copy is used. This would be a good method to create a sample data set for testing purposes. Typically efficient when creating clean nonproduction environments.
  - Primarily used to provide high quality (i.e., realistic) data for development and testing of applications without disclosing sensitive information.
  - Includes protecting data for use in analytics and training as well as facilitating compliance with standards and regulations that require limits on the use of data that identifies individuals.
  - Facilitates cloud adoption because DevOps workloads are among the first that organizations migrate to the cloud. Masking data on-premise prior to uploading it to the cloud reduces risks for organizations concerned with cloud-based data disclosure.
- *Dynamic data masking (DDM)/dynamic obscuring*. Data is obscured as it is called (such as when the customer service agent or customer is granted authorized access, but the data is obscured as it is fed to them). Efficient when protecting production environments. It can hide the full credit card number from customer service representatives, but the data remains available for processing.
  - Primarily used to apply role-based (object-level) security for databases/applications.
  - In practice, the complexities involve in preventing masked data from being written back to the database essentially means DDM should only be applied in read-only contexts such as reporting or customer service inquiry functions.
  - Not well suited for use in a dynamic (read/write) environment such as an enterprise application because masked data could be written back to the database, corrupting the data.

!!!
Masking is not very effective for test systems but is very useful for billing scenarios. This is a common dynamic (DDM) method of masking data.
!!!
==- Deletion/Nulls
Deleting the raw data from the display before it is represented, or displaying null sets.

!!!
Other possible masking techniques include:

*Encryption*. Most complex and most significant performance decrease.
*Numeric variance*. For financial and data drive information fields.
!!!
==-

### Anonymization

Unlike masking or obfuscation, in which the data is replaced, hidden, or removed entirely, anonymization is the process of removing any *identifiable characteristics* from data. It is often used *in conjunction* with another method such as masking.

Obscuring more information about an individual to prevent aggregation or inference.

Anonymization strips out identifying information from a record.

The process of anonymization is similar to masking and includes identifying the relevant information to anonymize and choosing a relevant method for obscuring the data.

### Tokenization

Tokenization is the practice of utilizing a random or opaque value to replace what would otherwise be sensitive data.

The practice of tokenization involves having two distinct databases: one with the live, actual sensitive data, and one with nonrepresentational tokens mapped to each piece of data. In this method, the user or program calling the data is authenticated by the token server, which pulls the appropriate token from the token database, and then calls the actual data that maps to that token from the real database of production data, and finally presents it to the user or program.

1. An application collects or generates a piece of sensitive data.
2. Data is sent to the tokenization server; it is not stored locally.
3. The tokenization server generates the token. The sensitive data and the token are stored in the token database.
4. The tokenization server returns the token to the application.
5. The application stores the token rather than the original data.
6. When the sensitive data is needed, an authorized application or user can request it.

Tokenization generates a token that is used to substitute sensitive data, which itself is stored in a secured location such as a database. When accessed by a nonauthorized entity, only the token string is shown, not the actual data.

!!!
Tokenization is often used when the format of the data is important (e.g., replacing credit card numbers in an existing system that requires the same format text string). Tokenization is often implemented to satisfy the PCI DSS requirements for firms that process credit cards.
!!!
