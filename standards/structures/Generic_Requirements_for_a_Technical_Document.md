# Generic Requirements for a Technical Document

## About This Document

### Identification

Standard ID: GRTD.

Superior standard ID: None. 


### Purpose

This document is a standard for a generic technical document outline. 

This standard is the root node of a hierarchy of interconnected standards. Each standard within this hierarchy specifies requirements for a certain aspect of technical writing such as narrative structure, document logic, terminology usage, and so on. Each standard at further levels may redefine the requirements that are specified here. 

The aim of this standard is to help authors follow the most important rules applicable to technical text and avoid the most baneful errors that can be made in technical writing. The standard does not force authors to keep any predefined document structures, style conventions, or terminology. Instead, it introduces a generic frame that should be detailed in standards at the next hierarchy levels.

### Structure

The standard uses four information types to present its content.

| Information Type | Purpose                                                                       |
|------------------|-------------------------------------------------------------------------------|
| Requirement      | States a rule that technical content must comply with                         |
| Directive        | Gives practical guidance on how to comply with the preceding requirement      |
| Extension Point  | Marks a point where the standard may or should be extended at a further level |
| Example          | Provides a learn-by-example illustration of a requirement or directive        |

Each entry of any information type is introduced by a header table with the following columns.

| Column        | Description                                                                     |
|---------------|---------------------------------------------------------------------------------|
| ID            | A unique identifier of the entry                                                |
| Second column | The content of the entry: a requirement, directive, extension point, or example |

An entry may be followed by details. The details are optional and extend from the header table to the next header table or to the end of the section, whichever comes first.


### Extending the Standard

Each requirement, directive, and example in this standard has a unique identifier. A standard at a further level of the hierarchy may extend this standard by treating any of these entries in one of the following ways.

| Treatment    | Description                                                         |
|--------------|---------------------------------------------------------------------|
| Redefinition | A replacement entry with the same identifier overrides the original |
| Cancellation | The entry is explicitly declared void and no longer applies         |

Extension points work differently. An extension point cannot be redefined or cancelled. Instead, a standard at a further level introduces additional content and links it to the extension point by referring to its identifier.

The identifier of each entry follows the scheme `{type}.{standard ID}.{number}`. 

The type prefix indicates the entry kind as shown below.

| Prefix | Entry Kind      |
|--------|-----------------|
| `R`    | Requirement     |
| `D`    | Directive       |
| `X`    | Extension Point |
| `E`    | Example         |

The number is arbitrary, but the recommended practice is to use four-digit numbers with leading zeroes and a step of 10, so that entries can be inserted between existing ones without renumbering. Identifiers are shared across all entry kinds within the same standard.

Cancellation of an entry appears as follows. 

| ID          | Requirement |
|-------------|-------------|
| R.GRTD.4320 | Cancelled   |

The following techniques are available for extending the standard via extension points.

If an entire standard extends a superior standard, the extension point should be referenced in its "Identification" section.

If a certain entry extends a superior standard, the extension point should be referenced in the entry table as shown below.

| ID          | Ext. Pt.    | Requirement         |
|-------------|-------------|---------------------|
| R.ABCD.0210 | R.GRTD.4320 | A rabbit must drum. |


## Terms

*Aspect:* An angle from which a text presents its subject to readers.

*Concept:* A phenomenon, fact or an idea that readers completely understand or that can be explained to the readers through the relations among concepts they already understand.

*Continuous prose:* Text presented as a continuous flow of continuous prose blocks without explicit section titles inside the text.

*Continuous prose block:* A paragraph, list, table, figure, note, or similar structural text fragment, a member of a series of such fragments stacked top to bottom within a column or the parent fragment.

*Continuous prose span:* A word, phrase, abbreviation, inline image, or similar continuous prose fragment, arbitrarily delimited within a single block or the parent fragment and extending in the reading direction.

*Critical note:* A note that informs readers about possible hazard or other unwanted effects or consequences of their activities.

*Descriptive phrase:* A phrase that identifies a concept through a generic term and additional descriptive properties.

*Document:* A stable body of text that has attributes allowing it to be identified.

*Genre:* Both the angle from which its subject is presented and the way the material is organized and expressed, determined by the information needs of the target audience.

*Information type:* A category of text intended to present a certain type of subject from a certain type of aspect.

*Light verb:* A generic verb with weak or abstract meaning that mainly serves to express an action denoted by another word in the phrase. Light verbs include verbs such as perform, execute, conduct, make, and fulfill.

*Light verb construction:* A phrase that consists of a generic verb and a noun that denotes an action. Light verb constructions include phrases such as perform scanning, execute synchronization, conduct verification, and make a decision.

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

*Subject:* A concept that a text introduces or explains to readers.

*Target audience:* A group of probable readers who share similar skills and information needs that they expect the text to satisfy. Robots and AI agents may comprise the target audience of a text as well as human beings, animals, higher and lower spirits, or aliens.

*Term:* A word or phrase that serves as the name of a specialized concept in a particular field of production, science, or art. According to another definition, a term is a lexical unit of a language for special purposes that denotes a general concrete or abstract concept within the theory of a particular specialized field of knowledge or activity. 

