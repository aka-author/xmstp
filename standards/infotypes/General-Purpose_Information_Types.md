# General-Purpose Information Types

## About This Document

### Identification

Standard ID: GPIT.

Superior standard ID: Generic Requirements for a Technical Document (GRTD).

| ID          | Directive                                                                                                              |
|-------------|------------------------------------------------------------------------------------------------------------------------|
| D.GPIT.0000 | The agent must read [Generic Requirements for a Technical Document](../narratives/Generic_Requirements_for_a_Technical_Document.md) first. |


### Purpose

This document is a standard for common information types that may appear in technical documents of any kind.

This standard specifies requirements for a set of information types that are not specific to any particular document genre and may be reused across different document kinds, such as definitions, glossaries, property sheets, and similar structures.

The aim of this standard is to help authors structure recurring types of content consistently and correctly. The standard does not prescribe which information types must appear in a given document. Instead, it defines the rules that apply whenever an author chooses to use a particular information type.


## Providing the Base Text Framework

### Continuous Prose Generic Information Types

**Continuous prose span** is recognized here as primitive information type.

**Continuous prose block** is recognized here as primitive information type.

The following types of content prose blocks understood at the level of common sense are recognize here as primitive information types:

- Paragraph
- Unsorted list
- Ordered list
- Figure
- Table
- Note
- Extract


## Giving Definitions of Concepts

### General Requirements for Definitions

**Definition** is a subtype of **Continuous prose span**.

The purpose of a **Definition** is to introduce a term for a concept within running text.

| ID          | Requirement                                        |
|-------------|----------------------------------------------------|
| R.GPIT.0100 | A **Definition** must always be a single sentence.                                      |
| R.GPIT.0105 | A **Definition** must be self-contained. Cross-references are prohibited in definitions. |


### Genus-Differentia Definitions

**Genus-differentia definition** is a subtype of **Definition**.

The purpose of a **Genus-differentia definition** is to define a term for a concept that can be formally derived from a wider concept.

| ID          | Requirement                                                            |
|-------------|------------------------------------------------------------------------|
| R.GPIT.0110 | A **Genus-differentia definition** must narrow a broader concept down. |

| ID          | Directive                                                       |
|-------------|-----------------------------------------------------------------|
| D.GPIT.0120 | State the broader concept first, then impose limitations on it. |

A **Genus-differentia definition** usually follows the scheme below.

`{Concept being defined} is a {broader concept} that {limitations}.`

| ID          | Example                                |
|-------------|----------------------------------------|
| E.GPIT.0130 | Writing a genus-differentia definition |

*A registered user is a user that has an account in the system.*

Here, *registered user* is the concept being defined. *User* is the broader concept. *Having an account in the system* is the limitation that distinguishes a registered user from other users.


### Conjunctive Definitions

**Conjunctive definition** is a subtype of **Definition**.

The purpose of a **Conjunctive definition** is to define an umbrella term for a few specific concepts.

| ID          | Requirement                                                         |
|-------------|---------------------------------------------------------------------|
| R.GPIT.0140 | A **Conjunctive definition** must enumerate the concepts it unites. |

| ID          | Directive                                                  |
|-------------|------------------------------------------------------------|
| D.GPIT.0150 | List all constituent concepts explicitly and exhaustively. |

A **Conjunctive definition** usually follows the scheme below.

`{Concept being defined} includes {constituent concept 1}, {constituent concept 2}, and {constituent concept N}.`

| ID          | Example                          |
|-------------|----------------------------------|
| E.GPIT.0160 | Writing a conjunctive definition |

*A vehicle includes automobiles, motorbikes, and bicycles.*

Here, *vehicle* is the concept being defined. *Automobiles*, *motorbikes*, and *bicycles* are the constituent concepts it unites.


### Generalizing Definitions

**Generalizing definition** is a subtype of **Definition**.

The purpose of a **Generalizing definition** is to define a term for a concept that cannot or need not be defined formally, but may rather be explained at the common sense level.

| ID          | Requirement                                                                     |
|-------------|---------------------------------------------------------------------------------|
| R.GPIT.0170 | A **Generalizing definition** must provide representative cases of the concept. |

| ID          | Directive                                                                      |
|-------------|--------------------------------------------------------------------------------|
| D.GPIT.0180 | List the most representative cases and signal that the list is not exhaustive. |

A **Generalizing definition** usually follows the scheme below.

`{Concept being defined} includes {case 1}, {case 2}, and other {broader concept}.`

| ID          | Example                           |
|-------------|-----------------------------------|
| E.GPIT.0190 | Writing a generalizing definition |

*Pets are cats, dogs, parrots, and other creatures people keep in their homes.*

Here, *pets* is the concept being defined. *Cats*, *dogs*, and *parrots* are representative cases. The phrase *other creatures people keep in their homes* signals that the list is not exhaustive.


## Assembling Glossaries

### Glossary Entries

**Glossary entry** is a subtype of **Continuous prose block**.

The purpose of a **Glossary entry** is to introduce a term within a **Glossary**.

| ID          | Requirement                                                 |
|-------------|-------------------------------------------------------------|
| R.GPIT.0200 | A **Glossary entry** must contain the rubrics listed below. |

