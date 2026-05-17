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

*Critical note:* A note that informs readers about possible hazard or other unwanted effects or consequences of their activities.

*Descriptive phrase:* A phrase that identifies a phenomenon through a generic term and additional descriptive properties.

*Document:* A stable body of text that has attributes allowing it to be identified.

*Generic verb:* A verb with weak or abstract meaning that mainly serves to express an action denoted by another word in the phrase.

> **Examples**
> Generic verbs include verbs such as perform, execute, conduct, make, and fulfill.

*Genre:* Both the angle from which its subject is presented and the way the material is organized and expressed, determined by the information needs of the target audience.

*Information type:* A category of text intended to present a certain type of subject from a certain type of aspect.

> **Note**  
> An information type usually implies a specific method for structuring text and specific style conventions, including usage of specific sentence patterns.

> **Example**  
> Text that presents a task from the aspect of how to fulfill it may belong to the procedure information type. A text that presents an API method from the aspect of its parameters may belong to the reference information type. A text that presents a business process from the aspect of its stages may belong to the process description information type.

*Light verb:* A generic verb with weak or abstract meaning that mainly serves to express an action denoted by another word in the phrase.

*Light verb construction:* A phrase that consists of a generic verb and a noun that denotes an action.

> **Example**  
> Light verb constructions include phrases such as perform scanning, execute synchronization, conduct verification, and make a decision.

*Narrative:* A flow of statements that guides readers from facts and ideas they already know to facts and ideas they do not yet know.

*Note:* A text fragment that provides additional information related to the surrounding text.

*Noun phrase:* A phrase that usually has a noun or pronoun as its head and has the same grammatical functions as a noun.

*Parallel enumeration:* A text snippet that describes two or more comparable items by presenting the same set of properties for each of them.

*Phenomenon:* A product, its component, feature, process, task, domain entity, or any other thing or relation that can be recognized and discussed separately from other comparable things or relations.

*Plain enumeration:* A text snippet that describes two or more comparable items by naming them.

*Reader:* A human being, AI agent, or any intelligent entity that can accept, perceive, and use the information represented in the document. 

*Rheme:* The part of a sentence that presents new information about the theme.

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

*Term-related vocabulary:* The set of words and phrases regularly used together with a term in a certain context.

*Theme:* The part of a sentence that presents the known or assumed information and serves as the point of departure for what is said next.

## Words and Phrases

### Keeping Professional Vocabulary

| Req. ID  | Requirement                            |
|----------|----------------------------------------|
| GRTD.101 | Jargon and barbarisms must be avoided. |


| Ext. Pt. ID  | Extension Point                                                       |
|--------------|-----------------------------------------------------------------------|
| GRTD.101     | A list of prohibited words should be specified for a certain project. |


### Choosing the Right Level of Generality

| Req. ID  | Requirement                                                            |
|----------|------------------------------------------------------------------------|
| GRTD.101 | Words and phrases must be as precise as possible in a certain context. |

Redundantly generic words and phrases should be avoided. At the same time, words and phrases should not describe only the most common cases while ignoring less common but realistic ones.

Imagine a system that manages an automated parking facility. Users usually arrive by car, but some of them may ride scooters or motorbikes. In this case, the word *car* would be too narrow, *vehicle* would be precise enough, and the phrase *transportation unit* would be too generic.


## Choosing the Right Level of Formality

| Req. ID  | Requirement                                                                                              |
|----------|----------------------------------------------------------------------------------------------------------|
| GRTD.101 | If a term is defined for an action, then the action must be expressed as a light verb construction.      |
| GRTD.102 | A light verb construction must not be used for actions that are self-evident and have no defined term.   |

For example, the following definition is provided in the document on a hotel management system:

*Checkout room cleaning is a procedure that makes a room available for a new guest's check-in.*

In this case, we should always write *perform the checkout room cleaning* and never write
*clean the room after checkout* or other phrases with *clean* when referring specifically to this procedure.

Conversely, consider a sentence from the beginning of a manual for a robotic vacuum cleaner:

*A person should perform room cleaning as often as possible.*

The sentence above sounds unnecessarily formal. The following sentence sounds better:

*A person should clean their room as often as possible.*

The plain verb is preferable here because *room cleaning* is not a defined term in the document.


### Using Self-Evident Words Consistently

| Req. ID  | Requirement                                                                            |
|----------|----------------------------------------------------------------------------------------|
| GRTD.101 | A single word or set of synonyms must be chosen for a repeatedly mentioned phenomenon. |
| GRTD.101 | Different synonyms must be chosen for different repeatedly mentioned phenomena.        |