*Term-related vocabulary:* The set of words and phrases regularly used together with a term in a certain context.

*Theme:* The part of a sentence that presents the known or assumed information and serves as the point of departure for what is said next.


## Words and Phrases

### Keeping Professional Vocabulary

| ID          | Requirement                            |
|-------------|----------------------------------------|
| R.GRTD.0100 | Jargon and barbarisms must be avoided. |

| ID          | Extension Point                                                       |
|-------------|-----------------------------------------------------------------------|
| X.GRTD.0110 | A list of prohibited words should be specified for a certain project. |


### Choosing the Right Level of Generality

| ID          | Requirement                                                            |
|-------------|------------------------------------------------------------------------|
| R.GRTD.0120 | Words and phrases must be as precise as possible in a certain context. |

| ID          | Directive                                                 |
|-------------|-----------------------------------------------------------|
| D.GRTD.0130 | Choose words that are neither too narrow nor too generic. |

Redundantly generic words and phrases should be avoided. At the same time, words and phrases should not describe only the most common cases while ignoring less common but realistic ones.

| ID          | Example                            |
|-------------|------------------------------------|
| E.GRTD.0140 | Adjusting the generality of a term |

Imagine a system that manages an automated parking facility. Users usually arrive by car, but some of them may ride scooters or motorbikes. In this case, the word *car* would be too narrow, *vehicle* would be precise enough, and the phrase *transportation unit* would be too generic.


### Choosing the Right Level of Formality

| ID          | Requirement                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------------|
| R.GRTD.0150 | If a term is defined for an action, then the action must be expressed as a light verb construction. |
| R.GRTD.0160 | A light verb construction must not be used for self-evident actions that have no defined term.      |

| ID          | Example                                   |
|-------------|-------------------------------------------|
| E.GRTD.0170 | Adjusting the level of phrasing formality |

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

| ID          | Requirement                                                                         |
|-------------|-------------------------------------------------------------------------------------|
| R.GRTD.0180 | A single word or set of synonyms must be chosen for a repeatedly mentioned concept. |
| R.GRTD.0190 | Different synonyms must be chosen for different repeatedly mentioned concepts.      |

| ID          | Example                                            |
|-------------|----------------------------------------------------|
| E.GRTD.0200 | Fixing the consistency of self-evident words usage |

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

| ID          | Extension Point                                                                  |
|-------------|----------------------------------------------------------------------------------|
| X.GRTD.0210 | The vocabulary of self-evident words should be restricted for a certain project. |


### Using Terms Consistently

| ID          | Requirement                                                                               |
|-------------|-------------------------------------------------------------------------------------------|
| R.GRTD.0220 | A term must never be shortened unless a shortened form or an abbreviation is declared.    |
| R.GRTD.0230 | A word derived from a term must not be treated as a term unless it is explicitly defined. |
| R.GRTD.0240 | Only a term must refer to a concept if it is defined; using synonyms is forbidden.        |
| R.GRTD.0250 | Homonyms of defined terms must not be used with different meanings.                       |

| ID          | Example                               |
|-------------|---------------------------------------|
| E.GRTD.0260 | Fixing the consistency of terms usage |

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

| ID          | Requirement                                                                                    |
|-------------|------------------------------------------------------------------------------------------------|
| R.GRTD.0270 | A single word or phrase must be chosen to express the same meaning related to a specific term. |

| ID          | Example                                           |
|-------------|---------------------------------------------------|
| E.GRTD.0280 | Fixing the consistency of term-related vocabulary |

In the following paragraph the verbs *open*, *display*, and *show* denote the same situation: the user makes the transaction browser (whatever it is) visible. Such inconsistency may mislead readers, making them think that the paragraph describes three different actions.

```markdown
Open the transaction browser from the main menu. You can then display the transaction browser by pressing Ctrl+T. If the transaction browser is hidden, show the transaction list again from the toolbar.
```

In the paragraph, the verb *open* is consistently applied to the situation when the user makes the transaction browser available.

```markdown
Open the transaction browser from the main menu. You can then open the transaction browser by pressing Ctrl+T. If the transaction browser is hidden, open the transaction browser again from the toolbar.
```

| ID          | Extension Point                                                        |
|-------------|------------------------------------------------------------------------|
| X.GRTD.0290 | Term-related words and phrases should be defined in a certain project. |


## Sentences

### Ensuring Syntactic Clarity

| ID          | Requirement                                                                  |
|-------------|------------------------------------------------------------------------------|
| R.GRTD.0300 | A noun phrase must make the relationships between its constituents explicit. |

| ID          | Example                                            |
|-------------|----------------------------------------------------|
| E.GRTD.0310 | Fixing the syntactic clarity lack in a noun phrase |

Consider the following sentence:

*The service provides computation capacities for arnocle software testing.*

The noun phrase *arnocle software testing* is ambiguous because readers might hesitate whether it refers to arnocle software or arnocle testing. If they are not familiar enough with the concept of arnocles, they have no chance to figure it out instantly. Authors had better rewrite the phrase in one of the following ways depending on its actual meaning: *testing of arnocle software* or *arnocle testing of software*.

