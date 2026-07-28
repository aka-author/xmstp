# Extensible Manual of Style for Technical Publications. Prescriptive Content Information Types

## About This Document

### Identification

Standard ID: PCIT.

Superior standard ID: General-Purpose Information Types (GPIT).

| ID          | Directive                                                                            |
|-------------|--------------------------------------------------------------------------------------|
| D.PCIT.0000 | The agent must read [General-Purpose Information Types](General-Purpose_Information_Types.md) first. |

### Purpose

This document is a standard for information types applicable to prescriptive technical documents.

The aim of this standard is to help authors structure recurring types of content consistently and correctly. The standard does not prescribe which information types must appear in a given document. Instead, it defines the rules that apply whenever an author chooses to use a particular information type.


## Prescriptions

### Prescription

**Prescription** is a subtype of **Continuous prose span**.

The purpose of a **Prescription** is to establish a normative statement concerning its subject.

| ID          | Directive                                                                                     |
|-------------|-----------------------------------------------------------------------------------------------|
| D.PCIT.0100 | The quantifiers *all*, *any*, etc., referring to an unbounded set of subjects are deprecated. |


### Positive Prescription

**Positive Prescription** is a subtype of **Prescription**.

The purpose of a **Positive Prescription** is to oblige the subject of a requirement to exhibit certain behavior or possess a certain property, quality, or capacity.

| ID          | Requirement                                                                                |
|-------------|--------------------------------------------------------------------------------------------|
| R.PCIT.0210 | A **Positive Prescription** must be a sentence with the verb *must* as its predicate.      |
| R.PCIT.0220 | The predicates *should*, *shall*, *has to* are not allowed in a **Positive Prescription**. |

| ID          | Example                                                                 |
|-------------|-------------------------------------------------------------------------|
| E.PCIT.0310 | *The system must store the user's settings.*                            |
| E.PCIT.0320 | *The report must contain a unique identifier.*                          |
| E.PCIT.0330 | *The application must display the current status.*                      |
| E.PCIT.0340 | *The device must support operation at temperatures from 0 °C to 40 °C.* |


### Negative Prescription

**Negative Prescription** is a subtype of **Prescription**.

The purpose of a **Negative Prescription** is to forbid the subject of a requirement from exhibiting certain behavior or possessing a certain property, quality, or capacity.

| ID          | Requirement                                                                             |
|-------------|-----------------------------------------------------------------------------------------|
| R.PCIT.0410 | A **Negative Prescription** must be a sentence based on one of the negative predicates. |
| R.PCIT.0420 | The predicate *must not* is not allowed in a **Negative Prescription**.                 |

The negative predicates allowed in a **Negative Prescription** are listed below:

- *is/are forbidden*
- *is/are prohibited*
- *is/are not allowed*

| ID          | Example                                                                             |
|-------------|-------------------------------------------------------------------------------------|
| E.PCIT.0510 | *Unauthorized users are forbidden from accessing the administration panel.*         |
| E.PCIT.0520 | *Modification of archived records after approval is prohibited.*                    |
| E.PCIT.0530 | *The vehicle is not allowed to operate with the service door open.*                 |
| E.PCIT.0540 | *Employees are prohibited from sharing access credentials with other users.*        |
| E.PCIT.0550 | *Deletion of audit records before the retention period expires is forbidden.*       |
| E.PCIT.0560 | *Use of default passwords in production systems is prohibited.*                     |
| E.PCIT.0570 | *The application is not allowed to store authentication credentials in plain text.* |
| E.PCIT.0590 | *Operators are forbidden from disabling the emergency shutdown function.*           |
| E.PCIT.0600 | *Transmission of personal data over an unencrypted connection is forbidden.*        |
| E.PCIT.0610 | *Installation of unsigned software packages is prohibited.*                         |


### Exceptional Prescription

**Exceptional Prescription** is a subtype of **Prescription**.

| ID          | Requirement                                                                                    |
|-------------|------------------------------------------------------------------------------------------------|
| R.PCIT.0710 | An **Exceptional Prescription** must be a sentence based on one of the exceptional predicates. |
| R.PCIT.0720 | The predicates *can* and *may* are not allowed in an **Exceptional Prescription**.             |

The exceptional predicates allowed in an **Exceptional Prescription** are listed below:

- *is/are allowed*
- *is/are acceptable*