The following paragraph violates the requirements listed above.

```markdown
If the application has not started automatically, launch it manually from the menu. After the program is running, run the synchronization procedure.
```

The following errors are made in the previous paragraph:

- Synonyms *application* and *program* denote the same subject.
- Synonyms *start*, *launch*, and *run* denote the same effect.
- The verb *run* denotes the different activities.

The errors are fixed in the paragraph below.

```markdown
If the program has not run automatically, run it manually from the menu. After the program is running, start the synchronization procedure.
```

| Ext. Pt. ID  | Extension Point                                                                  |
|--------------|----------------------------------------------------------------------------------|
| GRTD.101     | The vocabulary of self-evident words should be restricted for a certain project. |


### Using Terms Consistently

| Req. ID  | Requirement                                                                               |
|----------|-------------------------------------------------------------------------------------------|
| GRTD.101 | A term must never be shortened unless a shortened form or an abbreviation is declared.    |
| GRTD.102 | A word derived from a term must not be treated as a term unless it is explicitly defined. |
| GRTD.102 | Only a term must refer to a phenomenon if it is defined; using synonyms is forbidden.     |
| GRTD.102 | Homonyms of defined terms must not be used with different meanings.                       |

In the following paragraph, each sentence starting from the second one violates a corresponding requirement from the list above.

```markdown
Final cleaning is the preparation of a room after a guest departs. The cleaning must be completed before the next guest checks in. Once the guest departs, the staff will finally clean the room according to the standard procedure. If final tidying up is delayed, the room remains unavailable. The cleaning of the pool is scheduled for every morning. 
```

The errors are described in the table below. 

| Sentence # | Error Explanation                                                   |
|------------|---------------------------------------------------------------------|
| 2          | The term *final cleaning* is shortened to *cleaning*.               |
| 3          | The verb *finally clean* is derived from *final cleaning*.          |
| 4          | The synonymic phrase *final tidying up* replaces the correct term.  |
| 5          | The word *cleaning* is applied to a pool as a common sense concept. |

In the following paragraph, the errors described in the previous paragraph are fixed.

```markdown
Final cleaning is the preparation of a room after a guest departs. Once the guest departs, the staff will perform final cleaning according to the standard procedure. If room servicing is delayed, final cleaning is postponed. The pool undergoes maintenance every morning.
```

### Using Term-Related Vocabulary Consistently

| Req. ID  | Requirement                                                                                    |
|----------|------------------------------------------------------------------------------------------------|
| GRTD.101 | A single word or phrase must be chosen to express the same meaning related to a specific term. |

In the following paragraph the verbs *open*, *display*, and *show* denote the same situation: the user makes the transaction browser (whatever it is) visible. Such inconsistency may mislead readers, making them think that the paragraph describes three different actions.

```markdown
Open the transaction browser from the main menu. You can then display the transaction browser by pressing Ctrl+T. If the transaction browser is hidden, show the transaction list again from the toolbar.
```

In the paragraph, the verb *open* is consistently applied to the situation when the user makes the transaction browser available.

```markdown
Open the transaction browser from the main menu. You can then open the transaction browser by pressing Ctrl+T. If the transaction browser is hidden, open the transaction browser again from the toolbar.
```

| Ext. Pt. ID  | Extension Point                                                        |
|--------------|------------------------------------------------------------------------|
| GRTD.101     | Term-related words and phrases should be defined in a certain project. |


## Sentences

### Ensuring Syntactic Clarity

| Req. ID  | Requirement                                                                  |
|----------|------------------------------------------------------------------------------|
| GRTD.203 | A noun phrase must make the relationships between its constituents explicit. |

Consider the following sentence:

*The service provides computation capacities for arnocle software testing.*

The noun phrase *arnocle software testing* is ambiguous because readers might hesitate whether it refers to arnocle software or arnocle testing. If they are not familiar enough with the concept of arnocles, they have no chance to figure it out instantly. Authors had better rewrite the phrase in one of the following ways depending on its actual meaning: *testing of arnocle software* or *arnocle testing of software*.

| Req. ID  | Requirement                                                         |
|----------|---------------------------------------------------------------------|
| GRTD.203 | Relations between actions mentioned in a sentence must be explicit. |

The phrase below does not disclose the relationship between clicking the button and turning video recording on.

*Click Record and turn on video recording.*

The sentence should be rewritten so that the relationship between these two actions is clarified.

| Relation Between Actions | Explicit Phrasing                                       |
|--------------------------|---------------------------------------------------------|
| Causation                | *Click Record to turn on video recording.*              |
| Sequence                 | *Click Record and then turn on video recording.*        |
| Simultaneity             | *Click Record and turn on video recording in parallel.* |