| ID          | Requirement                                                         |
|-------------|---------------------------------------------------------------------|
| R.GRTD.0320 | Relations between actions mentioned in a sentence must be explicit. |

| ID          | Example                                                 |
|-------------|---------------------------------------------------------|
| E.GRTD.0330 | Fixing the syntactic clarity lack in a verb conjunction |

The phrase below does not disclose the relationship between clicking the button and turning video recording on.

*Click Record and turn on video recording.*

The sentence should be rewritten so that the relationship between these two actions is clarified.

| Relation Between Actions | Explicit Phrasing                                       |
|--------------------------|---------------------------------------------------------|
| Causation                | *Click Record to turn on video recording.*              |
| Sequence                 | *Click Record and then turn on video recording.*        |
| Simultaneity             | *Click Record and turn on video recording in parallel.* |


### Presenting Ideas Separately

| ID          | Requirement                                              |
|-------------|----------------------------------------------------------|
| R.GRTD.0340 | Each sentence must present a single self-contained idea. |

| ID          | Directive                                                       |
|-------------|-----------------------------------------------------------------|
| D.GRTD.0350 | Split sentences that present more than one self-contained idea. |

Sentences that present more than one self-contained idea are deprecated. A sentence that provides more than one self-contained idea should be split into separate sentences. 

| ID          | Example                                                      |
|-------------|--------------------------------------------------------------|
| E.GRTD.0360 | Splitting an overcomplicated sentence into simpler sentences |

For example, the following sentence encloses three self-contained ideas: 

*After the system validates the configuration file successfully, it stores the parameters in the database and restarts the service automatically.*

This sentence should be split into three sentences, each delivering a self-contained idea:

*The system validates the configuration file. If the system has validated the configuration file successfully, it stores the configuration parameters in the database. Finally, the system restarts the service automatically.*

| ID          | Requirement                                                                                  |
|-------------|----------------------------------------------------------------------------------------------|
| R.GRTD.0370 | Two ideas whose conflict matters for the further narrative must be treated as a single idea. |

| ID          | Example                                    |
|-------------|--------------------------------------------|
| E.GRTD.0380 | Representing a conflict as a holistic idea |

Consider the following statement:

*The firewall blocks unauthorized access. This introduces latency in high-traffic environments. Therefore, organizations must evaluate whether the security benefit justifies the performance cost before deploying it in production.*

The first sentence might confuse the readers. The reason is, it presents a well-known or even trivial fact. Having read it, one gets perplexed: "Absolutely, and so what?" The better way to describe the same situation is shown below:

*The firewall blocks unauthorized access, but it introduces latency in high-traffic environments. Therefore, organizations must evaluate whether the security benefit justifies the performance cost before deploying it in production.*


## Paragraphs

### Maintaining Paragraph Observability

| ID          | Requirement                                  |
|-------------|----------------------------------------------|
| R.GRTD.0390 | A paragraph must contain up to 10 sentences. |

| ID          | Extension Point                                                   |
|-------------|-------------------------------------------------------------------|
| X.GRTD.0400 | The limit of 10 sentences may be redefined for a certain project. |


### Restricting Pronoun References Locally

| ID          | Requirement                                                                              |
|-------------|------------------------------------------------------------------------------------------|
| R.GRTD.0410 | Pronouns must refer only to subjects explicitly mentioned earlier in the same paragraph. |

| ID          | Directive                                                                                  |
|-------------|--------------------------------------------------------------------------------------------|
| D.GRTD.0420 | Replace pronouns that refer to subjects outside the current paragraph with explicit nouns. |

| ID          | Example                 |
|-------------|-------------------------|
| E.GRTD.0430 | Fixing misused pronouns |

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

| ID          | Requirement                                                                             |
|-------------|-----------------------------------------------------------------------------------------|
| R.GRTD.0440 | The first sentence in the paragraph must introduce or mention the idea to be discussed. |
| R.GRTD.0450 | The last sentence in the paragraph must deliver a meaningful conclusion or direction.   |
| R.GRTD.0460 | The intermediate sentences in the paragraph must be organized as a train of thoughts.   |
| R.GRTD.0470 | Ideas obvious to or already introduced to the target audience must be omitted.          |

| ID          | Example                                         |
|-------------|-------------------------------------------------|
| E.GRTD.0480 | Building a train of thoughts within a paragraph |

The paragraph below keeps readers baffled until they reach the last sentence, look back, and, finally, restore the logic in their minds themselves.

*Organizations deploying firewalls must carefully evaluate the tradeoff between security and availability. Latency reduces availability. The firewall introduces latency in high-traffic environments. High traffic volumes are typical for public-facing services. Public-facing services are therefore the most affected by firewall-induced performance degradation.*

This paragraph throws an instruction at the readers and then tries to justify it. The trivial connection between latency and availability comes instantly after the direction, explaining nothing. Later, the author adds more reasons as if they doubt whether the readers believe them.

The following revision logically leads readers from the initial cause to a meaningful conclusion.

*The firewall blocks unauthorized access, but it introduces latency in high-traffic environments. This latency grows proportionally with the volume of incoming traffic. High traffic volumes are typical for public-facing services. Public-facing services are therefore the most affected by firewall-induced performance degradation. Organizations deploying firewalls in such environments must carefully evaluate the tradeoff between security and availability.*