| Rubric           | Type of Content | Mandatory | Repetition  |
|------------------|-----------------|-----------|-------------|
| **Gloss**        | **Paragraph**   | Yes       | Once        |
| **Explanations** | **Note**        | Note      | One or more |

| ID          | Requirement                                                                    |
|-------------|--------------------------------------------------------------------------------|
| R.GPIT.0210 | The **Gloss** must be derived from a **Definition** by factoring the term out. |

| ID          | Directive                                                                                             |
|-------------|-------------------------------------------------------------------------------------------------------|
| D.GPIT.0220 | Place the term first, followed by a colon, followed by the **Definition** rephrased as a noun phrase. |

| ID          | Example                                   |
|-------------|-------------------------------------------|
| E.GPIT.0230 | Turning a **Definition** into a **Gloss** |

Given the following **Definition**:

*A registered user is a user that has an account in the system.*

The corresponding **Glossary term introduction** is:

*Registered user: a user that has an account in the system.*


### Glossaries

#### General Requirements for Glossaries

**Glossary** is a subtype of **generic text block**.

The purpose of a **Glossary** is to give readers a list of terms with their definitions, where they can be easily found and referenced.

| ID          | Requirement                                           |
|-------------|-------------------------------------------------------|
| R.GPIT.0240 | A **Glossary** must contain the rubrics listed below. |

| Rubric             | Type of Content    | Mandatory | Repetition  |
|--------------------|--------------------|-----------|-------------|
| **Glossary entry** | **Glossary entry** | Yes       | One or more |


#### Alphabetic Glossaries

**Alphabetic glossary** is a subtype of **Glossary**.

The purpose of an **Alphabetic glossary** is to give readers a **Glossary** optimized for fast search of a term of interest.

| ID          | Requirement                                                                   |
|-------------|-------------------------------------------------------------------------------|
| R.GPIT.0250 | Entries in an **Alphabetic glossary** must be ordered by term alphabetically. |

| ID          | Example                        |
|-------------|--------------------------------|
| E.GPIT.0260 | Writing an alphabetic glossary |

```markdown
*Account:* a record in the system that describes a registered user.

*Anonymous user:* a user that does not have an account in the system.

> **Note**
> Anonymous users have limited access to the system features.

*Registered user:* a user that has an account in the system.
```


#### Logical Glossaries

**Logical glossary** is a subtype of **Glossary**.

The purpose of a **Logical glossary** is to give readers a **Glossary** optimized for understanding the ontology of the document.

| ID          | Requirement                                                                                 |
|-------------|---------------------------------------------------------------------------------------------|
| R.GPIT.0270 | A term in a **Logical glossary** must never be defined after a **Definition** that uses it. |

| ID          | Example                                             |
|-------------|-----------------------------------------------------|
| E.GPIT.0280 | Fixing a logical glossary with incorrect term order |

The following **Glossary** violates the requirement.

```markdown
*Account:* a record in the system that describes a registered user.

*User:* a person who accesses the system to utilize the features it provides.

*Anonymous user:* a user that does not have an account in the system.

*Registered user:* a user that has an account in the system.
```

The term *user* is used in the definition of *account* but defined after it.

The error is fixed below. The term *user* is moved before the entries that use it.

```markdown
*User:* a person who accesses the system to utilize the features it provides.

*Account:* a record in the system that describes a registered user.

*Anonymous user:* a user that does not have an account in the system.

*Registered user:* a user that has an account in the system.
```


## Property Sheets

### Technical Parameters List

**Technical parameters list** is a subtype of **Continuous prose block**.

The purpose of a **Technical parameters list** is to communicate the values of technical parameters of the subject to readers.

| ID          | Requirement                                                            |
|-------------|------------------------------------------------------------------------|
| R.GPIT.0290 | A **Technical parameters list** must contain the rubrics listed below. |

| Rubric                    | Type of Content | Mandatory | Repetition |
|---------------------------|-----------------|-----------|------------|
| **Introduction sentence** | **Paragraph**   | Yes       | Once       |
| **Parameter table**       | **Table**       | Yes       | Once       |

| ID          | Requirement                                                           |
|-------------|-----------------------------------------------------------------------| 
| R.GPIT.0300 | The **Introduction sentence** must explicitly reference the subject.  |
| R.GPIT.0310 | The **Introduction sentence** must introduce the **Parameter table**. |

| ID          | Directive                                                                          |
|-------------|------------------------------------------------------------------------------------|
| D.GPIT.0320 | The **Introduction sentence** should apply one of the following sentence patterns. |

- `The technical parameters of {subject} are given in the table below.`
- `The {subject} has the following technical parameters.`

| ID          | Example                                |
|-------------|----------------------------------------|
| E.GPIT.0330 | The technical parameters of a firewall |

```markdown
The firewall has the following technical parameters.

| Parameter                      | Value        |
|--------------------------------|--------------|
| Maximum throughput             | 10 Gbps      |
| Supported protocols            | TCP/UDP/ICMP |
| Maximum concurrent connections | 1,000,000    |
```