### Presenting Ideas Separately

| Req. ID  | Requirement                                              |
|----------|----------------------------------------------------------|
| GRTD.203 | Each sentence must present a single self-contained idea. |

Sentences that present more than one self-contained idea are deprecated. A sentence that provides more than one self-contained idea should be split into separate sentences. 

For example, the following sentence encloses three self-contained ideas: 

*After the system validates the configuration file successfully, it stores the parameters in the database and restarts the service automatically.*

This sentence should be split into three sentences, each delivering a self-contained idea:

*The system validates the configuration file. If the system has validated the configuration file successfully, it stores the configuration parameters in the database. Finally, the system restarts the service automatically.*

| Req. ID  | Requirement                                                                                  |
|----------|----------------------------------------------------------------------------------------------|
| GRTD.203 | Two ideas whose conflict matters for the further narrative must be treated as a single idea. |

Consider the following statement:

*The firewall blocks unauthorized access. This introduces latency in high-traffic environments. Therefore, organizations must evaluate whether the security benefit justifies the performance cost before deploying it in production.*

The first sentence might confuse the readers. The reason is, it presents a well-known or even trivial fact. Having read it, one gets perplexed: "Absolutely, and so what?" The better way to describe the same situation is shown below:

*The firewall blocks unauthorized access, but it introduces latency in high-traffic environments. Therefore, organizations must evaluate whether the security benefit justifies the performance cost before deploying it in production.*


## Paragraphs

### Maintaining Paragraph Observability

| Req. ID  | Requirement                                    |
|----------|------------------------------------------------|
| GRTD.205 | A paragraph should contain up to 10 sentences. |

| Ext. Pt. ID  | Extension Point                                                   |
|--------------|-------------------------------------------------------------------|
| GRTD.101     | The limit of 10 sentences may be redefined for a certain project. |


### Restricting Pronoun References Locally

| Req. ID  | Requirement                                                                      |
|----------|----------------------------------------------------------------------------------|
| GRTD.204 | Pronouns must refer only to subjects explicitly mentioned in the same paragraph. |

Pronouns that refer to subjects that are not explicitly mentioned in the same paragraph are deprecated.

Consider the example below. The pronoun *they* in the second paragraph refers to *users* or *registered users* who are mentioned only in the first paragraph. Notice that such a usage of the pronoun yields an ambiguity.

```markdown
Users can create support tickets through the web interface. 
Registered users can also attach screenshots to tickets.

They can track ticket statuses on the support page. Email 
notifications about ticket updates are also available.
```

The second paragraph should be rewritten as follows. 

```markdown
Registered users can track ticket statuses on the support page. 
Email notifications about ticket updates are also available.
```


### Implementing a Train of Thoughts within a Paragraph

| Req. ID  | Requirement                                                                             |
|----------|-----------------------------------------------------------------------------------------|
| GRTD.204 | The first sentence in the paragraph must introduce or mention the idea to be discussed. |
| GRTD.204 | The last sentence in the paragraph must deliver a meaningful conclusion or direction.   |
| GRTD.204 | The intermediate sentences in the paragraph must be organized as a train of thoughts.   |
| GRTD.204 | Ideas obvious to or already introduced to the target audience must be omitted.          |

The paragraph below keeps readers baffled until they reach the last sentence, look back, and, finally, restore the logic in their minds themselves.

*Organizations deploying firewalls must carefully evaluate the tradeoff between security and availability. Latency reduces availability. The firewall introduces latency in high-traffic environments. High traffic volumes are typical for public-facing services. Public-facing services are therefore the most affected by firewall-induced performance degradation.*

This paragraph throws an instruction at the readers and then tries to justify it. The trivial connection between latency and availability comes instantly after the direction, explaining nothing. Later, the author adds more reasons as if they doubt whether the readers believe them.

The following revision logically leads readers from the initial cause to a meaningful conclusion.

*The firewall blocks unauthorized access, but it introduces latency in high-traffic environments. This latency grows proportionally with the volume of incoming traffic. High traffic volumes are typical for public-facing services. Public-facing services are therefore the most affected by firewall-induced performance degradation. Organizations deploying firewalls in such environments must carefully evaluate the tradeoff between security and availability.*

A paragraph should be structured from exposition to conclusion. The exposition comes first. It introduces a new idea or points to a known one. The conclusion goes at the end of the paragraph. It delivers the actual value of the paragraph. The intermediate sentences build a bridge between the exposition and the conclusion. In the train of thoughts, each sentence picks up the rheme of the previous one as its new theme. This way, the reasoning advances step by step until the conclusion becomes inevitable.

