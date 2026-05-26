# General-Purpose Information Types

## About This Document

### Identification

Standard ID: GPIT.

Superior standard ID: Generic Requirements for a Technical Document (GRTD). 


### Purpose

This document is a standard for common information types that may appear in technical documents of any kind.

This standard specifies requirements for a set of information types that are not specific to any particular document genre and may be reused across different document kinds, such as definitions, glossaries, property sheets, and similar structures.

The aim of this standard is to help authors structure recurring types of content consistently and correctly. The standard does not prescribe which information types must appear in a given document. Instead, it defines the rules that apply whenever an author chooses to use a particular information type.


## Giving Definitions of Concepts

### General Requirements for Definitions

| ID          | Requirement                                                                                    |
|-------------|------------------------------------------------------------------------------------------------|
| R.GPIT.0190 | A definition must be one of the following types: genus-differentia, conjunctive, generalizing. |
| R.GPIT.0190 | A definition must always be a single sentence.                                                 |


#### Genus-Differentia Definitions

| ID          | Requirement                                                        |
|-------------|--------------------------------------------------------------------|
| R.GPIT.0200 | A genus-differentia definition must narrow a broader concept down. |

| ID          | Directive                                                       |
|-------------|-----------------------------------------------------------------|
| D.GPIT.0210 | State the broader concept first, then impose limitations on it. |

A genus-differentia definition usually follows the scheme below.

`{Concept being defined} is a {broader concept} that {limitations}.`

| ID          | Example                                                           |
|-------------|-------------------------------------------------------------------|
| E.GPIT.0220 | Writing a genus-differentia definition                            |

*A registered user is a user that has an account in the system.*

Here, *registered user* is the concept being defined. *User* is the broader concept. *Having an account in the system* is the limitation that distinguishes a registered user from other users.


#### Conjunctive Definitions

| ID          | Requirement                                                        |
|-------------|--------------------------------------------------------------------|
| R.GPIT.0230 | A conjunctive definition must enumerate the concepts it unites.    |

| ID          | Directive                                                          |
|-------------|--------------------------------------------------------------------|
| D.GPIT.0240 | List all constituent concepts explicitly and exhaustively.         |

A conjunctive definition usually follows the scheme below.

`{Concept being defined} includes {constituent concept 1}, {constituent concept 2}, and {constituent concept N}.`

| ID          | Example                          |
|-------------|----------------------------------|
| E.GPIT.0250 | Writing a conjunctive definition |

*A vehicle includes automobiles, motorbikes, and bicycles.*

Here, *vehicle* is the concept being defined. *Automobiles*, *motorbikes*, and *bicycles* are the constituent concepts it unites.


#### Generalizing Definitions

| ID          | Requirement                                                                 |
|-------------|-----------------------------------------------------------------------------|
| R.GPIT.0260 | A generalizing definition must provide representative cases of the concept. |

| ID          | Directive                                                                      |
|-------------|--------------------------------------------------------------------------------|
| D.GPIT.0270 | List the most representative cases and signal that the list is not exhaustive. |

A generalizing definition usually follows the scheme below.

`{Concept being defined} includes {case 1}, {case 2}, and other {broader concept}.`

| ID          | Example                           |
|-------------|-----------------------------------|
| E.GPIT.0280 | Writing a generalizing definition |

*Pets are cats, dogs, parrots, and other creatures people keep in their homes.*

Here, *pets* is the concept being defined. *Cats*, *dogs*, and *parrots* are representative cases. The phrase *other creatures people keep in their homes* signals that the list is not exhaustive.


## Assembling Glossaries

### Glossary Entries

| ID          | Requirement                                                                   |
|-------------|-------------------------------------------------------------------------------|
| R.GPIT.0290 | A glossary entry must be derived from a definition by factoring the term out. |

| ID          | Directive                                                                                         |
|-------------|---------------------------------------------------------------------------------------------------|
| D.GPIT.0300 | Place the term first, followed by a colon, followed by the definition rephrased as a noun phrase. |

| ID          | Example                                    |
|-------------|--------------------------------------------|
| E.GPIT.0310 | Turning a definition into a glossary entry |

Given the following definition:

*A registered user is a user that has an account in the system.*

The corresponding glossary entry is:

*Registered user: a user that has an account in the system.*


### Glossaries

#### General Requirements for Glossaries

| ID          | Requirement                                                             |
|-------------|-------------------------------------------------------------------------|
| R.CMIT.0320 | A glossary must consist of glossary entries and optional related notes. |
| R.CMIT.0330 | A glossary must be either alphabetic or logical.                        |


#### Alphabetic Glossaries

| ID          | Requirement                                                               |
|-------------|---------------------------------------------------------------------------|
| R.CMIT.0340 | Entries in an alphabetic glossary must be ordered by term alphabetically. |

| ID          | Example                        |
|-------------|--------------------------------|
| E.CMIT.0360 | Writing an alphabetic glossary |

```markdown
*Account:* a record in the system that describes a registered user.

*Anonymous user:* a user that does not have an account in the system.

> **Note**
> Anonymous users have limited access to the system features.

*Registered user:* a user that has an account in the system.
```

#### Logical Glossaries

| ID          | Requirement                                                                         |
|-------------|-------------------------------------------------------------------------------------|
| R.CMIT.0350 | A term in a logical glossary must never be defined after a definition that uses it. |

| ID          | Example                                             |
|-------------|-----------------------------------------------------|
| E.CMIT.0370 | Fixing a logical glossary with incorrect term order |

The following glossary violates the requirement. 

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

### Technical Parameters




| ID | Example |
|----|---------|
| E.GPIT.100 |   |

```markdown
The firewall has the following technical parameters.

| Parameter                      | Value        |
|--------------------------------|--------------|
| Maximum throughput             | 10 Gbps      |
| Supported protocols            | TCP/UDP/ICMP |
| Maximum concurrent connections | 1,000,000    |
```
