# Generic Requirements for a Technical Document

## About this Document

### Purpose

This document is a standard for a generic technical document outline. 

This standard is the root node of a hierarchy of interconnected standards. Each standard within this hierarchy specifies requirements for a certain aspect of technical writing such as narrative structure, document logic, terminology usage, and so on. Each standard at further levels may redefine the requirements that are specified here. 

The aim of this standard is to help authors follow the most important rules applicable to technical text and avoid the most baneful errors that can be made in technical writing. The standard does not force authors to keep any predefined document structures, style conventions, or terminology. Instead, it introduces a generic frame that should be detailed in standards at the next hierarchy levels.

Each requirement in this standard has a unique identifier. A document at a further layer redefines a requirement by introducing a replacement requirement with the same identifier. 


### Identification

Standard ID: GRTD.

Level: 1.


## Terms

*Aspect:* An angle from which a text presents its subject to readers.

*Concept:* A fact or an idea that readers completely understand or that can be explained to the readers through the relations among concepts they already understand.

*Continuous prose:* Text presented as a continuous flow of continuous prose blocks without explicit section titles inside the text.

*Continuous prose block:* A structural fragment of text used to present information inside a continuous text flow, such as a paragraph, list, table, figure, note, or example.

*Descriptive phrase:* A phrase that identifies a phenomenon through a generic term and additional descriptive properties.

*Document:* A stable body of text that has attributes allowing it to be identified.

*Genre:* Both the angle from which its subject is presented and the way the material is organized and expressed, determined by the information needs of the target audience.

*Information type:* A category of text intended to present a certain type of subject from a certain type of aspect.

> **Note**  
> An information type usually implies a specific method for structuring text and specific style conventions, including usage of specific sentence patterns.

> **Example**  
> Text that presents a task from the aspect of how to fulfill it may belong to the procedure information type. A text that presents an API method from the aspect of its parameters may belong to the reference information type. A text that presents a business process from the aspect of its stages may belong to the process description information type.

*Narrative:* A flow of statements that guides readers from facts and ideas they already know to facts and ideas they do not yet know.

*Parallel enumeration:* A text snippet that describes two or more comparable items by presenting the same set of properties for each of them.

*Phenomenon:* A product, its component, feature, process, task, domain entity, or any other thing or relation that can be recognized and discussed separately from other comparable things or relations.

*Plain enumeration:* A text snippet that describes two or more comparable items by naming them.

*Reader:* A human being, AI agent, or any intelligent entity that can accept, perceive, and use the information represented in the document. 

*Self-contained idea:* An idea that can be explained or discussed independently from another idea.

*Sentence pattern:* A recurrent sentence structure used to present a certain type of information in a consistent way.

> **Example**  
> A text may repeatedly instruct readers to click the OK button to save data. In such situations, authors should choose one sentence pattern and use it consistently throughout the text. For example, authors may choose the sentence pattern *Click OK to save the data* instead of other sentence patterns such as *Save the data by clicking OK* or *To save the data, click OK.* The other sentence patterns are not necessarily worse, but mixing them may make the text less consistent.

*Subject:* A phenomenon that a text introduces or explains to readers.

*Target audience:* A group of probable readers who share similar skills and information needs that they expect the text to satisfy. 

> **NOTE**  
> Robots and AI agents may comprise the target audience of a text as well as human beings, animals, higher and lower spirits, or aliens.

*Term:* A word or phrase that serves as the name of a specialized concept in a particular field of production, science, or art.

> **NOTE**  
> According to another definition, a term is a lexical unit of a language for special purposes that denotes a general concrete or abstract concept within the theory of a particular specialized field of knowledge or activity. 


## Framing a Document

### Targeting a Document

| Req. ID  | Requirement                                                  |
|----------|--------------------------------------------------------------|
| GRTD.101 | Each document must be written for a certain target audience. |

Examples are given below. 

| Document                                | Target Audience       |
|-----------------------------------------|-----------------------|
| Easy Reports. User Manual               | Accountants           |
| Easy Reports. Requirement Specification | Architect, developers |


### Characterizing a Document

| Req. ID  | Requirement                                                                   |
|----------|-------------------------------------------------------------------------------|
| GRTD.201 | Each document must represent a certain subject in a certain genre.            |
| GRTD.202 | The title of the document must explicitly disclose its subject and its genre. |