| ID          | Example                                                                                         |
|-------------|-------------------------------------------------------------------------------------------------|
| E.PCIT.0810 | *Administrators are allowed to modify system settings.*                                         |
| E.PCIT.0820 | *Emergency maintenance is allowed outside the scheduled maintenance window.*                    |
| E.PCIT.0830 | *Deletion of archived records after the retention period expires is allowed.*                   |
| E.PCIT.0840 | *Operation without network access is acceptable in offline mode.*                               |
| E.PCIT.0850 | *A response time of up to five seconds is acceptable for batch operations.*                     |
| E.PCIT.0860 | *Use of a temporary identifier is allowed while the external registry is unavailable.*          |
| E.PCIT.0870 | *Minor differences in displayed timestamps are acceptable when caused by time-zone conversion.* |
| E.PCIT.0880 | *Operators are allowed to restart the service after an automatic recovery attempt fails.*       |


## Requirements

### Requirement Item

| ID          | Requirement                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------|
| R.PCIT.1010 | A **Requirement Item** is allowed to be accepted only in the context of its parent requirement. |

| ID          | Example                                               |
|-------------|-------------------------------------------------------|
| E.PCIT.1020 | A requirement containing all three prescription types |

```markdown
| ID      | Requirement                                                                            |
|---------|----------------------------------------------------------------------------------------|
| FN.1234 | The system must retain audit records for at least five years.                          |
| FN.1235 | The system is forbidden from modifying retained audit records.                         |
| FN.1236 | Administrators are allowed to delete audit records after the retention period expires. |
```

| ID          | Example                                    |
|-------------|--------------------------------------------|
| E.PCIT.1030 | A requirement containing two prescriptions |

```markdown
| ID      | Requirement                                                                        |
|---------|------------------------------------------------------------------------------------|
| FN.1234 | Reports must be generated in PDF format. DOCX format is allowed for draft reports. |
```

| ID          | Example                                    |
|-------------|--------------------------------------------|
| E.PCIT.1040 | A requirement containing requirement items |

```markdown
| ID        | Example                                                         |
|-----------|-----------------------------------------------------------------|
| FN.1234   | The **Hospitals** directory must contain the following columns: |
| FN.1234-A | - `Name`                                                        |
| FN.1234-B | - `City`                                                        |
| FN.1234-C | - `Zip code`                                                    |
| FN.1234-D | - `Address`                                                     |
| FN.1234-E | - `Phone number`                                                |
```

### Requirement

**Requirement** is a subtype of **Continuous prose block**.

The purpose of a **Requirement** is to state a complete, independently identifiable normative provision.

| ID          | Requirement                                                                                    |
|-------------|------------------------------------------------------------------------------------------------|
| R.PCIT.1310 | A **Requirement** must prescribe the behavior, properties, or qualities of a specific subject. |
| R.PCIT.1320 | A **Requirement** must state its meaning directly and explicitly.                              |
| R.PCIT.1330 | A **Requirement** must be a self-contained statement that makes sense out of context.          |
| R.PCIT.1340 | Pronouns referring to nouns outside the **Requirement** are not allowed in a **Requirement**.  |
| R.PCIT.1350 | A **Requirement** must contain only the rubrics listed below.                                  |

| Rubric                | Type of Content  | Mandatory | Repetition  |
|-----------------------|------------------|-----------|-------------|
| **Identifier**        | **String**       | Yes       | Once        |
| **Prescriptions**     | **Prescription** | Yes       | One or more |
| **Requirement Items** | **Requirement**  | No        | One or more |

| ID          | Example                                          |
|-------------|--------------------------------------------------|
| E.PCIT.1410 | Requirements demonstrating all information types |

```markdown
| ID        | Requirement                                                                                  |
|-----------|----------------------------------------------------------------------------------------------|
| FN.2000   | The **Users** directory must contain the following fields:                                   |
| FN.2000-A | - `User ID`                                                                                  |
| FN.2000-B | - `Name`                                                                                     |
| FN.2000-C | - `Role`                                                                                     |
| FN.2000-D | - `Status`                                                                                   |
| FN.2010   | The system must assign a unique identifier to each user.                                     |
| FN.2020   | Modification of disabled user accounts is prohibited.                                        |
| FN.2030   | Administrators are allowed to reactivate disabled user accounts.                             |
| FN.2040   | The system must retain audit records for 30 days. Earlier deletion is prohibited.            |
| FN.2050   | The system must export reports in PDF format. DOCX format is acceptable for draft reports.   |
| FN.2060   | Users are forbidden from sharing authentication credentials with other users.                |
| FN.2070   | Use of default passwords is prohibited.                                                      |
| FN.2080   | The system is not allowed to store passwords in plain text.                                  |
| FN.2090   | Temporary unavailability of the reporting service for up to five minutes is acceptable.      |
```