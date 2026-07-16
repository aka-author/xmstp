# Prescriptive Content Information Types

## About This Document

### Identification

Standard ID: PCIT.

Superior standard ID: General-Purpose Information Types (GPIT).

| ID          | Directive                                                        |
|-------------|------------------------------------------------------------------|
| D.PCIT.0000 | The agent must read General-Purpose_Information_Types.md (GPIT). |


### Purpose

This document is a standard for information types applicable to prescriptive technical documents.

The aim of this standard is to help authors structure recurring types of content consistently and correctly. The standard does not prescribe which information types must appear in a given document. Instead, it defines the rules that apply whenever an author chooses to use a particular information type.


## Terms

*Requirement:* A documented need, capability, condition, or constraint that a system, product, process, or service must satisfy.

*Requirement identifier:* A unique string permanently assigned to a requirement.


## Requirement

**Requirement** is a subtype of **Continuous prose block**.

The purpose of a **Requirement** is to 

| ID          | Requirement                                                    |
|-------------|----------------------------------------------------------------|
| R.PCIT.0100 | A **Requirement** must contain only the rubrics listed below.  |

| Rubric          | Type of Content            | Mandatory | Repetition |
|-----------------|----------------------------|-----------|------------|
| **Identifier**  | **String**                 | Yes       | Once       |
| **Statement**   | **Continuous prose block** | Yes       | Once       |

| ID          | Requirement                                                                                  |
|-------------|----------------------------------------------------------------------------------------------|
| R.PCIT.0100 | An **Identifier** must be a unique string withing the requirement specification or database. |
| R.PCIT.0100 | A **Statement** must be a series of one or more sentences each has the verb must as a predicate. |
| R.PCIT.0100 | A **Statement** must provide cross-reference if . |

* have a persistent identifier;
* use `must` for obligations;
* use `must not` for prohibitions;
* contain one verifiable obligation;
* avoid recommendations disguised as requirements;
* avoid vague verbs such as `support`, `handle`, or `provide` without a defined result;
* avoid combining independent obligations under one identifier.