The table below breaks down the connections among the sentences in the revised paragraph.

| # | Role        | Theme                  | Rheme                                                  |
|---|-------------|------------------------|--------------------------------------------------------|
| 1 | Exposition  | The firewall           | The conflict between security and availability         |
| 2 | Development | This latency           | Its growth proportional to traffic volume              |
| 3 | Development | High traffic volumes   | Their prevalence in public-facing services             |
| 4 | Development | Public-facing services | Their heightened exposure to availability degradation  |
| 5 | Conclusion  | The conflict           | Its organizational impact in public-facing deployments |


## Narrative

### Managing Concepts

#### Introducing Concepts for Recognized Phenomena

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

#### Introducing Concepts Before Using Them

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

### Enumerating Subjects

#### Introducing Enumerations

| Req. ID  | Requirement                                                                         |
|----------|-------------------------------------------------------------------------------------|
| GRTD.401 | An enumeration must be introduced in the paragraph directly above it.               |
| GRTD.401 | The paragraph directly above the enumeration must end with the introduction phrase. |
| GRTD.401 | The introduction phrase must contain a common term for the enumeration items.       |
| GRTD.401 | The introduction phrase must never expose the number of enumeration items.          |
| GRTD.401 | The introduction phrase must never end with a preposition or a verb.                |

Introduction phrases, when properly written, usually employ one of the following sentence patterns:

- *following {common term in plural}:*
- *{common term in plural} ... are listed below:*
- *{common term in plural} ... are as follows:*

Examples of poorly written introduction phrases are given below:

*The five most important features of the system are:*
*The system includes:*
*Users may pay for the service with:*

The same introduction phrases with the errors fixed are given below:

*The most important features of the system are listed below:*
*The system includes the following components:*
*Users may pay for the service with the following methods:*


#### Presenting Items in a Plain Enumeration

| Req. ID  | Requirement                                                                                      |
|----------|--------------------------------------------------------------------------------------------------|
| GRTD.401 | An unordered list must be used to represent an enumeration if the items are ordered arbitrarily. |
| GRTD.401 | An ordered list must be used to represent an enumeration if the items have an inherent order.    |

In particular, an ordered list is relevant in the following cases:

- Positions in a ranking or rating
- Phases of a procedure, process, or lifecycle
- Versions or releases of a product
- Concepts broadly known under their numbers, e.g. OSI/ISO layers

| Ext. Pt. ID  | Extension Point                                                                  |
|--------------|----------------------------------------------------------------------------------|
| GRTD.101     | More cases when ordered lists are relevant may be defined for a certain project. |

| Req. ID  | Requirement                                                                     |
|----------|---------------------------------------------------------------------------------|
| GRTD.401 | The grammatical structure of the items in the same enumeration must be uniform. |

The most popular grammatical forms of enumeration items are as follows:

- Nouns and noun phrases
- Phrases with a verbal noun in gerund form as the head
- Full sentences

The enumeration shown below violates the requirement of grammatical uniformity.

```markdown
The system supports the following authentication methods:

- Password-based login
- Using a hardware token
- Biometric
- You can also authenticate via SMS code
```

In the following example the error is fixed. The enumeration items are grammatically uniform now.

```markdown
The system supports the following authentication methods:

- Password-based login
- Hardware token
- Biometric authentication
- SMS code
```

One of the most common errors made in enumerations is mixing nouns with verbal nouns. An example is shown below.

```markdown
The system supports the following operations:

- Data encryption
- Authenticating users
- Key rotation
- Backing up the database
```

To fix such an error, authors should choose either of these two forms and correct non-fitting items. The poorly written enumeration shown above might be fixed as follows.

```markdown
The system supports the following operations:

- Data encryption
- User authentication
- Key rotation
- Database backup
```


#### Describing Items in a Parallel Enumeration

| Req. ID  | Requirement                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| GRTD.401 | A table must be used to represent an enumeration where the items have the same structure.     |
| GRTD.401 | A numbering column must be included in the table if the items have an inherent order.         |
| GRTD.401 | An introduction phrase before a parallel enumeration must end with a full stop.               |

Consider the following enumeration.

```markdown
The system consists of the following modules:

- Authentication module — manages user authentication, not scalable
- Billing module — processes payments and invoices, can be scaled horizontally
- Notification module — sends email and SMS alerts, not scalable
- Reporting module — generates usage reports, scalability is supported
```

Such an enumeration should be represented as a table.

