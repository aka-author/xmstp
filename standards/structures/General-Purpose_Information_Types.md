# General-Purpose Information Types

## About This Document

### Identification

Standard ID: GPIT.

Superior standard ID: Generic Requirements for a Technical Document (GRTD).


### Purpose

This document is a standard for common information types that may appear in technical documents of any kind.

This standard specifies requirements for a set of information types that are not specific to any particular document genre and may be reused across different document kinds, such as definitions, glossaries, property sheets, and similar structures.

The aim of this standard is to help authors structure recurring types of content consistently and correctly. The standard does not prescribe which information types must appear in a given document. Instead, it defines the rules that apply whenever an author chooses to use a particular information type.


## Providing the Base Text Framework

### Generic Text Block

The purpose of a generic text block is to provide a structural unit of continuous prose within a document.

| ID          | Requirement                                                             |
|-------------|-------------------------------------------------------------------------|
| R.GPIT.0100 | The generic text snippet must be a correct snippet of continuous prose. |

| ID          | Extension Point                                                                        |
|-------------|----------------------------------------------------------------------------------------|
| X.GPIT.0100 | The subordinate standards may define extensions or limitations for continuous content. |


## Giving Definitions of Concepts

### General Requirements for Definitions

The definition is a subtype of a generic text span.

The purpose of a definition is to introduce a term for a concept within running text.

| ID          | Requirement                                                                                    |
|-------------|------------------------------------------------------------------------------------------------|
| R.GPIT.0190 | A definition must be one of the following types: genus-differentia, conjunctive, generalizing. |
| R.GPIT.0200 | A definition must always be a single sentence.                                                 |


### Genus-Differentia Definitions

Genus-differentia definition is a subtype of definition.

The purpose of a genus-differentia definition is to define a term for a concept that can be formally derived from a wider concept.

| ID          | Requirement                                                        |
|-------------|--------------------------------------------------------------------|
| R.GPIT.0210 | A genus-differentia definition must narrow a broader concept down. |

| ID          | Directive                                                       |
|-------------|-----------------------------------------------------------------|
| D.GPIT.0220 | State the broader concept first, then impose limitations on it. |

A genus-differentia definition usually follows the scheme below.

`{Concept being defined} is a {broader concept} that {limitations}.`

| ID          | Example                                |
|-------------|----------------------------------------|
| E.GPIT.0230 | Writing a genus-differentia definition |

*A registered user is a user that has an account in the system.*

Here, *registered user* is the concept being defined. *User* is the broader concept. *Having an account in the system* is the limitation that distinguishes a registered user from other users.


### Conjunctive Definitions

Conjunctive definition is a subtype of definition.

The purpose of a conjunctive definition is to define an umbrella term for a few specific concepts.

| ID          | Requirement                                                     |
|-------------|-----------------------------------------------------------------|
| R.GPIT.0240 | A conjunctive definition must enumerate the concepts it unites. |

| ID          | Directive                                                  |
|-------------|------------------------------------------------------------|
| D.GPIT.0250 | List all constituent concepts explicitly and exhaustively. |

A conjunctive definition usually follows the scheme below.

`{Concept being defined} includes {constituent concept 1}, {constituent concept 2}, and {constituent concept N}.`

| ID          | Example                          |
|-------------|----------------------------------|
| E.GPIT.0260 | Writing a conjunctive definition |

*A vehicle includes automobiles, motorbikes, and bicycles.*

Here, *vehicle* is the concept being defined. *Automobiles*, *motorbikes*, and *bicycles* are the constituent concepts it unites.


### Generalizing Definitions

Generalizing definition is a subtype of definition.

The purpose of a generalizing definition is to define a term for a concept that cannot or need not be defined formally, but may rather be explained at the common sense level.

| ID          | Requirement                                                                 |
|-------------|-----------------------------------------------------------------------------|
| R.GPIT.0270 | A generalizing definition must provide representative cases of the concept. |

| ID          | Directive                                                                      |
|-------------|--------------------------------------------------------------------------------|
| D.GPIT.0280 | List the most representative cases and signal that the list is not exhaustive. |

A generalizing definition usually follows the scheme below.

`{Concept being defined} includes {case 1}, {case 2}, and other {broader concept}.`