A paragraph should be structured from exposition to conclusion. The exposition comes first. It introduces a new idea or points to a known one. The conclusion goes at the end of the paragraph. It delivers the actual value of the paragraph. The intermediate sentences build a bridge between the exposition and the conclusion. In the train of thoughts, each sentence picks up the rheme of the previous one as its new theme. This way, the reasoning advances step by step until the conclusion becomes inevitable.

The table below breaks down the connections among the sentences in the revised paragraph.

| #   | Role        | Theme                  | Rheme                                                  |
|-----|-------------|------------------------|--------------------------------------------------------|
| 1   | Exposition  | The firewall           | The conflict between security and availability         |
| 2   | Development | This latency           | Its growth proportional to traffic volume              |
| 3   | Development | High traffic volumes   | Their prevalence in public-facing services             |
| 4   | Development | Public-facing services | Their heightened exposure to availability degradation  |
| 5   | Conclusion  | The conflict           | Its organizational impact in public-facing deployments |


### Maintaining Continuous Prose Consistency

| ID          | Requirement                                                                                     |
|-------------|-------------------------------------------------------------------------------------------------|
| R.GRTD.0490 | A paragraph or a critical note must come first after the title in continuous prose.             |
| R.GRTD.0500 | A figure must be explicitly introduced in a preceding paragraph of the same continuous prose.   |
| R.GRTD.0510 | A table must be explicitly introduced in a preceding paragraph of the same continuous prose.    |
| R.GRTD.0520 | An example must be explicitly introduced in a preceding paragraph of the same continuous prose. |

| ID          | Example                               |
|-------------|---------------------------------------|
| E.GRTD.0530 | Fixing an improper table introduction |

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

## Narratives

### Managing Concepts

#### Introducing Concepts for Recognized Phenomena

| ID          | Requirement                                                  |
|-------------|--------------------------------------------------------------|
| R.GRTD.0540 | A concept must be introduced to mention the same phenomenon. |
| R.GRTD.0550 | Repeating the same descriptive phrase must be avoided.       |

| ID          | Directive                                                       |
|-------------|-----------------------------------------------------------------|
| D.GRTD.0560 | Define a term instead of repeating the same descriptive phrase. |

| ID          | Example                          |
|-------------|----------------------------------|
| E.GRTD.0570 | Conceptualizing repetitive ideas |

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

| ID          | Requirement                                                                                       |
|-------------|---------------------------------------------------------------------------------------------------|
| R.GRTD.0580 | Each concept that is not obvious to readers must be explicitly introduced before being mentioned. |
| R.GRTD.0590 | Defining concepts cyclically is prohibited.                                                       |

| ID          | Example                                      |
|-------------|----------------------------------------------|
| E.GRTD.0600 | Defining and using terms in the proper order |

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

| ID          | Requirement                                                                         |
|-------------|-------------------------------------------------------------------------------------|
| R.GRTD.0610 | An enumeration must be introduced in the paragraph directly above it.               |
| R.GRTD.0620 | The paragraph directly above the enumeration must end with the introduction phrase. |
| R.GRTD.0630 | The introduction phrase must contain a common term for the enumeration items.       |
| R.GRTD.0640 | The introduction phrase must never expose the number of enumeration items.          |
| R.GRTD.0650 | The introduction phrase must never end with a preposition or a verb.                |

| ID          | Directive                                               |
|-------------|---------------------------------------------------------|
| D.GRTD.0660 | Choose a precise common term for the enumeration items. |

Highly abstract common terms such as *object*, *subject*, or *thing* are not recommended as common terms, unless we enumerate specific objects in software design, subjects of particular scientific research, or things in someone's suitcase. Abstract nouns are acceptable as common terms when they are terms rather than words of common vocabulary.

| ID          | Directive                                                           |
|-------------|---------------------------------------------------------------------|
| D.GRTD.0670 | Use one of the standard sentence patterns for introduction phrases. |

Introduction phrases, when properly written, usually employ one of the following sentence patterns:

- *following {common term in plural}:*
- *{common term in plural} ... are listed below:*
- *{common term in plural} ... are as follows:*

| ID          | Example                                                        |
|-------------|----------------------------------------------------------------|
| E.GRTD.0680 | Fixing poorly written introduction phrases before enumerations |

Examples of poorly written introduction phrases are given below:

*The five most important features of the system are:*
*The system includes:*
*Users may pay for the service with:*

The same introduction phrases with the errors fixed are given below:

*The most important features of the system are listed below:*
*The system includes the following components:*
*Users may pay for the service with the following methods:*

| ID          | Requirement                                                                                   |
|-------------|-----------------------------------------------------------------------------------------------|
| R.GRTD.0690 | For partial enumerations, the selection criteria must be declared in the introduction phrase. |

| ID          | Directive                                                               |
|-------------|-------------------------------------------------------------------------|
| D.GRTD.0700 | Identify a selection criterion and state it in the introduction phrase. |

The selection criteria declare which subset of items is included in the enumeration and why the remaining items are omitted. The following are typical examples of selection criteria.