Examples are given below. 

| Subject      | Point of View | Genre                     | Document Title                          |
|--------------|---------------|---------------------------|-----------------------------------------|
| Easy Reports | Usage         | User Manual               | Easy Reports. User Manual               |
| Easy Reports | Requirements  | Requirement Specification | Easy Reports. Requirement Specification |


## Building Continuous Prose 

### Preferring Simple Phrases

| Req. ID  | Requirement                                              |
|----------|----------------------------------------------------------|
| GRTD.203 | Each sentence must present a single self-contained idea. |

Sentences that present more than one self-contained idea are deprecated. A sentence that provides more than one self-contained idea should be split into separate sentences. 

For example, the following sentence encloses three self-contained ideas: 

*After the system validates the configuration file successfully, it stores the parameters in the database and restarts the service automatically.*

This sentence should be split into three sentences, each delivering a self-contained idea:

*The system validates the configuration file. If the system has validated the configuration file successfully, it stores the configuration parameters in the database. Finally, the system restarts the service automatically.*


### Preferring Observable Paragraphs

## Introducing and Mentioning Concepts

### Introducing Concepts for Recognized Phenomena

| Req. ID  | Requirement                                                  |
|----------|--------------------------------------------------------------|
| GRTD.301 | A concept must be introduced to mention the same phenomenon. |
| GRTD.302 | Repeating the same descriptive phrase must be avoided.       |

Technically, an author should define a term instead of repeating the same descriptive phrase. 

An example of improper usage of descriptive phrases.

```markdown
A *user who has an account in the system* is permitted to publish articles in the system. 
A *user who does not have an account in the system* is not permitted to publish articles in the system.

A *user who has an account in the system* is permitted to write comments to articles. 
A *user who does not have an account in the system* is not permitted to write comments to articles.
```

An example of introducing concepts for phenomena that are mentioned repeatedly. 

```markdown
A *registered user* is a user that has an account in the system.

An *anonymous user* is a user that does not have an account in the system.

*Registered users* are permitted to publish articles in the system. *Anonymous users* are not permitted to publish articles in the system. 

*Registered users* are permitted to write comments to articles. *Anonymous users* are not permitted to write comments to articles.
```

### Introducing Concepts Before Using Them

| Req. ID  | Requirement                                                                                       |
|----------|---------------------------------------------------------------------------------------------------|
| GRTD.303 | Each concept that is not obvious to readers must be explicitly introduced before being mentioned. |
| GRTD.304 | Defining concepts cyclically is prohibited.                                                       |

An example of wrong concept usage: the concepts are not defined. 

```markdown
# User Manual

## Users and Their Permissions

*Registered users* are permitted to write comments to articles. *Anonymous users* are
not permitted to write comments to articles.
```

An example of wrong concept usage: the concepts are defined cyclically. 

```markdown
A *user* is a person who has an *account* in the system.

An *account* is a record in the system that describes a *user*. 
```

An example of correct concept usage: the concepts are defined before they are mentioned.

```markdown
A *user* is a person who accesses the system to utilize the features it provides.

An *account* is a record in the system that describes a *user*.

A *registered user* is a *user* that has an *account* in the system.

An *anonymous user* is a *user* that does not have an *account* in the system.

*Registered users* are permitted to write comments to articles. *Anonymous users* are 
not permitted to write comments to articles.
```


### Enumerating and Describing Subjects

#### Plain Enumeration


A plain enumeration must be represented as an unsorted list. 

#### Enumerating Structured Items

### Arranging Narratives as Cascades


**Requirements**

| Req. ID  | Requirement                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| GRTD.401 | The facts and ideas that the narrative introduces must first be enumerated and then explained. |


**Examples**

**Wrong**

```markdown
The red light prohibits traffic. Everyone must stop and wait for the yellow light.

The yellow light tells traffic participants to prepare. They should get ready to move.

The green light allows traffic. Participants must start moving.
```

**Correct**

```markdown
The traffic light gives the following signals:

* Red
* Yellow
* Green

The red light prohibits traffic. Everyone must stop and wait for the yellow light.

The yellow light tells traffic participants to prepare. They should get ready to move.

The green light allows traffic. Participants must start moving.
```

## Maintaining Parallel Text Structures

### Applying Sentence Patterns to Same Situations

### Applying Information Types to Same Aspects