| ID          | Example                           |
|-------------|-----------------------------------|
| E.GPIT.0290 | Writing a generalizing definition |

*Pets are cats, dogs, parrots, and other creatures people keep in their homes.*

Here, *pets* is the concept being defined. *Cats*, *dogs*, and *parrots* are representative cases. The phrase *other creatures people keep in their homes* signals that the list is not exhaustive.


## Assembling Glossaries

### Glossary Entries

Glossary entry is a subtype of generic text span.

The purpose of a glossary entry is to introduce a term within a glossary.

| ID          | Requirement                                                                   |
|-------------|-------------------------------------------------------------------------------|
| R.GPIT.0300 | A glossary entry must be derived from a definition by factoring the term out. |

| ID          | Directive                                                                                         |
|-------------|---------------------------------------------------------------------------------------------------|
| D.GPIT.0310 | Place the term first, followed by a colon, followed by the definition rephrased as a noun phrase. |

| ID          | Example                                    |
|-------------|--------------------------------------------|
| E.GPIT.0320 | Turning a definition into a glossary entry |

Given the following definition:

*A registered user is a user that has an account in the system.*

The corresponding glossary entry is:

*Registered user: a user that has an account in the system.*


### Glossaries

#### General Requirements for Glossaries

Glossary is a subtype of generic text block.

The purpose of a glossary is to give readers a list of terms with their definitions, where they can be easily found and referenced.

| ID          | Requirement                                                             |
|-------------|-------------------------------------------------------------------------|
| R.GPIT.0330 | A glossary must consist of glossary entries and optional related notes. |
| R.GPIT.0340 | A glossary must be either alphabetic or logical.                        |


#### Alphabetic Glossaries

Alphabetical glossary is a subtype of glossary.

The purpose of an alphabetical glossary is to give readers a glossary optimized for fast search of a term of interest.

| ID          | Requirement                                                               |
|-------------|---------------------------------------------------------------------------|
| R.GPIT.0350 | Entries in an alphabetic glossary must be ordered by term alphabetically. |

| ID          | Example                        |
|-------------|--------------------------------|
| E.GPIT.0360 | Writing an alphabetic glossary |

```markdown
*Account:* a record in the system that describes a registered user.

*Anonymous user:* a user that does not have an account in the system.

> **Note**
> Anonymous users have limited access to the system features.

*Registered user:* a user that has an account in the system.
```

#### Logical Glossaries

Logical glossary is a subtype of glossary.

The purpose of a logical glossary is to give readers a glossary optimized for understanding the ontology of the document.

| ID          | Requirement                                                                         |
|-------------|-------------------------------------------------------------------------------------|
| R.GPIT.0370 | A term in a logical glossary must never be defined after a definition that uses it. |

| ID          | Example                                             |
|-------------|-----------------------------------------------------|
| E.GPIT.0380 | Fixing a logical glossary with incorrect term order |

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

### Technical Parameters List

Technical parameter list is a subtype of generic text block.

The purpose of a technical parameter list is to communicate the values of technical parameters of the subject to readers.

| ID          | Requirement                                                        |
|-------------|---------------------------------------------------------------------|
| R.GPIT.0390 | A technical parameters list must contain the parts listed below.   |

| Part                  | Mandatory |
|-----------------------|-----------|
| Introduction sentence | Yes       |
| Parameter table       | Yes       |

| ID          | Requirement                                                        |
|-------------|---------------------------------------------------------------------|
| R.GPIT.0400 | The introduction sentence must explicitly reference the subject.   |
| R.GPIT.0410 | The introduction sentence must introduce the parameter table.      |

| ID          | Directive                                                                    |
|-------------|------------------------------------------------------------------------------|
| D.GPIT.0420 | The introduction phrase should apply one of the following sentence patterns. |

- `The technical parameters of {subject} are given in the table below.`
- `The {subject} has the following technical parameters.`

| ID          | Example                                |
|-------------|----------------------------------------|
| E.GPIT.0430 | The technical parameters of a firewall |

```markdown
The firewall has the following technical parameters.

| Parameter                      | Value        |
|--------------------------------|--------------|
| Maximum throughput             | 10 Gbps      |
| Supported protocols            | TCP/UDP/ICMP |
| Maximum concurrent connections | 1,000,000    |
```