| Criterion      | Typical Situations                                                    |
|----------------|-----------------------------------------------------------------------|
| Importance     | The most significant, influential, or impactful items                 |
| Relevance      | Items applicable to a specific context, audience, or use case         |
| Recognition    | Items formally recognized or supported within the product or standard |
| Timeliness     | Items known, discovered, or introduced at the time of writing         |
| Unavoidability | Items that cannot be ignored, while others may be safely omitted      |

| ID          | Example                                                            |
|-------------|--------------------------------------------------------------------|
| E.GRTD.0710 | Fixing misleading introduction phrases before partial enumerations |

The following introduction phrase misinforms the readers. 

```markdown
The following types of attacks threaten the system:

- Distributed denial of service
- SQL injection
- Man-in-the-middle
```

The sad truth is that the types of attacks are far more numerous.

The introduction phrase may be rewritten as follows:

*The following types of attacks threaten the system to the greatest extent:*

| ID          | Requirement                                                                                           |
|-------------|-------------------------------------------------------------------------------------------------------|
| R.GRTD.0720 | For enumerated conditions, the relationships among them must be disclosed in the introduction phrase. |

| ID          | Example                                                         |
|-------------|-----------------------------------------------------------------|
| E.GRTD.0730 | Fixing a vague introduction phrase before enumerated conditions |

The following enumeration is poorly introduced:

```markdown
The system triggers an alert in the following cases:

- The CPU usage exceeds 90%.
- The memory usage exceeds 80%.
```

Depending on the actual logic, the introduction phrase should be rewritten in one of the following ways:

*The system triggers an alert when any of the following conditions is met:*, or
*The system triggers an alert when all of the following conditions are met simultaneously:*.

| ID          | Requirement                                                                                        |
|-------------|----------------------------------------------------------------------------------------------------|
| R.GRTD.0740 | For enumerated options, the introduction phrase must explain in which combinations they come.      |
| R.GRTD.0750 | Detailed explanations referred to in the introduction phrase must follow the enumeration directly. |

| ID          | Directive                                                                |
|-------------|--------------------------------------------------------------------------|
| D.GRTD.0760 | Identify the role of the enumerated options and their combination rules. |

Typically, the options play one of the following roles:

- Possibilities to be chosen
- Consequences that may arise
- Classification groups (exactly as in this enumeration!)

| ID          | Example                                                           |
|-------------|-------------------------------------------------------------------|
| E.GRTD.0770 | Fixing a vague introduction phrase before enumerated consequences |

The next introduction phrase leaves readers uncertain:

*The neural interface controller failure results in the following consequences:*

Depending on the relationship among the possible effects, the introduction phrase should be improved as follows.

| Relationship       | Introduction phrase                                                        |
|--------------------|----------------------------------------------------------------------------|
| Neither or one     | *... in neither or one of the following effects*                           |
| One and only one   | *... in one and only one of the following effects*                         |
| Arbitrary subset   | *... in an unpredictable combination of the following effects*             |
| Conditioned subset | *... in a certain combination of the following effects as described below* |
| Always a full set  | *... in the following set of effects*                                      |

In the case of a conditioned subset, an explanation should come directly after the enumeration.


#### Presenting Items in a Plain Enumeration

| ID          | Requirement                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| R.GRTD.0780 | An unordered list must be used to represent an enumeration if the items are ordered arbitrarily. |
| R.GRTD.0790 | An ordered list must be used to represent an enumeration if the items have an inherent order.    |

| ID          | Directive                                                  |
|-------------|------------------------------------------------------------|
| D.GRTD.0800 | Use an ordered list when the items have an inherent order. |

In particular, an ordered list is relevant in the following cases:

- Positions in a ranking or rating
- Phases of a procedure, process, or lifecycle
- Versions or releases of a product
- Concepts broadly known under their numbers, e.g. OSI/ISO layers

| ID          | Requirement                                 |
|-------------|---------------------------------------------|
| R.GRTD.0810 | An enumeration must be formally exhaustive. |

| ID          | Directive                                    |
|-------------|----------------------------------------------|
| D.GRTD.0820 | Never imply the existence of unlisted items. |

Formally exhaustive means that the enumeration must not imply the existence of unlisted items. Items such as *etc.*, *and so on*, *and others*, and *other* are therefore forbidden. If the author cannot or does not intend to enumerate all items literally, this must be reflected in the introduction phrase.

| ID          | Extension Point                                                                  |
|-------------|----------------------------------------------------------------------------------|
| X.GRTD.0830 | More cases when ordered lists are relevant may be defined for a certain project. |

| ID          | Requirement                                                                       |
|-------------|-----------------------------------------------------------------------------------|
| R.GRTD.0840 | The enumeration items must be comparable and describable by the same common term. |
| R.GRTD.0850 | The grammatical structure of the items in the same enumeration must be uniform.   |

| ID          | Directive                                                           |
|-------------|---------------------------------------------------------------------|
| D.GRTD.0860 | Choose one grammatical form and apply it consistently to all items. |

The most popular grammatical forms of enumeration items are as follows:

- Nouns and noun phrases
- Phrases with a verbal noun in gerund form as the head
- Full sentences

| ID          | Example                                       |
|-------------|-----------------------------------------------|
| E.GRTD.0870 | Making enumerated items grammatically uniform |

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

| ID          | Example                                    |
|-------------|--------------------------------------------|
| E.GRTD.0880 | Fixing a mixture of nouns and verbal nouns |

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

| ID          | Requirement                                                                              |
|-------------|------------------------------------------------------------------------------------------|
| R.GRTD.0890 | The enumeration items must never share the same beginning, unless they are unchangeable. |

| ID          | Directive                                                     |
|-------------|---------------------------------------------------------------|
| D.GRTD.0900 | Factor the shared beginning out into the introduction phrase. |

| ID          | Example                                              |
|-------------|------------------------------------------------------|
| E.GRTD.0910 | Optimizing enumeration items with the same beginning |

The items of the following enumeration share the same beginning, which violates the requirement.

```markdown
The system supports the following operations:

- Encrypting the data
- Encrypting the keys
- Encrypting the backups
```

The enumeration and its introduction phrase may be corrected as follows.

```markdown
The system supports encryption of the following targets:

- Data
- Keys
- Backups
```

Items are considered unchangeable when their wording is fixed by convention or definition. The following are typical examples:

- Proper names
- Terms
- Identifiers

| ID          | Example                                              |
|-------------|------------------------------------------------------|
| E.GRTD.0920 | Using enumerations with the same beginning correctly |

The items of the enumeration below require no corrections.

```markdown
The most influential figures named Roger in the computer industry include the following:

- Roger Needham
- Roger Penrose
- Roger Pressman
- Roger Rivest
```


#### Describing Items in a Parallel Enumeration

| ID          | Requirement                                                                               |
|-------------|-------------------------------------------------------------------------------------------|
| R.GRTD.0930 | A table must be used to represent an enumeration where the items have the same structure. |
| R.GRTD.0940 | A numbering column must be included in the table if the items have an inherent order.     |
| R.GRTD.0950 | An introduction phrase before a parallel enumeration must end with a full stop.           |

| ID          | Example                                                     |
|-------------|-------------------------------------------------------------|
| E.GRTD.0960 | Transforming a cumbersome parallel enumeration into a table |

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

| ID          | Requirement                                                                                   |
|-------------|-----------------------------------------------------------------------------------------------|
| R.GRTD.0970 | The grammatical structure and/or format of the data must be uniform within each table column. |

| ID          | Example                                                                         |
|-------------|---------------------------------------------------------------------------------|
| E.GRTD.0980 | Applying the same format to values within each column in a parallel enumeration |

The parallel enumeration shown below violates the requirement of uniformity.

```markdown
The system consists of the following modules.

| Module                | Purpose                        | Scalable                 | Release date |
|-----------------------|--------------------------------|--------------------------|--------------|
| Authentication module | Manages user authentication    | No                       | 2021-03-15   |
| Billing module        | Payment and invoice processing | Yes                      | June 2022    |
| Notification module   | Sends email and SMS alerts     | Not supported            | 03/2023      |
| Reporting module      | For generating usage reports   | Scalability is supported | 2023         |
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

| ID          | Requirement                                                                              |
|-------------|------------------------------------------------------------------------------------------|
| R.GRTD.0990 | The format used for the same data type must be uniform across all parallel enumerations. |

| ID          | Directive                                                                              |
|-------------|----------------------------------------------------------------------------------------|
| D.GRTD.1000 | Choose a single format for each data type and apply it consistently across all tables. |

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

| ID          | Requirement                                                                        |
|-------------|------------------------------------------------------------------------------------|
| R.GRTD.1010 | Items mentioned to deliver an idea rather than to be presented must remain inline. |

| ID          | Directive                                                            |
|-------------|----------------------------------------------------------------------|
| D.GRTD.1020 | Do not convert illustrative or representative items to enumerations. |

Authors sometimes mention a few items not to enumerate them exhaustively, but to give readers an orientation. This happens in the following typical cases:

- Examples that illustrate what kind of things are being discussed
- Representative cases that orient readers before going into detail

In these cases, converting the items to a list implies completeness and misleads the reader. Such items must remain part of the running text.

| ID          | Example                              |
|-------------|--------------------------------------|
| E.GRTD.1030 | Using comma-separated items properly |

The comma-separated items in the following sentence are not an enumeration:

*A modern operating system manages many resources: processes, memory, file systems, and so on.*


### Cascading Narratives

#### Introducing Subjects Within Continuous Prose

| ID          | Requirement                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| R.GRTD.1040 | The subjects that the narrative covers must first be enumerated and then explained or discussed. |

| ID          | Example                                                             |
|-------------|---------------------------------------------------------------------|
| E.GRTD.1050 | Enumerating subjects before describing them in dedicated paragraphs |

The following example demonstrates how concepts can be discussed before being introduced. The structuring shown below is not reader-friendly, because it forces readers to dive into details before capturing the whole picture.

```markdown
The red light prohibits traffic. Everyone must stop and wait for the yellow light.

The yellow light tells traffic participants to prepare. They should get ready to move.

