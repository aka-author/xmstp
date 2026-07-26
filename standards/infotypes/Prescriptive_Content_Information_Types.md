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

### Positive Prescription

**Positive Prescription** is a subtype of **Prescription**.

The purpose of a **Positive Prescription** is to oblige the subject of a requirement to exhibit certain behavior or possess a certain property, quality, or capacity.

| ID          | Requirement                                                                           |
|-------------|---------------------------------------------------------------------------------------|
| R.PCIT.0110 | A **Positive Prescription** must be a sentence with the verb *must* as its predicate. |

| ID          | Example                                                                 |
|-------------|-------------------------------------------------------------------------|
| E.PCIT.0120 | *The system must store the user's settings.*                            |
| E.PCIT.0130 | *The report must contain a unique identifier.*                          |
| E.PCIT.0140 | *The application must display the current status.*                      |
| E.PCIT.0150 | *The device must support operation at temperatures from 0 °C to 40 °C.* |

### Negative Prescription

**Negative Prescription** is a subtype of **Prescription**.

The purpose of a **Negative Prescription** is to forbid the subject of a requirement from exhibiting certain behavior or possessing a certain property, quality, or capacity.

| ID          | Requirement                                                                                  |
|-------------|----------------------------------------------------------------------------------------------|
| R.PCIT.0160 | A **Negative Prescription** must be a sentence with the phrase *forbidden* as its predicate. |

| ID          | Example                                                                              |
|-------------|--------------------------------------------------------------------------------------|
| E.PCIT.0170 | *Unauthorized users are forbidden from accessing the administration panel.*          |
| E.PCIT.0180 | *The system is forbidden from deleting archived records automatically.*              |
| E.PCIT.0190 | *Personal data are forbidden from being transmitted over an unencrypted connection.* |
| E.PCIT.0200 | *The device is forbidden from operating when the protective cover is open.*          |

### Exceptional Prescription

**Exceptional Prescription** is a subtype of **Prescription**.

The purpose of an **Exceptional Prescription** is to explicitly allow the subject of a requirement to exhibit certain behavior or possess a certain property, quality, or capacity as an exception to another prescription.

| ID          | Requirement                                                                                    |
|-------------|------------------------------------------------------------------------------------------------|
| R.PCIT.0210 | An **Exceptional Prescription** must be a sentence with the phrase *allowed* as its predicate. |

| ID          | Example                                                                                      |
|-------------|----------------------------------------------------------------------------------------------|
| E.PCIT.0220 | *Administrators are allowed to modify system settings.*                                      |
| E.PCIT.0230 | *Emergency maintenance is allowed to be performed outside the scheduled maintenance window.* |
| E.PCIT.0240 | *Archived records are allowed to be deleted after the retention period expires.*             |
| E.PCIT.0250 | *The device is allowed to operate without network access in offline mode.*                   |

## Requirements

### Requirement

**Requirement** is a subtype of **Continuous prose block**.

The purpose of a **Requirement** is to state a complete, independently identifiable normative provision.

| ID          | Requirement                                                   |
|-------------|---------------------------------------------------------------|
| R.PCIT.0260 | A **Requirement** must contain only the rubrics listed below. |

| Rubric                | Type of Content  | Mandatory | Repetition  |
|-----------------------|------------------|-----------|-------------|
| **Identifier**        | **String**       | Yes       | Once        |
| **Prescriptions**     | **Prescription** | Yes       | One or more |
| **Requirement Items** | **Requirement**  | No        | One or more |

| ID          | Requirement                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------|
| R.PCIT.0270 | A **Requirement Item** is allowed to be accepted only in the context of its parent requirement. |

| ID          | Example                                               |
|-------------|-------------------------------------------------------|
| E.PCIT.0280 | A requirement containing all three prescription types |

| ID      | Requirement                                                                            |
|---------|----------------------------------------------------------------------------------------|
| FN.1234 | The system must retain audit records for at least five years.                          |
| FN.1235 | The system is forbidden from modifying retained audit records.                         |
| FN.1236 | Administrators are allowed to delete audit records after the retention period expires. |

| ID          | Example                                    |
|-------------|--------------------------------------------|
| E.PCIT.0290 | A requirement containing two prescriptions |

| ID      | Requirement                                                                        |
|---------|------------------------------------------------------------------------------------|
| FN.1234 | Reports must be generated in PDF format. DOCX format is allowed for draft reports. |

| ID          | Example                                    |
|-------------|--------------------------------------------|
| E.PCIT.0300 | A requirement containing requirement items |

```markdown
| ID        | Example                                                         |
|-----------|-----------------------------------------------------------------|
| FN.1234   | The **Hospitals** directory must contain the following columns: |
| FN.1234-A |-- `Name`                                                        |
| FN.1234-B |-- `City`                                                        |
| FN.1234-C |-- `Zip code`                                                    |
| FN.1234-D |-- `Address`                                                     |
| FN.1234-E |-- `Phone number`                                                |
```