```markdown
The system consists of the following modules.

| Module                | Purpose                         | Scalable |
|-----------------------|---------------------------------|----------|
| Authentication module | Manages user authentication     | No       |
| Billing module        | Processes payments and invoices | Yes      |
| Notification module   | Sends email and SMS alerts      | No       |
| Reporting module      | Generates usage reports         | Yes      |
```

| Req. ID  | Requirement                                                                                   |
|----------|-----------------------------------------------------------------------------------------------|
| GRTD.401 | The grammatical structure and/or format of the data must be uniform within each table column. |

The parallel enumeration shown below violates the requirement of uniformity.

```markdown
The system consists of the following modules.

| Module                | Purpose                              | Scalable      | Release date |
|-----------------------|--------------------------------------|---------------|--------------|
| Authentication module | Manages user authentication          | No            | 2021-03-15   |
| Billing module        | Payment and invoice processing       | Yes           | June 2022    |
| Notification module   | Sends email and SMS alerts           | Not supported | 03/2023      |
| Reporting module      | For generating usage reports         | Scalability is supported | 2023 |
```

In the following parallel enumeration, the error is fixed. The data is uniform within each column.

```markdown
The system consists of the following modules.

| Module                | Purpose                         | Scalable | Release date |
|-----------------------|---------------------------------|----------|--------------|
| Authentication module | Manages user authentication     | No       | 2021-03-15   |
| Billing module        | Processes payments and invoices | Yes      | 2022-06-01   |
| Notification module   | Sends email and SMS alerts      | No       | 2023-03-01   |
| Reporting module      | Generates usage reports         | Yes      | 2023-01-01   |
```

| Req. ID  | Requirement                                                                                              |
|----------|----------------------------------------------------------------------------------------------------------|
| GRTD.401 | The format used for the same data type must be uniform across all parallel enumerations in the document. |

The requirement applies to the following data types in particular.

| Data Type      | Explanation                                                                        |
|----------------|------------------------------------------------------------------------------------|
| Boolean values | A single format must be chosen, e.g. `Yes/No`, and used in all tables.             |
| Dates          | A single date format must be chosen, e.g. `YYYY-MM-DD`, and used in all tables.    |
| Magnitudes     | The same units and the same number of decimal places must be used throughout.      |
| Currency       | The same currency format must be chosen, e.g. `$1,000.00`, and used in all tables. |
| Percentages    | The same form must be chosen, e.g. `10%` or `0.10`, and used in all tables.        |

Inconsistent formatting forces readers to interpret the same kind of data differently in different places, which increases cognitive load and the risk of misreading.


#### Avoiding Redundant Enumerations

| Req. ID  | Requirement                                                                        |
|----------|------------------------------------------------------------------------------------|
| GRTD.401 | Items mentioned to deliver an idea rather than to be presented must remain inline. |

Authors sometimes mention a few items not to enumerate them exhaustively, but to give readers an orientation. This happens in the following typical cases:

- Examples that illustrate what kind of things are being discussed
- Representative cases that orient readers before going into detail

In these cases, converting the items to a list implies completeness and misleads the reader. Such items must remain part of the running text.

The comma-separated items in the following sentence are not an enumeration:

*A modern operating system manages many resources: processes, memory, file systems, and so on.*


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




## Documents


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







### Maintaining Continuous Prose Consistency

| Req. ID  | Requirement                                                                                     |
|----------|-------------------------------------------------------------------------------------------------|
| GRTD.206 | A paragraph or a critical note must come first after the title in continuous prose.             |
| GRTD.207 | A figure must be explicitly introduced in a preceding paragraph of the same continuous prose.   |
| GRTD.208 | A table must be explicitly introduced in a preceding paragraph of the same continuous prose.    |
| GRTD.209 | An example must be explicitly introduced in a preceding paragraph of the same continuous prose. |

The example below displays continuous prose where the requirements are violated:

- The table comes first after the title.
- Neither paragraph introduces the table.

```markdown
### Supported File Formats

| Format                   | Extension |
|--------------------------|-----------|
| Portable Document Format | `.pdf`    |
| Markdown                 | `.md`     |

The table above lists file formats supported by the application.
```

The example below displays continuous prose where the requirements are fulfilled:

- The paragraph comes first after the title. 
- The table is introduced in the preceding paragraph.

```markdown
### Supported File Formats

The table below lists file formats supported by the application.

| Format                   | Extension |
|--------------------------|-----------|
| Portable Document Format | `.pdf`    |
| Markdown                 | `.md`     |
```





## Maintaining Parallel Text Structures

### Applying Sentence Patterns to Same Situations

### Applying Information Types to Same Aspects