The green light allows traffic. Participants must start moving.
```

An enumeration of concepts should come before paragraphs that discuss each concept in detail. The structure shown below is easier to follow because the reader knows what to expect before engaging with each concept in detail. This becomes especially important when the descriptions are long or complex.

```markdown
The traffic light gives the following signals:

- Red
- Yellow
- Green

The red light prohibits traffic. Everyone must stop and wait for the yellow light.

The yellow light tells traffic participants to prepare. They should get ready to move.

The green light allows traffic. Participants must start moving.
```


#### Developing Narrative Across Sections

| ID          | Requirement                                                                                      |
|-------------|--------------------------------------------------------------------------------------------------|
| R.GRTD.1060 | A section covering multiple subjects must open with an introductory subsection enumerating them. |
| R.GRTD.1070 | Each subject enumerated in the introductory subsection must have its own subsection.             |

| ID          | Example                                                                                  |
|-------------|------------------------------------------------------------------------------------------|
| E.GRTD.1080 | Enumerate subjects in an introductory subsection before dedicating a subsection to each. |

The cascading technique is applicable to formal sections. First, an introductory section must provide a holistic view of the subject. Then each part is described in a dedicated section.

| ID          | Example                                                                                       |
|-------------|-----------------------------------------------------------------------------------------------|
| E.GRTD.1090 | Introducing subjects in the introductory section before describing them in dedicated sections |

The following structure demonstrates how the cascading technique is applied at the section level. The introductory subsection gives the reader a complete picture before any details are discussed. This becomes especially important when the individual sections are long or complex.

```markdown
3. Handling Traffic Light Signals

3.1. Types of Signals

The traffic light gives the following signals:

- Red
- Yellow
- Green

3.2. Handling the Red Light
    ...

3.3. Handling the Yellow Light
    ...

3.4. Handling the Green Light
    ...
```


#### Ordering Subjects Uniformly

| ID          | Requirement                                                                                  |
|-------------|----------------------------------------------------------------------------------------------|
| R.GRTD.1100 | Subject descriptions must follow the same order in which the subjects were first enumerated. |

| ID          | Example                                                  |
|-------------|----------------------------------------------------------|
| E.GRTD.1110 | Keeping the same order when discussing the same subjects |

The following example demonstrates inconsistently ordered list items, paragraphs, and subsections.

```markdown
3. Handling Traffic Light Signals

3.1. Types of Signals

The traffic light gives the following signals:

- Red
- Yellow
- Green

The green light allows traffic. Participants must start moving.

The red light prohibits traffic. Everyone must stop and wait for the yellow light.

The yellow light tells traffic participants to prepare. They should get ready to move.

3.2. Handling the Yellow Light
    ...

3.3. Handling the Green Light
    ...

3.4. Handling the Red Light
    ...
```

The inconsistent ordering may mislead readers. Each time readers encounter an unexpected subject, they may become uncertain whether an expected subject was omitted or will be discussed later for some undisclosed reason. In addition, readers who briefly scan the document may become confused regarding navigation and subject organization.

The following improvement makes the ordering consistent and predictable for readers.

```markdown
3. Handling Traffic Light Signals

3.1. Types of Signals

The traffic light gives the following signals:

- Red
- Yellow
- Green

The red light prohibits traffic. Everyone must stop and wait for the yellow light.

The yellow light tells traffic participants to prepare. They should get ready to move.

The green light allows traffic. Participants must start moving.

3.1. Handling the Red Light
    ...

3.2. Handling the Yellow Light
    ...

3.3. Handling the Green Light
    ...
```


### Unifying Description Patterns

#### Applying Sentence Patterns to Parallel Cases

| ID          | Requirement                                                                              |
|-------------|------------------------------------------------------------------------------------------|
| R.GRTD.1120 | Parallel cases must be described with the same sentence pattern throughout the document. |

| ID          | Example                                                     |
|-------------|-------------------------------------------------------------|
| E.GRTD.1130 | Choosing a sentence pattern for a final step of a procedure |

The example below represents parallel situations described inconsistently.

```markdown
To update a client card:
...
3. Click OK to save the data.

If you want to edit a product description:
...
3. Save the data by clicking OK.

For modifying an order record:
...
3. Click OK. The data will be saved.
```

The example shown above may be improved as follows.

```markdown
To update a client card:
...
3. Click OK to save the data.

To update a product description:
...
3. Click OK to save the data.

To update an order record:
...
3. Click OK to save the data.
```

| ID          | Extension Point                                                      |
|-------------|----------------------------------------------------------------------|
| X.GRTD.1140 | A set of sentence patterns should be defined for a specific project. |


#### Applying Information Types to Parallel Subjects

| ID          | Requirement                                                                                         |
|-------------|-----------------------------------------------------------------------------------------------------|
| R.GRTD.1150 | The same information type must be used to describe parallel subjects from the same aspect.          |
| R.GRTD.1160 | An information type must prescribe a template for describing a subject from the aspect.             |
| R.GRTD.1170 | The template must define rubrics across which the subject must be described.                        |
| R.GRTD.1180 | The template must prescribe the content of each rubric, including nested subjects and their aspect. |
| R.GRTD.1190 | The template must prescribe sentence patterns to be applied in each rubric, if applicable.          |
| R.GRTD.1200 | The template must prescribe the order, mandatory status, and multiplicity of each rubric.           |


| ID          | Directive                                                                                |
|-------------|------------------------------------------------------------------------------------------|
| D.GRTD.1210 | Choose an information type and apply its template consistently to all parallel subjects. |

Readers process information faster when they know what to expect. Once a reader encounters a subject described according to a certain structure, they learn it. Every subsequent subject of the same type described from the same aspect follows the same structure, so the reader knows where to find each piece of information without scanning the text. Inconsistent structures force readers to re-orient with every new subject, which slows comprehension and increases the risk of missing critical information.

| ID          | Example                                                                      |
|-------------|------------------------------------------------------------------------------|
| E.GRTD.1220 | Choosing an information type for describing technical parameters of a device |

The following example displays two parallel subjects described inconsistently. The device is the subject, and technical parameters is the aspect in this case.

```markdown
The firewall has the following technical parameters:

- Maximum throughput: 10 Gbps
- Supported protocols: TCP, UDP, ICMP
- Maximum concurrent connections: 1,000,000

The IDS is characterized by the following technical parameters: 
throughput of up to 5 Gbps, signature-based detection, alert delivery 
via syslog and SNMP, and up to 500,000 concurrent connections.
```

Each device is described in a unique manner. This makes readers adapt to a new structure each time, which increases cognitive load and slows comprehension.

The text may be improved as follows.

```markdown
The firewall has the following technical parameters.

| Parameter                      | Value        |
|--------------------------------|--------------|
| Maximum throughput             | 10 Gbps      |
| Supported protocols            | TCP/UDP/ICMP |
| Maximum concurrent connections | 1,000,000    |

The technical parameters of the IDS are listed below.

| Parameter                      | Value           |
|--------------------------------|-----------------|
| Maximum throughput             | 5 Gbps          |
| Detection method               | Signature-based |
| Alert format                   | Syslog, SNMP    |
| Maximum concurrent connections | 500,000         |
```

Each device is described from the aspect of its technical parameters. The information type prescribes the following template:

- Introduction phrase
- Parameter table

The introduction phrase employs the following sentence pattern:

*The technical parameters of {device name} are listed below.*

The parameter table includes the following columns:

- Parameter
- Value

| ID          | Example                                            |
|-------------|----------------------------------------------------|
| E.GRTD.1230 | Choosing an information type for describing errors |

Consider one more example that displays three parallel subjects described inconsistently. The error is the subject, and its behavior and resolution is the aspect.

```markdown
Error 401

The error occurs when the authentication token is missing or expired. The system rejects the request and returns the error code to the client. The user must re-authenticate to obtain a valid token.

Error 403

Cause: the user is authenticated but lacks the required permissions.
Effect: access is denied.
Resolution: the administrator must grant the necessary permissions.

Error 503

| Rubric     | Description                                                   |
|------------|---------------------------------------------------------------|
| Cause      | The system is under excessive load or undergoing maintenance. |
| Effect     | The system is temporarily unavailable.                        |
| Resolution | The user should retry the request after a short delay.        |
```

The example may be improved as follows.

```markdown
Error 401

    Cause 
        The authentication token is missing or expired.

    Effect 
        The system rejects the request and returns the error code to the client.

    Resolution
        The user must re-authenticate to obtain a valid token.

Error 403

    Cause
        The user is authenticated but lacks the required permissions.

    Effect
        Access is denied.

    Resolution
        The administrator must grant the necessary permissions.

Error 503

    Cause
        The system is under excessive load or undergoing maintenance.

    Effect
        The system is temporarily unavailable.

    Resolution
        The user should retry the request after a short delay.
```

| ID          | Extension Point                                                      |
|-------------|----------------------------------------------------------------------|
| X.GRTD.1240 | A set of information types should be defined for a specific project. |


## Documents

### Targeting a Document

| ID          | Requirement                                                  |
|-------------|--------------------------------------------------------------|
| R.GRTD.1250 | Each document must be written for a certain target audience. |

| ID          | Example                              |
|-------------|--------------------------------------|
| E.GRTD.1260 | Identifying document target audience |

| Document                                | Target Audience       |
|-----------------------------------------|-----------------------|
| Easy Reports. User Manual               | Accountants           |
| Easy Reports. Requirement Specification | Architect, developers |


### Characterizing a Document

| ID          | Requirement                                                                   |
|-------------|-------------------------------------------------------------------------------|
| R.GRTD.1270 | Each document must represent a certain subject in a certain genre.            |
| R.GRTD.1280 | The title of the document must explicitly disclose its subject and its genre. |

| ID          | Example                    |
|-------------|----------------------------|
| E.GRTD.1290 | Assembling document titles |

| Subject      | Point of View | Genre                     | Document Title                          |
|--------------|---------------|---------------------------|-----------------------------------------|
| Easy Reports | Usage         | User Manual               | Easy Reports. User Manual               |
| Easy Reports | Requirements  | Requirement Specification | Easy Reports. Requirement Specification |
